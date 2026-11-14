# Normalizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Normalizer

```
class Normalizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.text.Normalizer](https://developer.android.com/reference/kotlin/java/text/Normalizer#) |

This class provides the method`normalize`which transforms Unicode text into an equivalent composed or decomposed form, allowing for easier sorting and searching of text. The`normalize`method supports the standard normalization forms described in [Unicode Standard Annex #15 --- Unicode Normalization Forms](https://www.unicode.org/reports/tr15/).

Characters with accents or other adornments can be encoded in several different ways in Unicode. For example, take the character A-acute. In Unicode, this can be encoded as a single character (the "composed" form): 

```kotlin
U+00C1    LATIN CAPITAL LETTER A WITH ACUTE
```
or as two separate characters (the "decomposed" form): 

```kotlin
U+0041    LATIN CAPITAL LETTER A
       U+0301    COMBINING ACUTE ACCENT
```
To a user of your program, however, both of these sequences should be treated as the same "user-level" character "A with acute accent". When you are searching or comparing text, you must ensure that these two sequences are treated as equivalent. In addition, you must handle characters with more than one accent. Sometimes the order of a character's combining accents is significant, while in other cases accent sequences in different orders are really equivalent.

Similarly, the string "ffi" can be encoded as three separate letters: 

```kotlin
U+0066    LATIN SMALL LETTER F
       U+0066    LATIN SMALL LETTER F
       U+0069    LATIN SMALL LETTER I
```
or as the single character 

```kotlin
U+FB03    LATIN SMALL LIGATURE FFI
```
The ffi ligature is not a distinct semantic character, and strictly speaking it shouldn't be in Unicode at all, but it was included for compatibility with existing character sets that already provided it. The Unicode standard identifies such characters by giving them "compatibility" decompositions into the corresponding semantic characters. When sorting and searching, you will often want to use these mappings.

The`normalize`method helps solve these problems by transforming text into the canonical composed and decomposed forms as shown in the first example above. In addition, you can have it perform compatibility decompositions so that you can treat compatibility characters the same as their equivalents. Finally, the`normalize`method rearranges accents into the proper canonical order, so that you do not have to worry about accent rearrangement on your own.

The W3C generally recommends to exchange texts in NFC. Note also that most legacy character encodings use only precomposed forms and often do not encode any combining marks by themselves. For conversion to such character encodings the Unicode text needs to be normalized to NFC. For more usage examples, see the Unicode Standard Annex.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Form](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form) This enum provides constants of the four Unicode normalization forms that are described in [Unicode Standard Annex #15 --- Unicode Normalization Forms](https://www.unicode.org/reports/tr15/) and two methods to access them. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNormalized](https://developer.android.com/reference/kotlin/java/text/Normalizer#isNormalized(kotlin.CharSequence,%20java.text.Normalizer.Form))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `form:` ` [Normalizer.Form](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form)!`)` Determines if the given sequence of char values is normalized. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [normalize](https://developer.android.com/reference/kotlin/java/text/Normalizer#normalize(kotlin.CharSequence,%20java.text.Normalizer.Form))`(`src:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `form:` ` [Normalizer.Form](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form)!`)` Normalize a sequence of char values. |

## Public methods

### isNormalized

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isNormalized(
    src: CharSequence!, 
    form: Normalizer.Form!
): Boolean
```

Determines if the given sequence of char values is normalized.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The sequence of char values to be checked. |
| `form` | [Normalizer.Form](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form)!:The normalization form; one of [java.text.Normalizer.Form#NFC](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFD](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFKC](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFKD](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the sequence of char values is normalized; false otherwise. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | If`src`or`form`is null. |

### normalize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun normalize(
    src: CharSequence!, 
    form: Normalizer.Form!
): String!
```

Normalize a sequence of char values. The sequence will be normalized according to the specified normalization form.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The sequence of char values to normalize. |
| `form` | [Normalizer.Form](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form)!:The normalization form; one of [java.text.Normalizer.Form#NFC](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFD](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFKC](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form), [java.text.Normalizer.Form#NFKD](https://developer.android.com/reference/kotlin/java/text/Normalizer.Form) |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The normalized String |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | If`src`or`form`is null. |
