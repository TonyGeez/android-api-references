# Normalizer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Normalizer

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/Normalizer "View this page in Java") 

```
class Normalizer : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.text.Normalizer](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#) |

Old Unicode normalization API.

This API has been replaced by the [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2) class and is only available for backward compatibility. This class simply delegates to the Normalizer2 class. There are two exceptions: The new API does not provide a replacement for`QuickCheckResult`and`compare()`.

`normalize`transforms Unicode text into an equivalent composed or decomposed form, allowing for easier sorting and searching of text.`normalize`supports the standard normalization forms described in [Unicode Standard Annex #15 --- Unicode Normalization Forms](https://www.unicode.org/reports/tr15/).

Characters with accents or other adornments can be encoded in several different ways in Unicode. For example, take the character A-acute. In Unicode, this can be encoded as a single character (the "composed" form): 

```kotlin
00C1    LATIN CAPITAL LETTER A WITH ACUTE
  
```
or as two separate characters (the "decomposed" form): 

```kotlin
0041    LATIN CAPITAL LETTER A
       0301    COMBINING ACUTE ACCENT
  
```

To a user of your program, however, both of these sequences should be treated as the same "user-level" character "A with acute accent". When you are searching or comparing text, you must ensure that these two sequences are treated equivalently. In addition, you must handle characters with more than one accent. Sometimes the order of a character's combining accents is significant, while in other cases accent sequences in different orders are really equivalent.

Similarly, the string "ffi" can be encoded as three separate letters: 

```kotlin
0066    LATIN SMALL LETTER F
       0066    LATIN SMALL LETTER F
       0069    LATIN SMALL LETTER I
  
```
or as the single character 

```kotlin
FB03    LATIN SMALL LIGATURE FFI
  
