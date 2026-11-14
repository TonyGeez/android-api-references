Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Character

```
class Character : Comparable<Char!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.lang.Character](https://developer.android.com/reference/kotlin/java/lang/Character#) |

The `Character` class is the java.lang# for values of the primitive type `char`. An object of type `Character` contains a single field whose type is `char`.

In addition, this class provides a large number of static methods for determining a character's category (lowercase letter, digit, etc.) and for converting characters from uppercase to lowercase and vice versa.

## Unicode Conformance

The fields and methods of class `Character` are defined in terms of character information from the Unicode Standard, specifically the *UnicodeData* file that is part of the Unicode Character Database. This file specifies properties including name and category for every assigned Unicode code point or character range. The file is available from the Unicode Consortium at <http://www.unicode.org>.

## Unicode Character Representations

The `char` data type (and therefore the value that a `Character` object encapsulates) are based on the original Unicode specification, which defined characters as fixed-width 16-bit entities. The Unicode Standard has since been changed to allow for characters whose representation requires more than 16 bits. The range of legal *code point* s is now U+0000 to U+10FFFF, known as *Unicode scalar value* . (Refer to the [*definition*](http://www.unicode.org/reports/tr27/#notation) of the U+*n* notation in the Unicode Standard.)

The set of characters from U+0000 to U+FFFF is sometimes referred to as the *Basic Multilingual Plane (BMP)* . Characters whose code points are greater than U+FFFF are called *supplementary character* s. The Java platform uses the UTF-16 representation in `char` arrays and in the `String` and `StringBuffer` classes. In this representation, supplementary characters are represented as a pair of `char` values, the first from the *high-surrogates* range, (\\uD800-\\uDBFF), the second from the *low-surrogates* range (\\uDC00-\\uDFFF).

A `char` value, therefore, represents Basic Multilingual Plane (BMP) code points, including the surrogate code points, or code units of the UTF-16 encoding. An `int` value represents all Unicode code points, including supplementary code points. The lower (least significant) 21 bits of `int` are used to represent Unicode code points and the upper (most significant) 11 bits must be zero. Unless otherwise specified, the behavior with respect to supplementary characters and surrogate `char` values is as follows:

- The methods that only accept a `char` value cannot support supplementary characters. They treat `char` values from the surrogate ranges as undefined characters. For example, `Character.isLetter('\u005CuD840')` returns `false`, even though this specific value if followed by any low-surrogate value in a string would represent a letter.
- The methods that accept an `int` value support all Unicode characters, including supplementary characters. For example, `Character.isLetter(0x2F81A)` returns `true` because the code point value represents a letter (a CJK ideograph).

In the Java SE API documentation, *Unicode code point* is used for character values in the range between U+0000 and U+10FFFF, and *Unicode code unit* is used for 16-bit `char` values that are code units of the *UTF-16* encoding. For more information on Unicode terminology, refer to the [Unicode Glossary](http://www.unicode.org/glossary/).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/java/lang/Character.Subset` Instances of this class represent particular subsets of the Unicode character set. |
| | `https://developer.android.com/reference/kotlin/java/lang/Character.UnicodeBlock` A family of character subsets representing the character blocks in the Unicode specification. |
| | `https://developer.android.com/reference/kotlin/java/lang/Character.UnicodeScript` A family of character subsets representing the character scripts defined in the [*Unicode Standard Annex #24: Script Names*](http://www.unicode.org/reports/tr24/). |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#BYTES:kotlin.Int` The number of bytes used to represent a `char` value in unsigned binary form. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#COMBINING_SPACING_MARK:kotlin.Byte` General category "Mc" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#CONNECTOR_PUNCTUATION:kotlin.Byte` General category "Pc" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#CONTROL:kotlin.Byte` General category "Cc" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#CURRENCY_SYMBOL:kotlin.Byte` General category "Sc" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DASH_PUNCTUATION:kotlin.Byte` General category "Pd" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DECIMAL_DIGIT_NUMBER:kotlin.Byte` General category "Nd" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_ARABIC_NUMBER:kotlin.Byte` Weak bidirectional character type "AN" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_BOUNDARY_NEUTRAL:kotlin.Byte` Weak bidirectional character type "BN" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_COMMON_NUMBER_SEPARATOR:kotlin.Byte` Weak bidirectional character type "CS" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER:kotlin.Byte` Weak bidirectional character type "EN" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR:kotlin.Byte` Weak bidirectional character type "ES" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR:kotlin.Byte` Weak bidirectional character type "ET" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_FIRST_STRONG_ISOLATE:kotlin.Byte` Weak bidirectional character type "FSI" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT:kotlin.Byte` Strong bidirectional character type "L" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING:kotlin.Byte` Strong bidirectional character type "LRE" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_ISOLATE:kotlin.Byte` Weak bidirectional character type "LRI" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE:kotlin.Byte` Strong bidirectional character type "LRO" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_NONSPACING_MARK:kotlin.Byte` Weak bidirectional character type "NSM" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_OTHER_NEUTRALS:kotlin.Byte` Neutral bidirectional character type "ON" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_PARAGRAPH_SEPARATOR:kotlin.Byte` Neutral bidirectional character type "B" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_FORMAT:kotlin.Byte` Weak bidirectional character type "PDF" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_ISOLATE:kotlin.Byte` Weak bidirectional character type "PDI" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT:kotlin.Byte` Strong bidirectional character type "R" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC:kotlin.Byte` Strong bidirectional character type "AL" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING:kotlin.Byte` Strong bidirectional character type "RLE" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ISOLATE:kotlin.Byte` Weak bidirectional character type "RLI" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE:kotlin.Byte` Strong bidirectional character type "RLO" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_SEGMENT_SEPARATOR:kotlin.Byte` Neutral bidirectional character type "S" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_UNDEFINED:kotlin.Byte` Undefined bidirectional character type. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_WHITESPACE:kotlin.Byte` Neutral bidirectional character type "WS" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#ENCLOSING_MARK:kotlin.Byte` General category "Me" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#END_PUNCTUATION:kotlin.Byte` General category "Pe" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#FINAL_QUOTE_PUNCTUATION:kotlin.Byte` General category "Pf" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#FORMAT:kotlin.Byte` General category "Cf" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#INITIAL_QUOTE_PUNCTUATION:kotlin.Byte` General category "Pi" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#LETTER_NUMBER:kotlin.Byte` General category "Nl" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#LINE_SEPARATOR:kotlin.Byte` General category "Zl" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#LOWERCASE_LETTER:kotlin.Byte` General category "Ll" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MATH_SYMBOL:kotlin.Byte` General category "Sm" in the Unicode specification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_CODE_POINT:kotlin.Int` The maximum value of a [Unicode code point](http://www.unicode.org/glossary/#code_point), constant `U+10FFFF`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_HIGH_SURROGATE:kotlin.Char` The maximum value of a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDBFF'`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_LOW_SURROGATE:kotlin.Char` The maximum value of a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDFFF'`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_RADIX:kotlin.Int` The maximum radix available for conversion to and from strings. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_SURROGATE:kotlin.Char` The maximum value of a Unicode surrogate code unit in the UTF-16 encoding, constant `'\u005CuDFFF'`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_VALUE:kotlin.Char` The constant value of this field is the largest value of type `char`, `'\u005CuFFFF'`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_CODE_POINT:kotlin.Int` The minimum value of a [Unicode code point](http://www.unicode.org/glossary/#code_point), constant `U+0000`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_HIGH_SURROGATE:kotlin.Char` The minimum value of a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuD800'`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_LOW_SURROGATE:kotlin.Char` The minimum value of a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDC00'`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_RADIX:kotlin.Int` The minimum radix available for conversion to and from strings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_SUPPLEMENTARY_CODE_POINT:kotlin.Int` The minimum value of a [Unicode supplementary code point](http://www.unicode.org/glossary/#supplementary_code_point), constant `U+10000`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_SURROGATE:kotlin.Char` The minimum value of a Unicode surrogate code unit in the UTF-16 encoding, constant `'\u005CuD800'`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_VALUE:kotlin.Char` The constant value of this field is the smallest value of type `char`, `'\u005Cu0000'`. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_LETTER:kotlin.Byte` General category "Lm" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_SYMBOL:kotlin.Byte` General category "Sk" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#NON_SPACING_MARK:kotlin.Byte` General category "Mn" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_LETTER:kotlin.Byte` General category "Lo" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_NUMBER:kotlin.Byte` General category "No" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_PUNCTUATION:kotlin.Byte` General category "Po" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_SYMBOL:kotlin.Byte` General category "So" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#PARAGRAPH_SEPARATOR:kotlin.Byte` General category "Zp" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#PRIVATE_USE:kotlin.Byte` General category "Co" in the Unicode specification. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#SIZE:kotlin.Int` The number of bits used to represent a `char` value in unsigned binary form, constant `16`. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#SPACE_SEPARATOR:kotlin.Byte` General category "Zs" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#START_PUNCTUATION:kotlin.Byte` General category "Ps" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#SURROGATE:kotlin.Byte` General category "Cs" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#TITLECASE_LETTER:kotlin.Byte` General category "Lt" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#UNASSIGNED:kotlin.Byte` General category "Cn" in the Unicode specification. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#UPPERCASE_LETTER:kotlin.Byte` General category "Lu" in the Unicode specification. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Character#Character(kotlin.Char)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Constructs a newly allocated `Character` object that represents the specified `char` value. |

| Public methods ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#charCount(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines the number of `char` values needed to represent the specified character (Unicode code point). |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#charValue()()` Returns the value of this `Character` object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointAt(kotlin.CharArray,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point at the given index of the `char` array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointAt(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point at the given index of the `char` array, where only array elements with `index` less than `limit` can be used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointAt(kotlin.CharSequence,%20kotlin.Int)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point at the given index of the `CharSequence`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointBefore(kotlin.CharArray,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point preceding the given index of the `char` array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointBefore(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point preceding the given index of the `char` array, where only array elements with `index` greater than or equal to `start` can be used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointBefore(kotlin.CharSequence,%20kotlin.Int)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the code point preceding the given index of the `CharSequence`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointCount(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of Unicode code points in a subarray of the `char` array argument. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointCount(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of Unicode code points in the text range of the specified char sequence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#codePointOf(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the code point value of the Unicode character specified by the given character name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#compare(kotlin.Char,%20kotlin.Char)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Compares two `char` values numerically. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#compareTo(kotlin.Char)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Compares two `Character` objects numerically. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html, radix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the numeric value of the character `ch` in the specified radix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Int,%20kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, radix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the numeric value of the specified character (Unicode code point) in the specified radix. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this object against the specified object. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)(digit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, radix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines the character representation for a specific digit in the specified radix. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getDirectionality(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the Unicode directionality property for the given character. |
| static [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getDirectionality(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the Unicode directionality property for the given character (Unicode code point). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/lang/Character#getName(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the name of the specified character , or null if the code point is `https://developer.android.com/reference/kotlin/java/lang/Character#UNASSIGNED:kotlin.Byte`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getNumericValue(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the `int` value that the specified Unicode character represents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getNumericValue(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `int` value that the specified character (Unicode code point) represents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns a value indicating a character's general category. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a value indicating a character's general category. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#hashCode()()` Returns a hash code for this `Character`; equal to the result of invoking `charValue()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#hashCode(kotlin.Char)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns a hash code for a `char` value; compatible with `Character.hashCode()`. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#highSurrogate(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the leading surrogate (a [high surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit)) of the [surrogate pair](http://www.unicode.org/glossary/#surrogate_pair) representing the specified supplementary character (Unicode code point) in the UTF-16 encoding. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isAlphabetic(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is alphabetic. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isBmpCodePoint(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines whether the specified character (Unicode code point) is in the [Basic Multilingual Plane (BMP)](https://developer.android.com/reference/kotlin/java/lang/Character#BMP). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isDefined(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if a character is defined in Unicode. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isDefined(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if a character (Unicode code point) is defined in Unicode. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a digit. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a digit. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isEmoji(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an Emoji. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isEmojiComponent(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an Emoji Component. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isEmojiModifier(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an Emoji Modifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isEmojiModifierBase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an Emoji Modifier Base. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isEmojiPresentation(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) has the Emoji Presentation property by default. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isExtendedPictographic(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an Extended Pictographic. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isHighSurrogate(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the given `char` value is a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) (also known as *leading-surrogate code unit*). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isISOControl(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is an ISO control character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isISOControl(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the referenced character (Unicode code point) is an ISO control character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character should be regarded as an ignorable character in a Java identifier or a Unicode identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) should be regarded as an ignorable character in a Java identifier or a Unicode identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isIdeographic(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a CJKV (Chinese, Japanese, Korean and Vietnamese) ideograph, as defined by the Unicode Standard. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character may be part of a Java identifier as other than the first character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the character (Unicode code point) may be part of a Java identifier as other than the first character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is permissible as the first character in a Java identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the character (Unicode code point) is permissible as the first character in a Java identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetter(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is permissible as the first character in a Java identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetterOrDigit(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character may be part of a Java identifier as other than the first character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a letter. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a letter. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a letter or digit. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a letter or digit. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLowSurrogate(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the given `char` value is a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) (also known as *trailing-surrogate code unit*). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a lowercase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a lowercase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isMirrored(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines whether the character is mirrored according to the Unicode specification. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isMirrored(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines whether the specified character (Unicode code point) is mirrored according to the Unicode specification. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSpace(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is ISO-LATIN-1 white space. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a Unicode space character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a Unicode space character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSupplementaryCodePoint(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines whether the specified character (Unicode code point) is in the [supplementary character](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary) range. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSurrogate(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the given `char` value is a Unicode *surrogate code unit*. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isSurrogatePair(kotlin.Char,%20kotlin.Char)(high: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html, low: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines whether the specified pair of `char` values is a valid [Unicode surrogate pair](http://www.unicode.org/glossary/#surrogate_pair). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is a titlecase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is a titlecase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character may be part of a Unicode identifier as other than the first character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) may be part of a Unicode identifier as other than the first character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is permissible as the first character in a Unicode identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is permissible as the first character in a Unicode identifier. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is an uppercase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is an uppercase character. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines whether the specified code point is a valid [Unicode code point value](http://www.unicode.org/glossary/#code_point). |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Determines if the specified character is white space according to Java. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Determines if the specified character (Unicode code point) is white space according to Java. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#lowSurrogate(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the trailing surrogate (a [low surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit)) of the [surrogate pair](http://www.unicode.org/glossary/#surrogate_pair) representing the specified supplementary character (Unicode code point) in the UTF-16 encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#offsetByCodePoints(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, codePointOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within the given `char` subarray that is offset from the given `index` by `codePointOffset` code points. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#offsetByCodePoints(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int)(seq: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, codePointOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within the given char sequence that is offset from the given `index` by `codePointOffset` code points. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#reverseBytes(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the value obtained by reversing the order of the bytes in the specified `char` value. |
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/Character#toChars(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the specified character (Unicode code point) to its UTF-16 representation stored in a `char` array. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toChars(kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, dstIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the specified character (Unicode code point) to its UTF-16 representation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toCodePoint(kotlin.Char,%20kotlin.Char)(high: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html, low: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Converts the specified surrogate pair to its supplementary code point value. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Converts the character argument to lowercase using case mapping information from the UnicodeData file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the character (Unicode code point) argument to lowercase using case mapping information from the UnicodeData file. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toString()()` Returns a `String` object representing this `Character`'s value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toString(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns a `String` object representing the specified `char`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toString(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a `String` object representing the specified character (Unicode code point). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toTitleCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Converts the character argument to titlecase using case mapping information from the UnicodeData file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toTitleCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the character (Unicode code point) argument to titlecase using case mapping information from the UnicodeData file. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Char)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Converts the character argument to uppercase using case mapping information from the UnicodeData file. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Int)(codePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Converts the character (Unicode code point) argument to uppercase using case mapping information from the UnicodeData file. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/Character#valueOf(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns a `Character` instance representing the specified `char` value. |

| Properties ||
|---|---|
| static [Class](https://developer.android.com/reference/kotlin/java/lang/Class)\< [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/lang/Character#TYPE:java.lang.Class` The `Class` instance representing the primitive type `char`. |

## Constants

### BYTES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BYTES: Int
```

The number of bytes used to represent a `char` value in unsigned binary form.

 Value: 2

### COMBINING_SPACING_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMBINING_SPACING_MARK: Byte
```

General category "Mc" in the Unicode specification.

 Value: 8

### CONNECTOR_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTOR_PUNCTUATION: Byte
```

General category "Pc" in the Unicode specification.

 Value: 23

### CONTROL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONTROL: Byte
```

General category "Cc" in the Unicode specification.

 Value: 15

### CURRENCY_SYMBOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CURRENCY_SYMBOL: Byte
```

General category "Sc" in the Unicode specification.

 Value: 26

### DASH_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DASH_PUNCTUATION: Byte
```

General category "Pd" in the Unicode specification.

 Value: 20

### DECIMAL_DIGIT_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DECIMAL_DIGIT_NUMBER: Byte
```

General category "Nd" in the Unicode specification.

 Value: 9

### DIRECTIONALITY_ARABIC_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_ARABIC_NUMBER: Byte
```

Weak bidirectional character type "AN" in the Unicode specification.

 Value: 6

### DIRECTIONALITY_BOUNDARY_NEUTRAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_BOUNDARY_NEUTRAL: Byte
```

Weak bidirectional character type "BN" in the Unicode specification.

 Value: 9

### DIRECTIONALITY_COMMON_NUMBER_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_COMMON_NUMBER_SEPARATOR: Byte
```

Weak bidirectional character type "CS" in the Unicode specification.

 Value: 7

### DIRECTIONALITY_EUROPEAN_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_EUROPEAN_NUMBER: Byte
```

Weak bidirectional character type "EN" in the Unicode specification.

 Value: 3

### DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR: Byte
```

Weak bidirectional character type "ES" in the Unicode specification.

 Value: 4

### DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR: Byte
```

Weak bidirectional character type "ET" in the Unicode specification.

 Value: 5

### DIRECTIONALITY_FIRST_STRONG_ISOLATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_FIRST_STRONG_ISOLATE: Byte
```

Weak bidirectional character type "FSI" in the Unicode specification.

 Value: 21

### DIRECTIONALITY_LEFT_TO_RIGHT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_LEFT_TO_RIGHT: Byte
```

Strong bidirectional character type "L" in the Unicode specification.

 Value: 0

### DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING: Byte
```

Strong bidirectional character type "LRE" in the Unicode specification.

 Value: 14

### DIRECTIONALITY_LEFT_TO_RIGHT_ISOLATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_LEFT_TO_RIGHT_ISOLATE: Byte
```

Weak bidirectional character type "LRI" in the Unicode specification.

 Value: 19

### DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE: Byte
```

Strong bidirectional character type "LRO" in the Unicode specification.

 Value: 15

### DIRECTIONALITY_NONSPACING_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_NONSPACING_MARK: Byte
```

Weak bidirectional character type "NSM" in the Unicode specification.

 Value: 8

### DIRECTIONALITY_OTHER_NEUTRALS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_OTHER_NEUTRALS: Byte
```

Neutral bidirectional character type "ON" in the Unicode specification.

 Value: 13

### DIRECTIONALITY_PARAGRAPH_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_PARAGRAPH_SEPARATOR: Byte
```

Neutral bidirectional character type "B" in the Unicode specification.

 Value: 10

### DIRECTIONALITY_POP_DIRECTIONAL_FORMAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_POP_DIRECTIONAL_FORMAT: Byte
```

Weak bidirectional character type "PDF" in the Unicode specification.

 Value: 18

### DIRECTIONALITY_POP_DIRECTIONAL_ISOLATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_POP_DIRECTIONAL_ISOLATE: Byte
```

Weak bidirectional character type "PDI" in the Unicode specification.

 Value: 22

### DIRECTIONALITY_RIGHT_TO_LEFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_RIGHT_TO_LEFT: Byte
```

Strong bidirectional character type "R" in the Unicode specification.

 Value: 1

### DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC: Byte
```

Strong bidirectional character type "AL" in the Unicode specification.

 Value: 2

### DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING: Byte
```

Strong bidirectional character type "RLE" in the Unicode specification.

 Value: 16

### DIRECTIONALITY_RIGHT_TO_LEFT_ISOLATE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_RIGHT_TO_LEFT_ISOLATE: Byte
```

Weak bidirectional character type "RLI" in the Unicode specification.

 Value: 20

### DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE: Byte
```

Strong bidirectional character type "RLO" in the Unicode specification.

 Value: 17

### DIRECTIONALITY_SEGMENT_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_SEGMENT_SEPARATOR: Byte
```

Neutral bidirectional character type "S" in the Unicode specification.

 Value: 11

### DIRECTIONALITY_UNDEFINED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_UNDEFINED: Byte
```

Undefined bidirectional character type. Undefined `char` values have undefined directionality in the Unicode specification.

 Value: -1

### DIRECTIONALITY_WHITESPACE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTIONALITY_WHITESPACE: Byte
```

Neutral bidirectional character type "WS" in the Unicode specification.

 Value: 12

### ENCLOSING_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCLOSING_MARK: Byte
```

General category "Me" in the Unicode specification.

 Value: 7

### END_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val END_PUNCTUATION: Byte
```

General category "Pe" in the Unicode specification.

 Value: 22

### FINAL_QUOTE_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FINAL_QUOTE_PUNCTUATION: Byte
```

General category "Pf" in the Unicode specification.

 Value: 30

### FORMAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FORMAT: Byte
```

General category "Cf" in the Unicode specification.

 Value: 16

### INITIAL_QUOTE_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INITIAL_QUOTE_PUNCTUATION: Byte
```

General category "Pi" in the Unicode specification.

 Value: 29

### LETTER_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LETTER_NUMBER: Byte
```

General category "Nl" in the Unicode specification.

 Value: 10

### LINE_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LINE_SEPARATOR: Byte
```

General category "Zl" in the Unicode specification.

 Value: 13

### LOWERCASE_LETTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOWERCASE_LETTER: Byte
```

General category "Ll" in the Unicode specification.

 Value: 2

### MATH_SYMBOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MATH_SYMBOL: Byte
```

General category "Sm" in the Unicode specification.

 Value: 25

### MAX_CODE_POINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_CODE_POINT: Int
```

The maximum value of a [Unicode code point](http://www.unicode.org/glossary/#code_point), constant `U+10FFFF`.

 Value: 1114111

### MAX_HIGH_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_HIGH_SURROGATE: Char
```

The maximum value of a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDBFF'`. A high-surrogate is also known as a *leading-surrogate*.

 Value: '\udbff'

### MAX_LOW_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_LOW_SURROGATE: Char
```

The maximum value of a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDFFF'`. A low-surrogate is also known as a *trailing-surrogate*.

 Value: '\udfff'

### MAX_RADIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_RADIX: Int
```

The maximum radix available for conversion to and from strings. The constant value of this field is the largest value permitted for the radix argument in radix-conversion methods such as the `digit` method, the `forDigit` method, and the `toString` method of class `Integer`.

 Value: 36

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#valueOf(kotlin.String)`

### MAX_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_SURROGATE: Char
```

The maximum value of a Unicode surrogate code unit in the UTF-16 encoding, constant `'\u005CuDFFF'`.

 Value: '\udfff'

### MAX_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_VALUE: Char
```

The constant value of this field is the largest value of type `char`, `'\u005CuFFFF'`.

 Value: '\uffff'

### MIN_CODE_POINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_CODE_POINT: Int
```

The minimum value of a [Unicode code point](http://www.unicode.org/glossary/#code_point), constant `U+0000`.

 Value: 0

### MIN_HIGH_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_HIGH_SURROGATE: Char
```

The minimum value of a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuD800'`. A high-surrogate is also known as a *leading-surrogate*.

 Value: '\ud800'

### MIN_LOW_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_LOW_SURROGATE: Char
```

The minimum value of a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) in the UTF-16 encoding, constant `'\u005CuDC00'`. A low-surrogate is also known as a *trailing-surrogate*.

 Value: '\udc00'

### MIN_RADIX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_RADIX: Int
```

The minimum radix available for conversion to and from strings. The constant value of this field is the smallest value permitted for the radix argument in radix-conversion methods such as the `digit` method, the `forDigit` method, and the `toString` method of class `Integer`.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Integer#valueOf(kotlin.String)`

### MIN_SUPPLEMENTARY_CODE_POINT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_SUPPLEMENTARY_CODE_POINT: Int
```

The minimum value of a [Unicode supplementary code point](http://www.unicode.org/glossary/#supplementary_code_point), constant `U+10000`.

 Value: 65536

### MIN_SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_SURROGATE: Char
```

The minimum value of a Unicode surrogate code unit in the UTF-16 encoding, constant `'\u005CuD800'`.

 Value: '\ud800'

### MIN_VALUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_VALUE: Char
```

The constant value of this field is the smallest value of type `char`, `'\u005Cu0000'`.

 Value: '\u0000'

### MODIFIER_LETTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODIFIER_LETTER: Byte
```

General category "Lm" in the Unicode specification.

 Value: 4

### MODIFIER_SYMBOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MODIFIER_SYMBOL: Byte
```

General category "Sk" in the Unicode specification.

 Value: 27

### NON_SPACING_MARK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NON_SPACING_MARK: Byte
```

General category "Mn" in the Unicode specification.

 Value: 6

### OTHER_LETTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTHER_LETTER: Byte
```

General category "Lo" in the Unicode specification.

 Value: 5

### OTHER_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTHER_NUMBER: Byte
```

General category "No" in the Unicode specification.

 Value: 11

### OTHER_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTHER_PUNCTUATION: Byte
```

General category "Po" in the Unicode specification.

 Value: 24

### OTHER_SYMBOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTHER_SYMBOL: Byte
```

General category "So" in the Unicode specification.

 Value: 28

### PARAGRAPH_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAGRAPH_SEPARATOR: Byte
```

General category "Zp" in the Unicode specification.

 Value: 14

### PRIVATE_USE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIVATE_USE: Byte
```

General category "Co" in the Unicode specification.

 Value: 18

### SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIZE: Int
```

The number of bits used to represent a `char` value in unsigned binary form, constant `16`.

 Value: 16

### SPACE_SEPARATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SPACE_SEPARATOR: Byte
```

General category "Zs" in the Unicode specification.

 Value: 12

### START_PUNCTUATION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val START_PUNCTUATION: Byte
```

General category "Ps" in the Unicode specification.

 Value: 21

### SURROGATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SURROGATE: Byte
```

General category "Cs" in the Unicode specification.

 Value: 19

### TITLECASE_LETTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TITLECASE_LETTER: Byte
```

General category "Lt" in the Unicode specification.

 Value: 3

### UNASSIGNED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNASSIGNED: Byte
```

General category "Cn" in the Unicode specification.

 Value: 0

### UPPERCASE_LETTER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UPPERCASE_LETTER: Byte
```

General category "Lu" in the Unicode specification.

 Value: 1

## Public constructors

### Character

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Character(value: Char)
```

**Deprecated:** *It is rarely appropriate to use this constructor. The static factory `https://developer.android.com/reference/kotlin/java/lang/Character#valueOf(kotlin.Char)` is generally a better choice, as it is likely to yield significantly better space and time performance.*

Constructs a newly allocated `Character` object that represents the specified `char` value.

| Parameters ||
|---|---|
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the value to be represented by the `Character` object. |

## Public methods

### charCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun charCount(codePoint: Int): Int
```

Determines the number of `char` values needed to represent the specified character (Unicode code point). If the specified character is equal to or greater than 0x10000, then the method returns 2. Otherwise, the method returns 1.

This method doesn't validate the specified character to be a valid Unicode code point. The caller must validate the character value using `https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int)` if necessary.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 2 if the character is a valid supplementary character; 1 otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSupplementaryCodePoint(kotlin.Int)`

### charValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun charValue(): Char
```

Returns the value of this `Character` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the primitive `char` value represented by this object. |

### codePointAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointAt(
    a: CharArray!, 
    index: Int
): Int
```

Returns the code point at the given index of the `char` array. If the `char` value at the given index in the `char` array is in the high-surrogate range, the following index is less than the length of the `char` array, and the `char` value at the following index is in the low-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at the given index is returned.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the `char` values (Unicode code units) in the `char` array to be converted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the value `index` is negative or not less than the length of the `char` array. |
| `java.lang.NullPointerException` | if `a` is null. |

### codePointAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointAt(
    a: CharArray!, 
    index: Int, 
    limit: Int
): Int
```

Returns the code point at the given index of the `char` array, where only array elements with `index` less than `limit` can be used. If the `char` value at the given index in the `char` array is in the high-surrogate range, the following index is less than the `limit`, and the `char` value at the following index is in the low-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at the given index is returned.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the `char` values (Unicode code units) in the `char` array to be converted |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index after the last array element that can be used in the `char` array |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than the `limit` argument, or if the `limit` argument is negative or greater than the length of the `char` array. |
| `java.lang.NullPointerException` | if `a` is null. |

### codePointAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointAt(
    seq: CharSequence, 
    index: Int
): Int
```

Returns the code point at the given index of the `CharSequence`. If the `char` value at the given index in the `CharSequence` is in the high-surrogate range, the following index is less than the length of the `CharSequence`, and the `char` value at the following index is in the low-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at the given index is returned.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): a sequence of `char` values (Unicode code units) |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the `char` values (Unicode code units) in `seq` to be converted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point at the given index |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the value `index` is negative or not less than `https://developer.android.com/reference/kotlin/java/lang/CharSequence#length()`. |
| `java.lang.NullPointerException` | if `seq` is null. |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointBefore(
    a: CharArray!, 
    index: Int
): Int
```

Returns the code point preceding the given index of the `char` array. If the `char` value at `(index - 1)` in the `char` array is in the low-surrogate range, `(index - 2)` is not negative, and the `char` value at `(index - 2)` in the `char` array is in the high-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at `(index - 1)` is returned.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index following the code point that should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point value before the given index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is less than 1 or greater than the length of the `char` array |
| `java.lang.NullPointerException` | if `a` is null. |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointBefore(
    a: CharArray!, 
    index: Int, 
    start: Int
): Int
```

Returns the code point preceding the given index of the `char` array, where only array elements with `index` greater than or equal to `start` can be used. If the `char` value at `(index - 1)` in the `char` array is in the low-surrogate range, `(index - 2)` is not less than `start`, and the `char` value at `(index - 2)` in the `char` array is in the high-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at `(index - 1)` is returned.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index following the code point that should be returned |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first array element in the `char` array |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point value before the given index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is not greater than the `start` argument or is greater than the length of the `char` array, or if the `start` argument is negative or not less than the length of the `char` array. |
| `java.lang.NullPointerException` | if `a` is null. |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointBefore(
    seq: CharSequence, 
    index: Int
): Int
```

Returns the code point preceding the given index of the `CharSequence`. If the `char` value at `(index - 1)` in the `CharSequence` is in the low-surrogate range, `(index - 2)` is not negative, and the `char` value at `(index - 2)` in the `CharSequence` is in the high-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at `(index - 1)` is returned.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the `CharSequence` instance |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index following the code point that should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point value before the given index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is less than 1 or greater than `https://developer.android.com/reference/kotlin/java/lang/CharSequence#length()`. |
| `java.lang.NullPointerException` | if `seq` is null. |

### codePointCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointCount(
    a: CharArray!, 
    offset: Int, 
    count: Int
): Int
```

Returns the number of Unicode code points in a subarray of the `char` array argument. The `offset` argument is the index of the first `char` of the subarray and the `count` argument specifies the length of the subarray in `char`s. Unpaired surrogates within the subarray count as one code point each.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first `char` in the given `char` array |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the subarray in `char`s |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of Unicode code points in the specified subarray |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `offset` or `count` is negative, or if `offset + count` is larger than the length of the given array. |
| `java.lang.NullPointerException` | if `a` is null. |

### codePointCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointCount(
    seq: CharSequence, 
    beginIndex: Int, 
    endIndex: Int
): Int
```

