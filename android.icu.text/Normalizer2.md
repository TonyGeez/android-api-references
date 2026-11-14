# Normalizer2

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Normalizer2

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/Normalizer2 "View this page in Java") 
| --- | --- |

```
abstract class Normalizer2
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#) |

Unicode normalization functionality for standard Unicode normalization or for using custom mapping tables. All instances of this class are unmodifiable/immutable. The Normalizer2 class is not intended for public subclassing.

The primary functions are to produce a normalized string and to detect whether a string is already normalized. The most commonly used normalization forms are those defined in https://www.unicode.org/reports/tr15/ However, this API supports additional normalization forms for specialized purposes. For example, NFKC_Casefold is provided via getInstance("nfkc_cf", COMPOSE) and can be used in implementations of UTS #46.

Not only are the standard compose and decompose modes supplied, but additional modes are provided as documented in the Mode enum.

Some of the functions in this class identify normalization boundaries. At a normalization boundary, the portions of the string before it and starting from it do not interact and can be handled independently.

The spanQuickCheckYes() stops at a normalization boundary. When the goal is a normalized string, then the text before the boundary can be copied, and the remainder can be processed with normalizeSecondAndAppend().

The hasBoundaryBefore(), hasBoundaryAfter() and isInert() functions test whether a character is guaranteed to be at a normalization boundary, regardless of context. This is used for moving from one normalization boundary to the next or preceding boundary, and for performing iterative normalization.

Iterative normalization is useful when only a small portion of a longer string needs to be processed. For example, in ICU, iterative normalization is used by the NormalizationTransliterator (to avoid replacing already-normalized text) and ucol_nextSortKeyPart() (to process only the substring for which sort key bytes are computed).

The set of normalization boundaries returned by these functions may not be complete: There may be more boundaries that could be returned. Different functions may return different boundaries.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------|
| | [Mode](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2.Mode) Constants for normalization modes. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [append](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#append(java.lang.StringBuilder,%20kotlin.CharSequence))`(`first:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `second:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Appends the second string to the first string (merging them at the boundary) and returns the first string. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [composePair](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#composePair(kotlin.Int,%20kotlin.Int))`(`a:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `b:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs pairwise composition of a \& b and returns the composite if there is one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCombiningClass](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getCombiningClass(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the combining class of c. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDecomposition](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getDecomposition(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the decomposition mapping of c. |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getInstance(java.io.InputStream,%20kotlin.String,%20android.icu.text.Normalizer2.Mode))`(`data:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mode:` ` [Normalizer2.Mode](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2.Mode)!`)` Returns a Normalizer2 instance which uses the specified data file (an ICU data file if data=null, or else custom binary data) and which composes or decomposes text according to the specified mode. |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFCInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFCInstance())`()` Returns a Normalizer2 instance for Unicode NFC normalization. |
| --- | --- |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFDInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFDInstance())`()` Returns a Normalizer2 instance for Unicode NFD normalization. |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFKCCasefoldInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFKCCasefoldInstance())`()` Returns a Normalizer2 instance for Unicode toNFKC_Casefold() normalization which is equivalent to applying the NFKC_Casefold mappings and then NFC. |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFKCInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFKCInstance())`()` Returns a Normalizer2 instance for Unicode NFKC normalization. |
| --- | --- |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFKCSimpleCasefoldInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFKCSimpleCasefoldInstance())`()` Returns a Normalizer2 instance for a variant of Unicode toNFKC_Casefold() normalization which is equivalent to applying the NFKC_Simple_Casefold mappings and then NFC. |
| openstatic [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | [getNFKDInstance](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getNFKDInstance())`()` Returns a Normalizer2 instance for Unicode NFKD normalization. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRawDecomposition](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#getRawDecomposition(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the raw decomposition mapping of c. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBoundaryAfter](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#hasBoundaryAfter(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Tests if the character always has a normalization boundary after it, regardless of context. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasBoundaryBefore](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#hasBoundaryBefore(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Tests if the character always has a normalization boundary before it, regardless of context. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInert](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#isInert(kotlin.Int))`(`c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Tests if the character is normalization-inert. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNormalized](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#isNormalized(kotlin.CharSequence))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Tests if the string is normalized. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [normalize](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#normalize(kotlin.CharSequence))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the normalized form of the source string. |
| abstract [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable.html#)! | [normalize](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#normalize(kotlin.CharSequence,%20java.lang.Appendable))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable.html#)!`)` Writes the normalized form of the source string to the destination Appendable and returns the destination Appendable. |
| --- | --- |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [normalize](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#normalize(kotlin.CharSequence,%20java.lang.StringBuilder))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `dest:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`)` Writes the normalized form of the source string to the destination string (replacing its contents) and returns the destination string. |
| abstract [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | [normalizeSecondAndAppend](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#normalizeSecondAndAppend(java.lang.StringBuilder,%20kotlin.CharSequence))`(`first:` ` [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!`, `second:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Appends the normalized form of the second string to the first string (merging them at the boundary) and returns the first string. |
| abstract [Normalizer.QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult)! | [quickCheck](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#quickCheck(kotlin.CharSequence))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Tests if the string is normalized. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [spanQuickCheckYes](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#spanQuickCheckYes(kotlin.CharSequence))`(`s:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Returns the end of the normalized substring of the input string. |

## Public methods

### append

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun append(
    first: StringBuilder!, 
    second: CharSequence!
): StringBuilder!
```

Appends the second string to the first string (merging them at the boundary) and returns the first string. The result is normalized if both the strings were normalized. The first and second strings must be different objects.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `first` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:string, should be normalized |
| `second` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:string, should be normalized |

| Return ||
|------------------------------------------------------------------------------------------------|-------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | first |

### composePair

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun composePair(
    a: Int, 
    b: Int
): Int
```

Performs pairwise composition of a \& b and returns the composite if there is one.

Returns a composite code point c only if c has a two-way mapping to a+b. In standard Unicode normalization, this means that c has a canonical decomposition to a+b and c does not have the Full_Composition_Exclusion property.

This function is independent of the mode of the Normalizer2. The default implementation returns a negative value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------|
| `a` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A (normalization starter) code point. |
| `b` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Another code point. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The non-negative composite code point if there is one; otherwise a negative value. |

### getCombiningClass

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCombiningClass(c: Int): Int
```

Gets the combining class of c. The default implementation returns 0 but all standard implementations return the Unicode Canonical_Combining_Class value.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | c's combining class |

### getDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDecomposition(c: Int): String!
```

Gets the decomposition mapping of c. Roughly equivalent to normalizing the String form of c on a DECOMPOSE Normalizer2 instance, but much faster, and except that this function returns null if c does not have a decomposition mapping in this instance's data. This function is independent of the mode of the Normalizer2.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | c's decomposition mapping, if any; otherwise null |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    data: InputStream!, 
    name: String!, 
    mode: Normalizer2.Mode!
): Normalizer2!
```

**Deprecated:** *Don't use because the binary`data`format is not stable across API levels.*

Returns a Normalizer2 instance which uses the specified data file (an ICU data file if data=null, or else custom binary data) and which composes or decomposes text according to the specified mode. Returns an unmodifiable singleton instance.

- Use data=null for data files that are part of ICU's own data.
- Use name="nfc" and COMPOSE/DECOMPOSE for Unicode standard NFC/NFD.
- Use name="nfkc" and COMPOSE/DECOMPOSE for Unicode standard NFKC/NFKD.
- Use name="nfkc_cf" and COMPOSE for Unicode standard NFKC_CF=NFKC_Casefold.

If data!=null, then the binary data is read once and cached using the provided name as the key. If you know or expect the data to be cached already, you can use data!=null for non-ICU data as well.

<br />

Any [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) is wrapped into a [android.icu.util.ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException.html#).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the binary, big-endian normalization (.nrm file) data, or null for ICU data |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:"nfc" or "nfkc" or "nfkc_cf" or "nfkc_scf" or name of custom data file |
| `mode` | [Normalizer2.Mode](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2.Mode)!:normalization mode (compose or decompose etc.) |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFCInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFCInstance(): Normalizer2!
```

Returns a Normalizer2 instance for Unicode NFC normalization. Same as getInstance(null, "nfc", Mode.COMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFDInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFDInstance(): Normalizer2!
```

Returns a Normalizer2 instance for Unicode NFD normalization. Same as getInstance(null, "nfc", Mode.DECOMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFKCCasefoldInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFKCCasefoldInstance(): Normalizer2!
```

Returns a Normalizer2 instance for Unicode toNFKC_Casefold() normalization which is equivalent to applying the NFKC_Casefold mappings and then NFC. See https://www.unicode.org/reports/tr44/#NFKC_Casefold

Same as getInstance(null, "nfkc_cf", Mode.COMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFKCInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFKCInstance(): Normalizer2!
```

Returns a Normalizer2 instance for Unicode NFKC normalization. Same as getInstance(null, "nfkc", Mode.COMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFKCSimpleCasefoldInstance

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFKCSimpleCasefoldInstance(): Normalizer2!
```

Returns a Normalizer2 instance for a variant of Unicode toNFKC_Casefold() normalization which is equivalent to applying the NFKC_Simple_Casefold mappings and then NFC. See https://www.unicode.org/reports/tr44/#NFKC_Simple_Casefold

Same as getInstance(null, "nfkc_scf", Mode.COMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getNFKDInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNFKDInstance(): Normalizer2!
```

Returns a Normalizer2 instance for Unicode NFKD normalization. Same as getInstance(null, "nfkc", Mode.DECOMPOSE). Returns an unmodifiable singleton instance.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------|
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2#)! | the requested Normalizer2, if successful |

### getRawDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRawDecomposition(c: Int): String!
```

Gets the raw decomposition mapping of c.

This is similar to the getDecomposition() method but returns the raw decomposition mapping as specified in UnicodeData.txt or (for custom data) in the mapping files processed by the gennorm2 tool. By contrast, getDecomposition() returns the processed, recursively-decomposed version of this mapping.

When used on a standard NFKC Normalizer2 instance, getRawDecomposition() returns the Unicode Decomposition_Mapping (dm) property.

When used on a standard NFC Normalizer2 instance, it returns the Decomposition_Mapping only if the Decomposition_Type (dt) is Canonical (Can); in this case, the result contains either one or two code points (=1..4 Java chars).

This function is independent of the mode of the Normalizer2. The default implementation returns null.

| Parameters ||
|-----|---------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):code point |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | c's raw decomposition mapping, if any; otherwise null |

### hasBoundaryAfter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasBoundaryAfter(c: Int): Boolean
```

Tests if the character always has a normalization boundary after it, regardless of context. If true, then the character does not normalization-interact with following characters. In other words, a string containing this character can be normalized by processing portions up to this character and after this character independently. This is used for iterative normalization. See the class documentation for details.

Note that this operation may be significantly slower than hasBoundaryBefore().

| Parameters ||
|-----|----------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):character to test |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if c has a normalization boundary after it |

### hasBoundaryBefore

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasBoundaryBefore(c: Int): Boolean
```

Tests if the character always has a normalization boundary before it, regardless of context. If true, then the character does not normalization-interact with preceding characters. In other words, a string containing this character can be normalized by processing portions before this character and starting from this character independently. This is used for iterative normalization. See the class documentation for details.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):character to test |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if c has a normalization boundary before it |

### isInert

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isInert(c: Int): Boolean
```

Tests if the character is normalization-inert. If true, then the character does not change, nor normalization-interact with preceding or following characters. In other words, a string containing this character can be normalized by processing portions before this character and after this character independently. This is used for iterative normalization. See the class documentation for details.

Note that this operation may be significantly slower than hasBoundaryBefore().

| Parameters ||
|-----|----------------------------------------------------------------------------------------------|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):character to test |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if c is normalization-inert |

### isNormalized

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNormalized(s: CharSequence!): Boolean
```

Tests if the string is normalized. Internally, in cases where the quickCheck() method would return "maybe" (which is only possible for the two COMPOSE modes) this method resolves to "yes" or "no" to provide a definitive result, at the cost of doing more work in those cases.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:input string |

| Return ||
|------------------------------------------------------------------------------------|-------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if s is normalized |

### normalize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun normalize(src: CharSequence!): String!
```

Returns the normalized form of the source string.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:source string |

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | normalized src |

### normalize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalize(
    src: CharSequence!, 
    dest: Appendable!
): Appendable!
```

Writes the normalized form of the source string to the destination Appendable and returns the destination Appendable. The source and destination strings must be different objects.

Any [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) is wrapped into a [android.icu.util.ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException.html#).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:source string |
| `dest` | [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable.html#)!:destination Appendable; gets normalized src appended |

| Return ||
|------------------------------------------------------------------------------------------|------|
| [Appendable](https://developer.android.com/reference/kotlin/java/lang/Appendable.html#)! | dest |

### normalize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalize(
    src: CharSequence!, 
    dest: StringBuilder!
): StringBuilder!
```

Writes the normalized form of the source string to the destination string (replacing its contents) and returns the destination string. The source and destination strings must be different objects.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:source string |
| `dest` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:destination string; its contents is replaced with normalized src |

| Return ||
|------------------------------------------------------------------------------------------------|------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | dest |

### normalizeSecondAndAppend

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun normalizeSecondAndAppend(
    first: StringBuilder!, 
    second: CharSequence!
): StringBuilder!
```

Appends the normalized form of the second string to the first string (merging them at the boundary) and returns the first string. The result is normalized if the first string was normalized. The first and second strings must be different objects.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `first` | [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)!:string, should be normalized |
| `second` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:string, will be normalized |

| Return ||
|------------------------------------------------------------------------------------------------|-------|
| [StringBuilder](https://developer.android.com/reference/kotlin/java/lang/StringBuilder.html#)! | first |

### quickCheck

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun quickCheck(s: CharSequence!): Normalizer.QuickCheckResult!
```

Tests if the string is normalized. For the two COMPOSE modes, the result could be "maybe" in cases that would take a little more work to resolve definitively. Use spanQuickCheckYes() and normalizeSecondAndAppend() for a faster combination of quick check + normalization, to avoid re-checking the "yes" prefix.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:input string |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|------------------------|
| [Normalizer.QuickCheckResult](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer.QuickCheckResult)! | the quick check result |

### spanQuickCheckYes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun spanQuickCheckYes(s: CharSequence!): Int
```

Returns the end of the normalized substring of the input string. In other words, with`end=spanQuickCheckYes(s);`the substring`s.subSequence(0, end)`will pass the quick check with a "yes" result.

The returned end index is usually one or more characters before the "no" or "maybe" character: The end index is at a normalization boundary. (See the class documentation for more about normalization boundaries.)

When the goal is a normalized string and most input strings are expected to be normalized already, then call this method, and if it returns a prefix shorter than the input string, copy that prefix and use normalizeSecondAndAppend() for the remainder.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:input string |

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | "yes" span end index |