```

The ffi ligature is not a distinct semantic character, and strictly speaking it shouldn't be in Unicode at all, but it was included for compatibility with existing character sets that already provided it. The Unicode standard identifies such characters by giving them "compatibility" decompositions into the corresponding semantic characters. When sorting and searching, you will often want to use these mappings.

`normalize`helps solve these problems by transforming text into the canonical composed and decomposed forms as shown in the first example above. In addition, you can have it perform compatibility decompositions so that you can treat compatibility characters the same as their equivalents. Finally,`normalize`rearranges accents into the proper canonical order, so that you do not have to worry about accent rearrangement on your own.

Form FCD, "Fast C or D", is also designed for collation. It allows to work on strings that are not necessarily normalized with an algorithm (like in collation) that works under "canonical closure", i.e., it treats precomposed characters and their decomposed equivalents the same.

It is not a normalization form because it does not provide for uniqueness of representation. Multiple strings may be canonically equivalent (their NFDs are identical) and may all conform to FCD without being identical themselves.

The form is defined such that the "raw decomposition", the recursive canonical decomposition of each character, results in a string that is canonically ordered. This means that precomposed characters are allowed for as long as their decompositions do not need canonical reordering.

Its advantage for a process like collation is that all NFD and most NFC texts - and many unnormalized texts - already conform to FCD and do not need to be normalized (NFD) for such a process. The FCD quick check will return YES for most strings in practice.

normalize(FCD) may be implemented with NFD.

For more details on FCD see Unicode Technical Note #5 (Canonical Equivalence in Applications): http://www.unicode.org/notes/tn5/#FCD

ICU collation performs either NFD or FCD normalization automatically if normalization is turned on for the collator object. Beyond collation and string search, normalized strings may be useful for string equivalence comparisons, transliteration/transcription, unique representations, etc.

The W3C generally recommends to exchange texts in NFC. Note also that most legacy character encodings use only precomposed forms and often do not encode any combining marks by themselves. For conversion to such character encodings the Unicode text needs to be normalized to NFC. For more usage examples, see the Unicode Standard Annex.

Note: The Normalizer class also provides API for iterative normalization. While the setIndex() and getIndex() refer to indices in the underlying Unicode input text, the next() and previous() methods iterate through characters in the normalized output. This means that there is not necessarily a one-to-one correspondence between characters returned by next() and previous() and the indices passed to and returned from setIndex() and getIndex(). It is for this reason that Normalizer does not implement the CharacterIterator interface.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------|
| | [QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult) Result values for quickCheck(). |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPARE_CODE_POINT_ORDER](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#COMPARE_CODE_POINT_ORDER:kotlin.Int) Option bit for compare: Compare strings in code point order instead of code unit order. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPARE_IGNORE_CASE](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#COMPARE_IGNORE_CASE:kotlin.Int) Option bit for compare: Perform case-insensitive comparison. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FOLD_CASE_DEFAULT](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#FOLD_CASE_DEFAULT:kotlin.Int) Option bit for compare: Case sensitively compare the strings |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FOLD_CASE_EXCLUDE_SPECIAL_I](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#FOLD_CASE_EXCLUDE_SPECIAL_I:kotlin.Int) Option value for case folding: Use the modified set of mappings provided in CaseFolding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_IS_FCD](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#INPUT_IS_FCD:kotlin.Int) Option bit for compare: Both input strings are assumed to fulfill FCD conditions. |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#compare(kotlin.CharArray,%20kotlin.CharArray,%20kotlin.Int))`(`s1:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `s2:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compare two strings for canonical equivalence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#compare(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s1:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `s1Start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `s1Limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `s2:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `s2Start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `s2Limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compare two strings for canonical equivalence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#compare(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`char32a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `char32b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience method that can have faster implementation by not allocating buffers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#compare(kotlin.Int,%20kotlin.String,%20kotlin.Int))`(`char32a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `str2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Convenience method that can have faster implementation by not allocating buffers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#compare(kotlin.String,%20kotlin.String,%20kotlin.Int))`(`s1:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `s2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `options:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compare two strings for canonical equivalence. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Normalizer.QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult)! | [MAYBE](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#MAYBE:android.icu.text.Normalizer.QuickCheckResult) Indicates it cannot be determined if string is in the normalized format without further thorough checks. |
| static [Normalizer.QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult)! | [NO](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#NO:android.icu.text.Normalizer.QuickCheckResult) Indicates that string is not in the normalized format |
| static [Normalizer.QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult)! | [YES](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer#YES:android.icu.text.Normalizer.QuickCheckResult) Indicates that string is in the normalized format |

## Constants

### COMPARE_CODE_POINT_ORDER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPARE_CODE_POINT_ORDER: Int
```

Option bit for compare: Compare strings in code point order instead of code unit order. 

 Value: 32768

### COMPARE_IGNORE_CASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPARE_IGNORE_CASE: Int
```

Option bit for compare: Perform case-insensitive comparison. 

 Value: 65536

### FOLD_CASE_DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOLD_CASE_DEFAULT: Int
```

Option bit for compare: Case sensitively compare the strings 

 Value: 0

### FOLD_CASE_EXCLUDE_SPECIAL_I

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FOLD_CASE_EXCLUDE_SPECIAL_I: Int
```

Option value for case folding: Use the modified set of mappings provided in CaseFolding.txt to handle dotted I and dotless i appropriately for Turkic languages (tr, az). 

 Value: 1

**See Also**

- [android.icu.lang.UCharacter#FOLD_CASE_EXCLUDE_SPECIAL_I](https://developer.android.com/reference/kotlin/android/icu/lang/UCharacter.html#FOLD_CASE_EXCLUDE_SPECIAL_I:kotlin.Int) 

### INPUT_IS_FCD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_IS_FCD: Int
```

Option bit for compare: Both input strings are assumed to fulfill FCD conditions. 

 Value: 131072

## Public methods

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    s1: CharArray!, 
    s2: CharArray!, 
    options: Int
): Int
```

Compare two strings for canonical equivalence. Further options include case-insensitive comparison and code point order (as opposed to code unit order). Convenience method.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s1` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:First source string. |
| `s2` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Second source string. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options: - FOLD_CASE_DEFAULT or 0 is used for default options: Case-sensitive comparison in code unit order, and the input strings are quick-checked for FCD. - INPUT_IS_FCD Set if the caller knows that both s1 and s2 fulfill the FCD conditions. If not set, the function will quickCheck for FCD and normalize if necessary. - COMPARE_CODE_POINT_ORDER Set to choose code point order instead of code unit order - COMPARE_IGNORE_CASE Set to compare strings case-insensitively using case folding, instead of case-sensitively. If set, then the following case folding options are used. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \<0 or 0 or \>0 as usual for string comparisons |

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    s1: CharArray!, 
    s1Start: Int, 
    s1Limit: Int, 
    s2: CharArray!, 
    s2Start: Int, 
    s2Limit: Int, 
    options: Int
): Int
```

Compare two strings for canonical equivalence. Further options include case-insensitive comparison and code point order (as opposed to code unit order). Canonical equivalence between two strings is defined as their normalized forms (NFD or NFC) being identical. This function compares strings incrementally instead of normalizing (and optionally case-folding) both strings entirely, improving performance significantly. Bulk normalization is only necessary if the strings do not fulfill the FCD conditions. Only in this case, and only if the strings are relatively long, is memory allocated temporarily. For FCD strings and short non-FCD strings there is no memory allocation. Semantically, this is equivalent to strcmp\ [CodePointOrder\](foldCase(NFD(s1)), foldCase(NFD(s2))) where code point order and foldCase are all optional.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s1` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:First source character array. |
| `s1Start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):start index of source |
| `s1Limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):limit of the source |
| `s2` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!:Second source character array. |
| `s2Start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):start index of the source |
| `s2Limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):limit of the source |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options: - FOLD_CASE_DEFAULT or 0 is used for default options: Case-sensitive comparison in code unit order, and the input strings are quick-checked for FCD. - INPUT_IS_FCD Set if the caller knows that both s1 and s2 fulfill the FCD conditions.If not set, the function will quickCheck for FCD and normalize if necessary. - COMPARE_CODE_POINT_ORDER Set to choose code point order instead of code unit order - COMPARE_IGNORE_CASE Set to compare strings case-insensitively using case folding, instead of case-sensitively. If set, then the following case folding options are used. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \<0 or 0 or \>0 as usual for string comparisons |

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    char32a: Int, 
    char32b: Int, 
    options: Int
): Int
```

Convenience method that can have faster implementation by not allocating buffers.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `char32a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first code point to be checked against the |
| `char32b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the second code point |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options |

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    char32a: Int, 
    str2: String!, 
    options: Int
): Int
```

Convenience method that can have faster implementation by not allocating buffers.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `char32a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the first code point to be checked against |
| `str2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the second string |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options |

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compare(
    s1: String!, 
    s2: String!, 
    options: Int
): Int
```

Compare two strings for canonical equivalence. Further options include case-insensitive comparison and code point order (as opposed to code unit order). Canonical equivalence between two strings is defined as their normalized forms (NFD or NFC) being identical. This function compares strings incrementally instead of normalizing (and optionally case-folding) both strings entirely, improving performance significantly. Bulk normalization is only necessary if the strings do not fulfill the FCD conditions. Only in this case, and only if the strings are relatively long, is memory allocated temporarily. For FCD strings and short non-FCD strings there is no memory allocation. Semantically, this is equivalent to strcmp\ [CodePointOrder\](foldCase(NFD(s1)), foldCase(NFD(s2))) where code point order and foldCase are all optional.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:First source string. |
| `s2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Second source string. |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A bit set of options: - FOLD_CASE_DEFAULT or 0 is used for default options: Case-sensitive comparison in code unit order, and the input strings are quick-checked for FCD. - INPUT_IS_FCD Set if the caller knows that both s1 and s2 fulfill the FCD conditions. If not set, the function will quickCheck for FCD and normalize if necessary. - COMPARE_CODE_POINT_ORDER Set to choose code point order instead of code unit order - COMPARE_IGNORE_CASE Set to compare strings case-insensitively using case folding, instead of case-sensitively. If set, then the following case folding options are used. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | \<0 or 0 or \>0 as usual for string comparisons |

## Properties

### MAYBE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAYBE: Normalizer.QuickCheckResult!
```

Indicates it cannot be determined if string is in the normalized format without further thorough checks. 

### NO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO: Normalizer.QuickCheckResult!
```

Indicates that string is not in the normalized format 

### YES

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YES: Normalizer.QuickCheckResult!
```

Indicates that string is in the normalized format