Returns the number of Unicode code points in the text range of the specified char sequence. The text range begins at the specified `beginIndex` and extends to the `char` at index `endIndex - 1`. Thus the length (in `char`s) of the text range is `endIndex-beginIndex`. Unpaired surrogates within the text range count as one code point each.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the char sequence |
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the first `char` of the text range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index after the last `char` of the text range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of Unicode code points in the specified text range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `beginIndex` is negative, or `endIndex` is larger than the length of the given sequence, or `beginIndex` is larger than `endIndex`. |
| `java.lang.NullPointerException` | if `seq` is null. |

### codePointOf

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun codePointOf(name: String): Int
```

Returns the code point value of the Unicode character specified by the given character name.

If a character is not assigned a name by the *UnicodeData* file (part of the Unicode Character Database maintained by the Unicode Consortium), its name is defined as the result of the expression:
`Character.UnicodeBlock.of(codePoint).toString().replace('_', ' ') + " " + Integer.toHexString(codePoint).toUpperCase(Locale.ROOT); `

The `name` matching is case insensitive, with any leading and trailing whitespace character removed. For the code points in the *UnicodeData* file, this method recognizes the name which conforms to the name defined in the "Unicode Name Property" section in the Unicode Standard. For other code points, this method recognizes the name generated with `https://developer.android.com/reference/kotlin/java/lang/Character#getName(kotlin.Int)` method.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the character name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the code point value of the character specified by its name. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `name` is not a valid character name. |
| `java.lang.NullPointerException` | if `name` is `null` |

### compare

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun compare(
    x: Char, 
    y: Char
): Int
```

Compares two `char` values numerically. The value returned is identical to what would be returned by:

```kotlin
Character.valueOf(x).compareTo(Character.valueOf(y))
  
```

<br />

| Parameters ||
|---|---|
| `x` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the first `char` to compare |
| `y` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the second `char` to compare |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if `x == y`; a value less than `0` if `x < y`; and a value greater than `0` if `x > y` |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Char): Int
```

Compares two `Character` objects numerically.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `anotherCharacter` | the `Character` to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the argument `Character` is equal to this `Character`; a value less than `0` if this `Character` is numerically less than the `Character` argument; and a value greater than `0` if this `Character` is numerically greater than the `Character` argument (unsigned comparison). Note that this is strictly a numerical comparison; it is not locale-dependent. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### digit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun digit(
    ch: Char, 
    radix: Int
): Int
```

Returns the numeric value of the character `ch` in the specified radix.

If the radix is not in the range `MIN_RADIX` ≤ `radix` ≤ `MAX_RADIX` or if the value of `ch` is not a valid digit in the specified radix, `-1` is returned. A character is a valid digit if at least one of the following is true:

- The method `isDigit` is `true` of the character and the Unicode decimal digit value of the character (or its single-character decomposition) is less than the specified radix. In this case the decimal digit value is returned.
- The character is one of the uppercase Latin letters `'A'` through `'Z'` and its code is less than `radix + 'A' - 10`. In this case, `ch - 'A' + 10` is returned.
- The character is one of the lowercase Latin letters `'a'` through `'z'` and its code is less than `radix + 'a' - 10`. In this case, `ch - 'a' + 10` is returned.
- The character is one of the fullwidth uppercase Latin letters A (`'\u005CuFF21'`) through Z (`'\u005CuFF3A'`) and its code is less than `radix + '\u005CuFF21' - 10`. In this case, `ch - '\u005CuFF21' + 10` is returned.
- The character is one of the fullwidth lowercase Latin letters a (`'\u005CuFF41'`) through z (`'\u005CuFF5A'`) and its code is less than `radix + '\u005CuFF41' - 10`. In this case, `ch - '\u005CuFF41' + 10` is returned.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Int,%20kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be converted. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value represented by the character in the specified radix. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)`

### digit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun digit(
    codePoint: Int, 
    radix: Int
): Int
```

Returns the numeric value of the specified character (Unicode code point) in the specified radix.

If the radix is not in the range `MIN_RADIX` ≤ `radix` ≤ `MAX_RADIX` or if the character is not a valid digit in the specified radix, `-1` is returned. A character is a valid digit if at least one of the following is true:

- The method `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)` is `true` of the character and the Unicode decimal digit value of the character (or its single-character decomposition) is less than the specified radix. In this case the decimal digit value is returned.
- The character is one of the uppercase Latin letters `'A'` through `'Z'` and its code is less than `radix + 'A' - 10`. In this case, `codePoint - 'A' + 10` is returned.
- The character is one of the lowercase Latin letters `'a'` through `'z'` and its code is less than `radix + 'a' - 10`. In this case, `codePoint - 'a' + 10` is returned.
- The character is one of the fullwidth uppercase Latin letters A (`'\u005CuFF21'`) through Z (`'\u005CuFF3A'`) and its code is less than `radix + '\u005CuFF21' - 10`. In this case, `codePoint - '\u005CuFF21' + 10` is returned.
- The character is one of the fullwidth lowercase Latin letters a (`'\u005CuFF41'`) through z (`'\u005CuFF5A'`) and its code is less than `radix + '\u005CuFF41'- 10`. In this case, `codePoint - '\u005CuFF41' + 10` is returned.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value represented by the character in the specified radix. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)`

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is `true` if and only if the argument is not `null` and is a `Character` object that represents the same `char` value as this object.

| Parameters ||
|---|---|
| `obj` | the object to compare with. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the objects are the same; `false` otherwise. |

### forDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forDigit(
    digit: Int, 
    radix: Int
): Char
```

Determines the character representation for a specific digit in the specified radix. If the value of `radix` is not a valid radix, or the value of `digit` is not a valid digit in the specified radix, the null character (`'\u005Cu0000'`) is returned.

The `radix` argument is valid if it is greater than or equal to `MIN_RADIX` and less than or equal to `MAX_RADIX`. The `digit` argument is valid if `0 <= digit < radix`.

If the digit is less than 10, then `'0' + digit` is returned. Otherwise, the value `'a' + digit - 10` is returned.

| Parameters ||
|---|---|
| `digit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number to convert to a character. |
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the `char` representation of the specified digit in the specified radix. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_RADIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_RADIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int)`

### getDirectionality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDirectionality(ch: Char): Byte
```

Returns the Unicode directionality property for the given character. Character directionality is used to calculate the visual ordering of text. The directionality value of undefined `char` values is `DIRECTIONALITY_UNDEFINED`.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#getDirectionality(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): `char` for which the directionality property is requested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the directionality property of the `char` value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_UNDEFINED:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_ARABIC_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_COMMON_NUMBER_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_NONSPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_BOUNDARY_NEUTRAL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_PARAGRAPH_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_SEGMENT_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_WHITESPACE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_OTHER_NEUTRALS:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_FORMAT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_FIRST_STRONG_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_ISOLATE:kotlin.Byte`

### getDirectionality

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDirectionality(codePoint: Int): Byte
```

Returns the Unicode directionality property for the given character (Unicode code point). Character directionality is used to calculate the visual ordering of text. The directionality value of undefined character is `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_UNDEFINED:kotlin.Byte`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) for which the directionality property is requested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the directionality property of the character. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_UNDEFINED:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ARABIC:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_EUROPEAN_NUMBER_TERMINATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_ARABIC_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_COMMON_NUMBER_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_NONSPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_BOUNDARY_NEUTRAL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_PARAGRAPH_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_SEGMENT_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_WHITESPACE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_OTHER_NEUTRALS:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_EMBEDDING:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_OVERRIDE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_EMBEDDING:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_OVERRIDE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_FORMAT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_LEFT_TO_RIGHT_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_RIGHT_TO_LEFT_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_FIRST_STRONG_ISOLATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DIRECTIONALITY_POP_DIRECTIONAL_ISOLATE:kotlin.Byte`

### getName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getName(codePoint: Int): String?
```

Returns the name of the specified character , or null if the code point is `https://developer.android.com/reference/kotlin/java/lang/Character#UNASSIGNED:kotlin.Byte`.

If the specified character is not assigned a name by the *UnicodeData* file (part of the Unicode Character Database maintained by the Unicode Consortium), the returned name is the same as the result of the expression:
`Character.UnicodeBlock.of(codePoint).toString().replace('_', ' ') + " " + Integer.toHexString(codePoint).toUpperCase(Locale.ROOT); ` For the `codePoint`s in the *UnicodeData* file, the name returned by this method follows the naming scheme in the "Unicode Name Property" section of the Unicode Standard. For other code points, such as Hangul/Ideographs, The name generation rule above differs from the one defined in the Unicode Standard.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the name of the specified character, or null if the code point is unassigned. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `codePoint` is not a valid Unicode code point. |

### getNumericValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getNumericValue(ch: Char): Int
```

Returns the `int` value that the specified Unicode character represents. For example, the character `'\u005Cu216C'` (the roman numeral fifty) will return an int with a value of 50.

The letters A-Z in their uppercase (`'\u005Cu0041'` through `'\u005Cu005A'`), lowercase (`'\u005Cu0061'` through `'\u005Cu007A'`), and full width variant (`'\u005CuFF21'` through `'\u005CuFF3A'` and `'\u005CuFF41'` through `'\u005CuFF5A'`) forms have numeric values from 10 through 35. This is independent of the Unicode specification, which does not assign numeric values to these `char` values.

If the character does not have a numeric value, then -1 is returned. If the character has a numeric value that cannot be represented as a nonnegative integer (for example, a fractional value), then -2 is returned.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#getNumericValue(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value of the character, as a nonnegative `int` value; -2 if the character has a numeric value but the value can not be represented as a nonnegative `int` value; -1 if the character has no numeric value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)`

### getNumericValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getNumericValue(codePoint: Int): Int
```

Returns the `int` value that the specified character (Unicode code point) represents. For example, the character `'\u005Cu216C'` (the Roman numeral fifty) will return an `int` with a value of 50.

The letters A-Z in their uppercase (`'\u005Cu0041'` through `'\u005Cu005A'`), lowercase (`'\u005Cu0061'` through `'\u005Cu007A'`), and full width variant (`'\u005CuFF21'` through `'\u005CuFF3A'` and `'\u005CuFF41'` through `'\u005CuFF5A'`) forms have numeric values from 10 through 35. This is independent of the Unicode specification, which does not assign numeric values to these `char` values.

If the character does not have a numeric value, then -1 is returned. If the character has a numeric value that cannot be represented as a nonnegative integer (for example, a fractional value), then -2 is returned.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value of the character, as a nonnegative `int` value; -2 if the character has a numeric value but the value can not be represented as a nonnegative `int` value; -1 if the character has no numeric value. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)`

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getType(ch: Char): Int
```

Returns a value indicating a character's general category.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a value of type `int` representing the character's general category. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#COMBINING_SPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CONNECTOR_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CONTROL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CURRENCY_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DASH_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DECIMAL_DIGIT_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#ENCLOSING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#END_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#FINAL_QUOTE_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#FORMAT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#INITIAL_QUOTE_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LETTER_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LINE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LOWERCASE_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MATH_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#NON_SPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#PARAGRAPH_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#PRIVATE_USE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#SPACE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#START_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#SURROGATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#TITLECASE_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#UNASSIGNED:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#UPPERCASE_LETTER:kotlin.Byte`

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getType(codePoint: Int): Int
```

Returns a value indicating a character's general category.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a value of type `int` representing the character's general category. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#COMBINING_SPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CONNECTOR_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CONTROL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#CURRENCY_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DASH_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#DECIMAL_DIGIT_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#ENCLOSING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#END_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#FINAL_QUOTE_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#FORMAT:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#INITIAL_QUOTE_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LETTER_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LINE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LOWERCASE_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MATH_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#MODIFIER_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#NON_SPACING_MARK:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_NUMBER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#OTHER_SYMBOL:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#PARAGRAPH_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#PRIVATE_USE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#SPACE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#START_PUNCTUATION:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#SURROGATE:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#TITLECASE_LETTER:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#UNASSIGNED:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#UPPERCASE_LETTER:kotlin.Byte`

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this `Character`; equal to the result of invoking `charValue()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this `Character` |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun hashCode(value: Char): Int
```

Returns a hash code for a `char` value; compatible with `Character.hashCode()`.

| Parameters ||
|---|---|
| `value` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The `char` for which to return a hash code. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for a `char` value. |

### highSurrogate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun highSurrogate(codePoint: Int): Char
```

Returns the leading surrogate (a [high surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit)) of the [surrogate pair](http://www.unicode.org/glossary/#surrogate_pair) representing the specified supplementary character (Unicode code point) in the UTF-16 encoding. If the specified character is not a [supplementary character](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary), an unspecified `char` is returned.

If `https://developer.android.com/reference/kotlin/java/lang/Character#isSupplementaryCodePoint(kotlin.Int)` is `true`, then `https://developer.android.com/reference/kotlin/java/lang/Character#isHighSurrogate(kotlin.Char)``(highSurrogate(x))` and `https://developer.android.com/reference/kotlin/java/lang/Character#toCodePoint(kotlin.Char,%20kotlin.Char)``(highSurrogate(x), ``https://developer.android.com/reference/kotlin/java/lang/Character#lowSurrogate(kotlin.Int)``(x)) == x` are also always `true`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a supplementary character (Unicode code point) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the leading surrogate code unit used to represent the character in the UTF-16 encoding |

### isAlphabetic

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isAlphabetic(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is alphabetic.

A character is considered to be alphabetic if its general category type, provided by `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`, is any of the following:

- `UPPERCASE_LETTER`
- `LOWERCASE_LETTER`
- `TITLECASE_LETTER`
- `MODIFIER_LETTER`
- `OTHER_LETTER`
- `LETTER_NUMBER`

or it has contributory property Other_Alphabetic as defined by the Unicode Standard.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a Unicode alphabet character, `false` otherwise. |

### isBmpCodePoint

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isBmpCodePoint(codePoint: Int): Boolean
```

Determines whether the specified character (Unicode code point) is in the [Basic Multilingual Plane (BMP)](https://developer.android.com/reference/kotlin/java/lang/Character#BMP). Such code points can be represented using a single `char`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be to |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified code point is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_VALUE:kotlin.Char` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_VALUE:kotlin.Char` inclusive; `false` otherwise. |

### isDefined

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDefined(ch: Char): Boolean
```

Determines if a character is defined in Unicode.

A character is defined if at least one of the following is true:

- It has an entry in the UnicodeData file.
- It has a value in a range defined by the UnicodeData file.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isDefined(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character has a defined meaning in Unicode; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Char)`

### isDefined

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDefined(codePoint: Int): Boolean
```

Determines if a character (Unicode code point) is defined in Unicode.

A character is defined if at least one of the following is true:

- It has an entry in the UnicodeData file.
- It has a value in a range defined by the UnicodeData file.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character has a defined meaning in Unicode; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)`

### isDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDigit(ch: Char): Boolean
```

Determines if the specified character is a digit.

A character is a digit if its general category type, provided by `Character.getType(ch)`, is `DECIMAL_DIGIT_NUMBER`.

Some Unicode character ranges that contain digits:

- `'\u005Cu0030'` through `'\u005Cu0039'`, ISO-LATIN-1 digits (`'0'` through `'9'`)
- `'\u005Cu0660'` through `'\u005Cu0669'`, Arabic-Indic digits
- `'\u005Cu06F0'` through `'\u005Cu06F9'`, Extended Arabic-Indic digits
- `'\u005Cu0966'` through `'\u005Cu096F'`, Devanagari digits
- `'\u005CuFF10'` through `'\u005CuFF19'`, Fullwidth digits

Many other character ranges contain digits as well.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a digit; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#digit(kotlin.Char,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)`

### isDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isDigit(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a digit.

A character is a digit if its general category type, provided by `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`, is `DECIMAL_DIGIT_NUMBER`.

Some Unicode character ranges that contain digits:

- `'\u005Cu0030'` through `'\u005Cu0039'`, ISO-LATIN-1 digits (`'0'` through `'9'`)
- `'\u005Cu0660'` through `'\u005Cu0669'`, Arabic-Indic digits
- `'\u005Cu06F0'` through `'\u005Cu06F9'`, Extended Arabic-Indic digits
- `'\u005Cu0966'` through `'\u005Cu096F'`, Devanagari digits
- `'\u005CuFF10'` through `'\u005CuFF19'`, Fullwidth digits

Many other character ranges contain digits as well.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a digit; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#forDigit(kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`

### isEmoji

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isEmoji(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an Emoji.

A character is considered to be an Emoji if and only if it has the `Emoji` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an Emoji; `false` otherwise. |

### isEmojiComponent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isEmojiComponent(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an Emoji Component.

A character is considered to be an Emoji Component if and only if it has the `Emoji_Component` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an Emoji Component; `false` otherwise. |

### isEmojiModifier

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isEmojiModifier(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an Emoji Modifier.

A character is considered to be an Emoji Modifier if and only if it has the `Emoji_Modifier` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an Emoji Modifier; `false` otherwise. |

### isEmojiModifierBase

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isEmojiModifierBase(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an Emoji Modifier Base.

A character is considered to be an Emoji Modifier Base if and only if it has the `Emoji_Modifier_Base` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an Emoji Modifier Base; `false` otherwise. |

### isEmojiPresentation

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isEmojiPresentation(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) has the Emoji Presentation property by default.

A character is considered to have the Emoji Presentation property if and only if it has the `Emoji_Presentation` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character has the Emoji Presentation property; `false` otherwise. |

### isExtendedPictographic

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isExtendedPictographic(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an Extended Pictographic.

A character is considered to be an Extended Pictographic if and only if it has the `Extended_Pictographic` property, defined in [Unicode Emoji (Technical Standard #51)](https://unicode.org/reports/tr51/#Emoji_Properties_and_Data_Files).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an Extended Pictographic; `false` otherwise. |

### isHighSurrogate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isHighSurrogate(ch: Char): Boolean
```

Determines if the given `char` value is a [Unicode high-surrogate code unit](http://www.unicode.org/glossary/#high_surrogate_code_unit) (also known as *leading-surrogate code unit*).

Such values do not represent characters by themselves, but are used in the representation of [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary) in the UTF-16 encoding.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the `char` value to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `char` value is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_HIGH_SURROGATE:kotlin.Char` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_HIGH_SURROGATE:kotlin.Char` inclusive; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowSurrogate(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character.UnicodeBlock#of(kotlin.Int)`

### isISOControl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isISOControl(ch: Char): Boolean
```

Determines if the specified character is an ISO control character. A character is considered to be an ISO control character if its code is in the range `'\u005Cu0000'` through `'\u005Cu001F'` or in the range `'\u005Cu007F'` through `'\u005Cu009F'`.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isISOControl(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an ISO control character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Char)`

### isISOControl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isISOControl(codePoint: Int): Boolean
```

Determines if the referenced character (Unicode code point) is an ISO control character. A character is considered to be an ISO control character if its code is in the range `'\u005Cu0000'` through `'\u005Cu001F'` or in the range `'\u005Cu007F'` through `'\u005Cu009F'`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an ISO control character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### isIdentifierIgnorable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isIdentifierIgnorable(ch: Char): Boolean
```

Determines if the specified character should be regarded as an ignorable character in a Java identifier or a Unicode identifier.

The following Unicode characters are ignorable in a Java identifier or a Unicode identifier:

- ISO control characters that are not whitespace
 - `'\u005Cu0000'` through `'\u005Cu0008'`
 - `'\u005Cu000E'` through `'\u005Cu001B'`
 - `'\u005Cu007F'` through `'\u005Cu009F'`
- all characters that have the `FORMAT` general category value

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an ignorable control character that may be part of a Java or Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)`

### isIdentifierIgnorable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isIdentifierIgnorable(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) should be regarded as an ignorable character in a Java identifier or a Unicode identifier.

The following Unicode characters are ignorable in a Java identifier or a Unicode identifier:

- ISO control characters that are not whitespace
 - `'\u005Cu0000'` through `'\u005Cu0008'`
 - `'\u005Cu000E'` through `'\u005Cu001B'`
 - `'\u005Cu007F'` through `'\u005Cu009F'`
- all characters that have the `FORMAT` general category value

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is an ignorable control character that may be part of a Java or Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)`

### isIdeographic

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isIdeographic(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a CJKV (Chinese, Japanese, Korean and Vietnamese) ideograph, as defined by the Unicode Standard.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a Unicode ideograph character, `false` otherwise. |

### isJavaIdentifierPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaIdentifierPart(ch: Char): Boolean
```

Determines if the specified character may be part of a Java identifier as other than the first character.

A character may be part of a Java identifier if any of the following conditions are true:

- it is a letter
- it is a currency symbol (such as `'$'`)
- it is a connecting punctuation character (such as `'_'`)
- it is a digit
- it is a numeric letter (such as a Roman numeral character)
- it is a combining mark
- it is a non-spacing mark
- `isIdentifierIgnorable` returns `true` for the character

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may be part of a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)`

### isJavaIdentifierPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaIdentifierPart(codePoint: Int): Boolean
```

Determines if the character (Unicode code point) may be part of a Java identifier as other than the first character.

A character may be part of a Java identifier if any of the following conditions are true:

- it is a letter
- it is a currency symbol (such as `'$'`)
- it is a connecting punctuation character (such as `'_'`)
- it is a digit
- it is a numeric letter (such as a Roman numeral character)
- it is a combining mark
- it is a non-spacing mark
- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Int)` returns `true` for the code point

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may be part of a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)`

### isJavaIdentifierStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaIdentifierStart(ch: Char): Boolean
```

Determines if the specified character is permissible as the first character in a Java identifier.

A character may start a Java identifier if and only if one of the following conditions is true:

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)` returns `true`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)` returns `LETTER_NUMBER`
- `ch` is a currency symbol (such as `'$'`)
- `ch` is a connecting punctuation character (such as `'_'`).

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may start a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Char)`

### isJavaIdentifierStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaIdentifierStart(codePoint: Int): Boolean
```

Determines if the character (Unicode code point) is permissible as the first character in a Java identifier.

A character may start a Java identifier if and only if one of the following conditions is true:

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)` returns `true`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)` returns `LETTER_NUMBER`
- the referenced character is a currency symbol (such as `'$'`)
- the referenced character is a connecting punctuation character (such as `'_'`).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may start a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Int)`

### isJavaLetter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaLetter(ch: Char): Boolean
```

**Deprecated:** *Replaced by isJavaIdentifierStart(char).*

Determines if the specified character is permissible as the first character in a Java identifier.

A character may start a Java identifier if and only if one of the following conditions is true:

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)` returns `true`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)` returns `LETTER_NUMBER`
- `ch` is a currency symbol (such as `'$'`)
- `ch` is a connecting punctuation character (such as `'_'`).

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may start a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Char)`

### isJavaLetterOrDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isJavaLetterOrDigit(ch: Char): Boolean
```

**Deprecated:** *Replaced by isJavaIdentifierPart(char).*

Determines if the specified character may be part of a Java identifier as other than the first character.

A character may be part of a Java identifier if and only if one of the following conditions is true:

- it is a letter
- it is a currency symbol (such as `'$'`)
- it is a connecting punctuation character (such as `'_'`)
- it is a digit
- it is a numeric letter (such as a Roman numeral character)
- it is a combining mark
- it is a non-spacing mark
- `isIdentifierIgnorable` returns `true` for the character.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may be part of a Java identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Char)`

### isLetter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLetter(ch: Char): Boolean
```

Determines if the specified character is a letter.

A character is considered to be a letter if its general category type, provided by `Character.getType(ch)`, is any of the following:

- `UPPERCASE_LETTER`
- `LOWERCASE_LETTER`
- `TITLECASE_LETTER`
- `MODIFIER_LETTER`
- `OTHER_LETTER`

Not all letters have case. Many characters are letters but are neither uppercase nor lowercase nor titlecase.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a letter; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Char)`

### isLetter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLetter(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a letter.

A character is considered to be a letter if its general category type, provided by `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`, is any of the following:

- `UPPERCASE_LETTER`
- `LOWERCASE_LETTER`
- `TITLECASE_LETTER`
- `MODIFIER_LETTER`
- `OTHER_LETTER`

Not all letters have case. Many characters are letters but are neither uppercase nor lowercase nor titlecase.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a letter; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)`

### isLetterOrDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLetterOrDigit(ch: Char): Boolean
```

Determines if the specified character is a letter or digit.

A character is considered to be a letter or digit if either `Character.isLetter(char ch)` or `Character.isDigit(char ch)` returns `true` for the character.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a letter or digit; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)`

### isLetterOrDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLetterOrDigit(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a letter or digit.

A character is considered to be a letter or digit if either `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)` or `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)` returns `true` for the character.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a letter or digit; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)`

### isLowSurrogate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLowSurrogate(ch: Char): Boolean
```

Determines if the given `char` value is a [Unicode low-surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit) (also known as *trailing-surrogate code unit*).

Such values do not represent characters by themselves, but are used in the representation of [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary) in the UTF-16 encoding.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the `char` value to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `char` value is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_LOW_SURROGATE:kotlin.Char` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_LOW_SURROGATE:kotlin.Char` inclusive; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isHighSurrogate(kotlin.Char)`

### isLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLowerCase(ch: Char): Boolean
```

Determines if the specified character is a lowercase character.

A character is lowercase if its general category type, provided by `Character.getType(ch)`, is `LOWERCASE_LETTER`, or it has contributory property Other_Lowercase as defined by the Unicode Standard.

The following are examples of lowercase characters:

```kotlin
a b c d e f g h i j k l m n o p q r s t u v w x y z
  '\u00DF' '\u00E0' '\u00E1' '\u00E2' '\u00E3' '\u00E4' '\u00E5' '\u00E6'
  '\u00E7' '\u00E8' '\u00E9' '\u00EA' '\u00EB' '\u00EC' '\u00ED' '\u00EE'
  '\u00EF' '\u00F0' '\u00F1' '\u00F2' '\u00F3' '\u00F4' '\u00F5' '\u00F6'
  '\u00F8' '\u00F9' '\u00FA' '\u00FB' '\u00FC' '\u00FD' '\u00FE' '\u00FF'
  
```

Many other Unicode characters are lowercase too.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is lowercase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)`

### isLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isLowerCase(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a lowercase character.

A character is lowercase if its general category type, provided by #getType, is `LOWERCASE_LETTER`, or it has contributory property Other_Lowercase as defined by the Unicode Standard.

The following are examples of lowercase characters:

```kotlin
a b c d e f g h i j k l m n o p q r s t u v w x y z
  '\u00DF' '\u00E0' '\u00E1' '\u00E2' '\u00E3' '\u00E4' '\u00E5' '\u00E6'
  '\u00E7' '\u00E8' '\u00E9' '\u00EA' '\u00EB' '\u00EC' '\u00ED' '\u00EE'
  '\u00EF' '\u00F0' '\u00F1' '\u00F2' '\u00F3' '\u00F4' '\u00F5' '\u00F6'
  '\u00F8' '\u00F9' '\u00FA' '\u00FB' '\u00FC' '\u00FD' '\u00FE' '\u00FF'
  
```

Many other Unicode characters are lowercase too.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is lowercase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`

### isMirrored

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isMirrored(ch: Char): Boolean
```

Determines whether the character is mirrored according to the Unicode specification. Mirrored characters should have their glyphs horizontally mirrored when displayed in text that is right-to-left. For example, `'\u005Cu0028'` LEFT PARENTHESIS is semantically defined to be an *opening parenthesis*. This will appear as a "(" in text that is left-to-right but as a ")" in text that is right-to-left.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isMirrored(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): `char` for which the mirrored property is requested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the char is mirrored, `false` if the `char` is not mirrored or is not defined. |

### isMirrored

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isMirrored(codePoint: Int): Boolean
```

Determines whether the specified character (Unicode code point) is mirrored according to the Unicode specification. Mirrored characters should have their glyphs horizontally mirrored when displayed in text that is right-to-left. For example, `'\u005Cu0028'` LEFT PARENTHESIS is semantically defined to be an *opening parenthesis*. This will appear as a "(" in text that is left-to-right but as a ")" in text that is right-to-left.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is mirrored, `false` if the character is not mirrored or is not defined. |

### isSpace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSpace(ch: Char): Boolean
```

**Deprecated:** *Replaced by isWhitespace(char).*

Determines if the specified character is ISO-LATIN-1 white space. This method returns `true` for the following five characters only:

| Character | Code | Name |
| `'\t'` | `U+0009` | `HORIZONTAL TABULATION` |
| `'\n'` | `U+000A` | `NEW LINE` |
| `'\f'` | `U+000C` | `FORM FEED` |
| `'\r'` | `U+000D` | `CARRIAGE RETURN` |
| `' '` | `U+0020` | `SPACE` |
|---|---|---|

<br />

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is ISO-LATIN-1 white space; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Char)`

### isSpaceChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSpaceChar(ch: Char): Boolean
```

Determines if the specified character is a Unicode space character. A character is considered to be a space character if and only if it is specified to be a space character by the Unicode Standard. This method returns true if the character's general category type is any of the following:

- `SPACE_SEPARATOR`
- `LINE_SEPARATOR`
- `PARAGRAPH_SEPARATOR`

<br />

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a space character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Char)`

### isSpaceChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSpaceChar(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a Unicode space character. A character is considered to be a space character if and only if it is specified to be a space character by the Unicode Standard. This method returns true if the character's general category type is any of the following:

- `https://developer.android.com/reference/kotlin/java/lang/Character#SPACE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#LINE_SEPARATOR:kotlin.Byte`
- `https://developer.android.com/reference/kotlin/java/lang/Character#PARAGRAPH_SEPARATOR:kotlin.Byte`

<br />

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a space character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### isSupplementaryCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSupplementaryCodePoint(codePoint: Int): Boolean
```

Determines whether the specified character (Unicode code point) is in the [supplementary character](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary) range.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified code point is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_SUPPLEMENTARY_CODE_POINT:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_CODE_POINT:kotlin.Int` inclusive; `false` otherwise. |

### isSurrogate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSurrogate(ch: Char): Boolean
```

Determines if the given `char` value is a Unicode *surrogate code unit*.

Such values do not represent characters by themselves, but are used in the representation of [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary) in the UTF-16 encoding.

A char value is a surrogate code unit if and only if it is either a [low-surrogate code unit](https://developer.android.com/reference/kotlin/java/lang/Character#isLowSurrogate(kotlin.Char)) or a [high-surrogate code unit](https://developer.android.com/reference/kotlin/java/lang/Character#isHighSurrogate(kotlin.Char)).

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the `char` value to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `char` value is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_SURROGATE:kotlin.Char` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_SURROGATE:kotlin.Char` inclusive; `false` otherwise. |

### isSurrogatePair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isSurrogatePair(
    high: Char, 
    low: Char
): Boolean
```

Determines whether the specified pair of `char` values is a valid [Unicode surrogate pair](http://www.unicode.org/glossary/#surrogate_pair).

This method is equivalent to the expression:

```kotlin
<code>isHighSurrogate(high) &amp;&amp; isLowSurrogate(low)
  </code>
```

| Parameters ||
|---|---|
| `high` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the high-surrogate code value to be tested |
| `low` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the low-surrogate code value to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified high and low-surrogate code values represent a valid surrogate pair; `false` otherwise. |

### isTitleCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isTitleCase(ch: Char): Boolean
```

Determines if the specified character is a titlecase character.

A character is a titlecase character if its general category type, provided by `Character.getType(ch)`, is `TITLECASE_LETTER`.

Some characters look like pairs of Latin letters. For example, there is an uppercase letter that looks like "LJ" and has a corresponding lowercase letter that looks like "lj". A third form, which looks like "Lj", is the appropriate form to use when rendering a word in lowercase with initial capitals, as for a book title.

These are some of the Unicode characters for which this method returns `true`:

- `LATIN CAPITAL LETTER D WITH SMALL LETTER Z WITH CARON`
- `LATIN CAPITAL LETTER L WITH SMALL LETTER J`
- `LATIN CAPITAL LETTER N WITH SMALL LETTER J`
- `LATIN CAPITAL LETTER D WITH SMALL LETTER Z`

Many other Unicode characters are titlecase too.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is titlecase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)`

### isTitleCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isTitleCase(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is a titlecase character.

A character is a titlecase character if its general category type, provided by `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`, is `TITLECASE_LETTER`.

Some characters look like pairs of Latin letters. For example, there is an uppercase letter that looks like "LJ" and has a corresponding lowercase letter that looks like "lj". A third form, which looks like "Lj", is the appropriate form to use when rendering a word in lowercase with initial capitals, as for a book title.

These are some of the Unicode characters for which this method returns `true`:

- `LATIN CAPITAL LETTER D WITH SMALL LETTER Z WITH CARON`
- `LATIN CAPITAL LETTER L WITH SMALL LETTER J`
- `LATIN CAPITAL LETTER N WITH SMALL LETTER J`
- `LATIN CAPITAL LETTER D WITH SMALL LETTER Z`

Many other Unicode characters are titlecase too.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is titlecase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`

### isUnicodeIdentifierPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUnicodeIdentifierPart(ch: Char): Boolean
```

Determines if the specified character may be part of a Unicode identifier as other than the first character.

A character may be part of a Unicode identifier if and only if one of the following statements is true:

- it is a letter
- it is a connecting punctuation character (such as `'_'`)
- it is a digit
- it is a numeric letter (such as a Roman numeral character)
- it is a combining mark
- it is a non-spacing mark
- `isIdentifierIgnorable` returns `true` for this character.
- it is an [`Other_ID_Start`](http://www.unicode.org/reports/tr44/#Other_ID_Start) character.
- it is an [`Other_ID_Continue`](http://www.unicode.org/reports/tr44/#Other_ID_Continue) character.

This method conforms to [UAX31-R1: Default Identifiers](https://unicode.org/reports/tr31/#R1) requirement of the Unicode Standard, with the following profile of UAX31:

```kotlin
Continue := Start + ID_Continue + ignorable
  Medial := empty
  ignorable := isIdentifierIgnorable(char) returns true for the character
  
```
`ignorable` is added to `Continue` for backward compatibility.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may be part of a Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Char)`

### isUnicodeIdentifierPart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUnicodeIdentifierPart(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) may be part of a Unicode identifier as other than the first character.

A character may be part of a Unicode identifier if and only if one of the following statements is true:

- it is a letter
- it is a connecting punctuation character (such as `'_'`)
- it is a digit
- it is a numeric letter (such as a Roman numeral character)
- it is a combining mark
- it is a non-spacing mark
- `isIdentifierIgnorable` returns `true` for this character.
- it is an [`Other_ID_Start`](http://www.unicode.org/reports/tr44/#Other_ID_Start) character.
- it is an [`Other_ID_Continue`](http://www.unicode.org/reports/tr44/#Other_ID_Continue) character.

This method conforms to [UAX31-R1: Default Identifiers](https://unicode.org/reports/tr31/#R1) requirement of the Unicode Standard, with the following profile of UAX31:

```kotlin
Continue := Start + ID_Continue + ignorable
  Medial := empty
  ignorable := isIdentifierIgnorable(int) returns true for the character
  
```
`ignorable` is added to `Continue` for backward compatibility.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may be part of a Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isIdentifierIgnorable(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierPart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetterOrDigit(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Int)`

### isUnicodeIdentifierStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUnicodeIdentifierStart(ch: Char): Boolean
```

Determines if the specified character is permissible as the first character in a Unicode identifier.

A character may start a Unicode identifier if and only if one of the following conditions is true:

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)` returns `true`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)` returns `LETTER_NUMBER`.
- it is an [`Other_ID_Start`](http://www.unicode.org/reports/tr44/#Other_ID_Start) character.

This method conforms to [UAX31-R1: Default Identifiers](https://unicode.org/reports/tr31/#R1) requirement of the Unicode Standard, with the following profile of UAX31:

```kotlin
Start := ID_Start + 'VERTICAL TILDE' (U+2E2F)
  
```
`'VERTICAL TILDE'` is added to `Start` for backward compatibility.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierStart(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may start a Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Char)`

### isUnicodeIdentifierStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUnicodeIdentifierStart(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is permissible as the first character in a Unicode identifier.

A character may start a Unicode identifier if and only if one of the following conditions is true:

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)` returns `true`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)` returns `LETTER_NUMBER`.
- it is an [`Other_ID_Start`](http://www.unicode.org/reports/tr44/#Other_ID_Start) character.

This method conforms to [UAX31-R1: Default Identifiers](https://unicode.org/reports/tr31/#R1) requirement of the Unicode Standard, with the following profile of UAX31:

```kotlin
Start := ID_Start + 'VERTICAL TILDE' (U+2E2F)
  
```
`'VERTICAL TILDE'` is added to `Start` for backward compatibility.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character may start a Unicode identifier; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isJavaIdentifierStart(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isLetter(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isUnicodeIdentifierPart(kotlin.Int)`

### isUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUpperCase(ch: Char): Boolean
```

Determines if the specified character is an uppercase character.

A character is uppercase if its general category type, provided by `Character.getType(ch)`, is `UPPERCASE_LETTER`. or it has contributory property Other_Uppercase as defined by the Unicode Standard.

The following are examples of uppercase characters:

```kotlin
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
  '\u00C0' '\u00C1' '\u00C2' '\u00C3' '\u00C4' '\u00C5' '\u00C6' '\u00C7'
  '\u00C8' '\u00C9' '\u00CA' '\u00CB' '\u00CC' '\u00CD' '\u00CE' '\u00CF'
  '\u00D0' '\u00D1' '\u00D2' '\u00D3' '\u00D4' '\u00D5' '\u00D6' '\u00D8'
  '\u00D9' '\u00DA' '\u00DB' '\u00DC' '\u00DD' '\u00DE'
  
```

Many other Unicode characters are uppercase too.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is uppercase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Char)`

### isUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isUpperCase(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is an uppercase character.

A character is uppercase if its general category type, provided by `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`, is `UPPERCASE_LETTER`, or it has contributory property Other_Uppercase as defined by the Unicode Standard.

The following are examples of uppercase characters:

```kotlin
A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
  '\u00C0' '\u00C1' '\u00C2' '\u00C3' '\u00C4' '\u00C5' '\u00C6' '\u00C7'
  '\u00C8' '\u00C9' '\u00CA' '\u00CB' '\u00CC' '\u00CD' '\u00CE' '\u00CF'
  '\u00D0' '\u00D1' '\u00D2' '\u00D3' '\u00D4' '\u00D5' '\u00D6' '\u00D8'
  '\u00D9' '\u00DA' '\u00DB' '\u00DC' '\u00DD' '\u00DE'
  
```

Many other Unicode characters are uppercase too.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is uppercase; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#getType(kotlin.Int)`

### isValidCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isValidCodePoint(codePoint: Int): Boolean
```

Determines whether the specified code point is a valid [Unicode code point value](http://www.unicode.org/glossary/#code_point).

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the Unicode code point to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified code point value is between `https://developer.android.com/reference/kotlin/java/lang/Character#MIN_CODE_POINT:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/lang/Character#MAX_CODE_POINT:kotlin.Int` inclusive; `false` otherwise. |

### isWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isWhitespace(ch: Char): Boolean
```

Determines if the specified character is white space according to Java. A character is a Java whitespace character if and only if it satisfies one of the following criteria:

- It is a Unicode space character (`SPACE_SEPARATOR`, `LINE_SEPARATOR`, or `PARAGRAPH_SEPARATOR`) but is not also a non-breaking space (`'\u005Cu00A0'`, `'\u005Cu2007'`, `'\u005Cu202F'`).
- It is `'\u005Ct'`, U+0009 HORIZONTAL TABULATION.
- It is `'\u005Cn'`, U+000A LINE FEED.
- It is `'\u005Cu000B'`, U+000B VERTICAL TABULATION.
- It is `'\u005Cf'`, U+000C FORM FEED.
- It is `'\u005Cr'`, U+000D CARRIAGE RETURN.
- It is `'\u005Cu001C'`, U+001C FILE SEPARATOR.
- It is `'\u005Cu001D'`, U+001D GROUP SEPARATOR.
- It is `'\u005Cu001E'`, U+001E RECORD SEPARATOR.
- It is `'\u005Cu001F'`, U+001F UNIT SEPARATOR.

<br />

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a Java whitespace character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Char)`

### isWhitespace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isWhitespace(codePoint: Int): Boolean
```

Determines if the specified character (Unicode code point) is white space according to Java. A character is a Java whitespace character if and only if it satisfies one of the following criteria:

- It is a Unicode space character (`https://developer.android.com/reference/kotlin/java/lang/Character#SPACE_SEPARATOR:kotlin.Byte`, `https://developer.android.com/reference/kotlin/java/lang/Character#LINE_SEPARATOR:kotlin.Byte`, or `https://developer.android.com/reference/kotlin/java/lang/Character#PARAGRAPH_SEPARATOR:kotlin.Byte`) but is not also a non-breaking space (`'\u005Cu00A0'`, `'\u005Cu2007'`, `'\u005Cu202F'`).
- It is `'\u005Ct'`, U+0009 HORIZONTAL TABULATION.
- It is `'\u005Cn'`, U+000A LINE FEED.
- It is `'\u005Cu000B'`, U+000B VERTICAL TABULATION.
- It is `'\u005Cf'`, U+000C FORM FEED.
- It is `'\u005Cr'`, U+000D CARRIAGE RETURN.
- It is `'\u005Cu001C'`, U+001C FILE SEPARATOR.
- It is `'\u005Cu001D'`, U+001D GROUP SEPARATOR.
- It is `'\u005Cu001E'`, U+001E RECORD SEPARATOR.
- It is `'\u005Cu001F'`, U+001F UNIT SEPARATOR.

<br />

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be tested. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character is a Java whitespace character; `false` otherwise. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isSpaceChar(kotlin.Int)`

### lowSurrogate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lowSurrogate(codePoint: Int): Char
```

Returns the trailing surrogate (a [low surrogate code unit](http://www.unicode.org/glossary/#low_surrogate_code_unit)) of the [surrogate pair](http://www.unicode.org/glossary/#surrogate_pair) representing the specified supplementary character (Unicode code point) in the UTF-16 encoding. If the specified character is not a [supplementary character](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary), an unspecified `char` is returned.

If `https://developer.android.com/reference/kotlin/java/lang/Character#isSupplementaryCodePoint(kotlin.Int)` is `true`, then `https://developer.android.com/reference/kotlin/java/lang/Character#isLowSurrogate(kotlin.Char)``(lowSurrogate(x))` and `https://developer.android.com/reference/kotlin/java/lang/Character#toCodePoint(kotlin.Char,%20kotlin.Char)``(``https://developer.android.com/reference/kotlin/java/lang/Character#highSurrogate(kotlin.Int)``(x), lowSurrogate(x)) == x` are also always `true`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a supplementary character (Unicode code point) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the trailing surrogate code unit used to represent the character in the UTF-16 encoding |

### offsetByCodePoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun offsetByCodePoints(
    a: CharArray!, 
    start: Int, 
    count: Int, 
    index: Int, 
    codePointOffset: Int
): Int
```

Returns the index within the given `char` subarray that is offset from the given `index` by `codePointOffset` code points. The `start` and `count` arguments specify a subarray of the `char` array. Unpaired surrogates within the text range given by `index` and `codePointOffset` count as one code point each.

| Parameters ||
|---|---|
| `a` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the `char` array |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the first `char` of the subarray |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the subarray in `char`s |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to be offset |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in code points |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index within the subarray |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `start` or `count` is negative, or if `start + count` is larger than the length of the given array, or if `index` is less than `start` or larger then `start + count`, or if `codePointOffset` is positive and the text range starting with `index` and ending with `start + count - 1` has fewer than `codePointOffset` code points, or if `codePointOffset` is negative and the text range starting with `start` and ending with `index - 1` has fewer than the absolute value of `codePointOffset` code points. |
| `java.lang.NullPointerException` | if `a` is null. |

### offsetByCodePoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun offsetByCodePoints(
    seq: CharSequence, 
    index: Int, 
    codePointOffset: Int
): Int
```

Returns the index within the given char sequence that is offset from the given `index` by `codePointOffset` code points. Unpaired surrogates within the text range given by `index` and `codePointOffset` count as one code point each.

| Parameters ||
|---|---|
| `seq` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the char sequence |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to be offset |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in code points |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index within the char sequence |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `index` is negative or larger than the length of the char sequence, or if `codePointOffset` is positive and the subsequence starting with `index` has fewer than `codePointOffset` code points, or if `codePointOffset` is negative and the subsequence before `index` has fewer than the absolute value of `codePointOffset` code points. |
| `java.lang.NullPointerException` | if `seq` is null. |

### reverseBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun reverseBytes(ch: Char): Char
```

Returns the value obtained by reversing the order of the bytes in the specified `char` value.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The `char` of which to reverse the byte order. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the value obtained by reversing (or, equivalently, swapping) the bytes in the specified `char` value. |

### toChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toChars(codePoint: Int): CharArray!
```

Converts the specified character (Unicode code point) to its UTF-16 representation stored in a `char` array. If the specified code point is a BMP (Basic Multilingual Plane or Plane 0) value, the resulting `char` array has the same value as `codePoint`. If the specified code point is a supplementary code point, the resulting `char` array has the corresponding surrogate pair.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a Unicode code point |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!` | a `char` array having `codePoint`'s UTF-16 representation. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `codePoint` is not a valid Unicode code point. |

### toChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toChars(
    codePoint: Int, 
    dst: CharArray!, 
    dstIndex: Int
): Int
```

Converts the specified character (Unicode code point) to its UTF-16 representation. If the specified code point is a BMP (Basic Multilingual Plane or Plane 0) value, the same value is stored in `dst[dstIndex]`, and 1 is returned. If the specified code point is a supplementary character, its surrogate values are stored in `dst[dstIndex]` (high-surrogate) and `dst[dstIndex+1]` (low-surrogate), and 2 is returned.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: an array of `char` in which the `codePoint`'s UTF-16 value is stored. |
| `dstIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the start index into the `dst` array where the converted value is stored. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | 1 if the code point is a BMP code point, 2 if the code point is a supplementary code point. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `codePoint` is not a valid Unicode code point. |
| `java.lang.IndexOutOfBoundsException` | if `dstIndex` is negative or not less than `dst.length`, or if `dst` at `dstIndex` doesn't have enough array element(s) to store the resulting `char` value(s). (If `dstIndex` is equal to `dst.length-1` and the specified `codePoint` is a supplementary character, the high-surrogate value is not stored in `dst[dstIndex]`.) |
| `java.lang.NullPointerException` | if the specified `dst` is null. |

### toCodePoint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toCodePoint(
    high: Char, 
    low: Char
): Int
```

Converts the specified surrogate pair to its supplementary code point value. This method does not validate the specified surrogate pair. The caller must validate it using `https://developer.android.com/reference/kotlin/java/lang/Character#isSurrogatePair(kotlin.Char,%20kotlin.Char)` if necessary.

| Parameters ||
|---|---|
| `high` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the high-surrogate code unit |
| `low` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the low-surrogate code unit |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the supplementary code point composed from the specified surrogate pair. |

### toLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toLowerCase(ch: Char): Char
```

Converts the character argument to lowercase using case mapping information from the UnicodeData file.

Note that `Character.isLowerCase(Character.toLowerCase(ch))` does not always return `true` for some ranges of characters, particularly those that are symbols or ideographs.

In general, `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()` should be used to map characters to lowercase. `String` case mapping methods have several benefits over `Character` case mapping methods. `String` case mapping methods can perform locale-sensitive mappings, context-sensitive mappings, and 1:M character mappings, whereas the `Character` case mapping methods cannot.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the lowercase equivalent of the character, if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()`

### toLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toLowerCase(codePoint: Int): Int
```

Converts the character (Unicode code point) argument to lowercase using case mapping information from the UnicodeData file.

Note that `Character.isLowerCase(Character.toLowerCase(codePoint))` does not always return `true` for some ranges of characters, particularly those that are symbols or ideographs.

In general, `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()` should be used to map characters to lowercase. `String` case mapping methods have several benefits over `Character` case mapping methods. `String` case mapping methods can perform locale-sensitive mappings, context-sensitive mappings, and 1:M character mappings, whereas the `Character` case mapping methods cannot.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the lowercase equivalent of the character (Unicode code point), if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a `String` object representing this `Character`'s value. The result is a string of length 1 whose sole component is the primitive `char` value represented by this `Character` object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this object. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(c: Char): String
```

Returns a `String` object representing the specified `char`. The result is a string of length 1 consisting solely of the specified `char`.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the `char` to be converted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string representation of the specified `char` |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toString(codePoint: Int): String
```

Returns a `String` object representing the specified character (Unicode code point). The result is a string of length 1 or 2, consisting solely of the specified `codePoint`.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the `codePoint` to be converted |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string representation of the specified `codePoint` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified `codePoint` is not a [valid Unicode code point](https://developer.android.com/reference/kotlin/java/lang/Character#isValidCodePoint(kotlin.Int)). |

### toTitleCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toTitleCase(ch: Char): Char
```

Converts the character argument to titlecase using case mapping information from the UnicodeData file. If a character has no explicit titlecase mapping and is not itself a titlecase char according to UnicodeData, then the uppercase mapping is returned as an equivalent titlecase mapping. If the `char` argument is already a titlecase `char`, the same `char` value will be returned.

Note that `Character.isTitleCase(Character.toTitleCase(ch))` does not always return `true` for some ranges of characters.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#toTitleCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the titlecase equivalent of the character, if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Char)`

### toTitleCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toTitleCase(codePoint: Int): Int
```

Converts the character (Unicode code point) argument to titlecase using case mapping information from the UnicodeData file. If a character has no explicit titlecase mapping and is not itself a titlecase char according to UnicodeData, then the uppercase mapping is returned as an equivalent titlecase mapping. If the character argument is already a titlecase character, the same character value will be returned.

Note that `Character.isTitleCase(Character.toTitleCase(codePoint))` does not always return `true` for some ranges of characters.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the titlecase equivalent of the character, if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isTitleCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toLowerCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Int)`

### toUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toUpperCase(ch: Char): Char
```

Converts the character argument to uppercase using case mapping information from the UnicodeData file.

Note that `Character.isUpperCase(Character.toUpperCase(ch))` does not always return `true` for some ranges of characters, particularly those that are symbols or ideographs.

In general, `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()` should be used to map characters to uppercase. `String` case mapping methods have several benefits over `Character` case mapping methods. `String` case mapping methods can perform locale-sensitive mappings, context-sensitive mappings, and 1:M character mappings, whereas the `Character` case mapping methods cannot.

**Note:** This method cannot handle [supplementary characters](https://developer.android.com/reference/kotlin/java/lang/Character#supplementary). To support all Unicode characters, including supplementary characters, use the `https://developer.android.com/reference/kotlin/java/lang/Character#toUpperCase(kotlin.Int)` method.

| Parameters ||
|---|---|
| `ch` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the uppercase equivalent of the character, if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()`

### toUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun toUpperCase(codePoint: Int): Int
```

Converts the character (Unicode code point) argument to uppercase using case mapping information from the UnicodeData file.

Note that `Character.isUpperCase(Character.toUpperCase(codePoint))` does not always return `true` for some ranges of characters, particularly those that are symbols or ideographs.

In general, `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()` should be used to map characters to uppercase. `String` case mapping methods have several benefits over `Character` case mapping methods. `String` case mapping methods can perform locale-sensitive mappings, context-sensitive mappings, and 1:M character mappings, whereas the `Character` case mapping methods cannot.

| Parameters ||
|---|---|
| `codePoint` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character (Unicode code point) to be converted. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the uppercase equivalent of the character, if any; otherwise, the character itself. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isUpperCase(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()`

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(c: Char): Char
```

Returns a `Character` instance representing the specified `char` value. If a new `Character` instance is not required, this method should generally be used in preference to the constructor `https://developer.android.com/reference/kotlin/java/lang/Character#Character(kotlin.Char)`, as this method is likely to yield significantly better space and time performance by caching frequently requested values. This method will always cache values in the range `'\u005Cu0000'` to `'\u005Cu007F'`, inclusive, and may cache other values outside of this range.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): a char value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | a `Character` instance representing `c`. |

## Properties

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE: Class<Char!>!
```

The `Class` instance representing the primitive type `char`.
