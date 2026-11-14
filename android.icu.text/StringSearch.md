# StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringSearch

Kotlin| [Java](../android/icu/text/StringSearch.md) 
| --- | --- |

```
class StringSearch : SearchIterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.text.SearchIterator](../android/icu/text/SearchIterator.md) ||
| | ↳ | [android.icu.text.StringSearch](../android/icu/text/StringSearch.md) |

StringSearch is a [SearchIterator](../android/icu/text/SearchIterator.md) that provides language-sensitive text searching based on the comparison rules defined in a [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) object. StringSearch ensures that language eccentricity can be handled, e.g. for the German collator, characters ß and SS will be matched if case is chosen to be ignored. See the ["ICU Collation Design Document"](https://htmlpreview.github.io/?https://github.com/unicode-org/icu-docs/blob/main/design/collation/ICU_collation_design.htm) for more information.

There are 2 match options for selection: 
Let S' be the sub-string of a text string S between the offsets start and end \[start, end\]. 
A pattern string P matches a text string S at the offsets \[start, end\] if 

```kotlin
option 1. Some canonical equivalent of P matches some canonical equivalent
            of S'
  option 2. P matches S' and if P starts or ends with a combining mark,
            there exists no non-ignorable combining mark before or after S?
            in S respectively.
  
```
Option 2. is the default.

This search has APIs similar to that of other text iteration mechanisms such as the break iterators in [BreakIterator](../android/icu/text/BreakIterator.md). Using these APIs, it is easy to scan through text looking for all occurrences of a given pattern. This search iterator allows changing of direction by calling a [reset](../android/icu/text/StringSearch.md))followed by a [next](../android/icu/text/SearchIterator.md))or [previous](../android/icu/text/SearchIterator.md)). Though a direction change can occur without calling [reset](../android/icu/text/StringSearch.md))first, this operation comes with some speed penalty. Match results in the forward direction will match the result matches in the backwards direction in the reverse order

[SearchIterator](../android/icu/text/SearchIterator.md) provides APIs to specify the starting position within the text string to be searched, e.g. [setIndex](../android/icu/text/SearchIterator.md)), [preceding](../android/icu/text/SearchIterator.md))and [following](../android/icu/text/SearchIterator.md)). Since the starting position will be set as it is specified, please take note that there are some danger points at which the search may render incorrect results:

- In the midst of a substring that requires normalization.
- If the following match is to be found, the position should not be the second character which requires swapping with the preceding character. Vice versa, if the preceding match is to be found, the position to search from should not be the first character which requires swapping with the next character. E.g certain Thai and Lao characters require swapping.
- If a following pattern match is to be found, any position within a contracting sequence except the first will fail. Vice versa if a preceding pattern match is to be found, an invalid starting point would be any character within a contracting sequence except the last.

A [BreakIterator](../android/icu/text/BreakIterator.md) can be used if only matches at logical breaks are desired. Using a [BreakIterator](../android/icu/text/BreakIterator.md) will only give you results that exactly matches the boundaries given by the [BreakIterator](../android/icu/text/BreakIterator.md). For instance the pattern "e" will not be found in the string "\\u00e9" if a character break iterator is used.

Options are provided to handle overlapping matches. E.g. In English, overlapping matches produces the result 0 and 2 for the pattern "abab" in the text "ababab", where mutually exclusive matches only produces the result of 0.

Options are also provided to implement "asymmetric search" as described in [UTS #10 Unicode Collation Algorithm](http://www.unicode.org/reports/tr10/#Asymmetric_Search), specifically the ElementComparisonType values.

Though collator attributes will be taken into consideration while performing matches, there are no APIs here for setting and getting the attributes. These attributes can be set by getting the collator from [getCollator](../android/icu/text/StringSearch.md))and using the APIs in [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md). Lastly to update StringSearch to the new collator attributes, [reset](../android/icu/text/StringSearch.md))has to be called.

Restriction: 
Currently there are no composite characters that consists of a character with combining class \> 0 before a character with combining class == 0. However, if such a character exists in the future, StringSearch does not guarantee the results for option 1.

Consult the [SearchIterator](../android/icu/text/SearchIterator.md) documentation for information on and examples of how to use instances of this class to implement text searching.

Note, StringSearch is not to be subclassed.

## Summary

| Inherited constants ||
|---|---|
| From class [SearchIterator](../android/icu/text/SearchIterator.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](../android/icu/text/SearchIterator.md) <br /> DONE is returned by previous() and next() after all valid matches have been returned, and by first() and last() if there are no matches at all. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringSearch](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Initializes the iterator to use the language-specific rules and break iterator rules defined in the default locale to search for argument pattern in the argument target text. |
| [StringSearch](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`, `collator:` ` [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!`)` Initializes the iterator to use the language-specific rules defined in the argument collator to search for argument pattern in the argument target text. |
| [StringSearch](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`, `collator:` ` [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!`, `breakiter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`)` Initializes the iterator to use the language-specific rules defined in the argument collator to search for argument pattern in the argument target text. |
| [StringSearch](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Initializes the iterator to use the language-specific rules and break iterator rules defined in the argument locale to search for argument pattern in the argument target text. |
| [StringSearch](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`, `locale:` ` [Locale](../java/util/Locale.md)!`)` Initializes the iterator to use the language-specific rules and break iterator rules defined in the argument locale to search for argument pattern in the argument target text. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)! | [getCollator](../android/icu/text/StringSearch.md))`()` Gets the [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) used for the language rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../android/icu/text/StringSearch.md))`()` Return the current index in the text being searched. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPattern](../android/icu/text/StringSearch.md))`()` Returns the pattern for which StringSearch is searching for. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCanonical](../android/icu/text/StringSearch.md))`()` Determines whether canonical matches (option 1, as described in the class documentation) is set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../android/icu/text/StringSearch.md))`()` Resets the iteration. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCanonical](../android/icu/text/StringSearch.md))`(`allowCanonical:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the canonical match mode. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCollator](../android/icu/text/StringSearch.md))`(`collator:` ` [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!`)` Sets the [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) to be used for language-specific searching. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIndex](../android/icu/text/StringSearch.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the position in the target text at which the next search will start. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPattern](../android/icu/text/StringSearch.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the pattern to search for. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](../android/icu/text/StringSearch.md))`(`text:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`)` Set the target text to be searched. |

| Protected methods ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handleNext](../android/icu/text/StringSearch.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Abstract method which subclasses override to provide the mechanism for finding the next match in the target text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [handlePrevious](../android/icu/text/StringSearch.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Abstract method which subclasses override to provide the mechanism for finding the previous match in the target text. |

| Inherited functions ||
|---|---|
| From class [SearchIterator](../android/icu/text/SearchIterator.md) |-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [first](../android/icu/text/SearchIterator.md))`()` <br /> Returns the first index at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by [getIndex()](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to the index [DONE](../android/icu/text/SearchIterator.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [following](../android/icu/text/SearchIterator.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the first index equal or greater than position at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by [getIndex()](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to the index [DONE](../android/icu/text/SearchIterator.md). <br /> | | [BreakIterator](../android/icu/text/BreakIterator.md)! | [getBreakIterator](../android/icu/text/SearchIterator.md))`()` <br /> Returns the BreakIterator that is used to restrict the indexes at which matches are detected. This will be the same object that was passed to the constructor or to [setBreakIterator](../android/icu/text/SearchIterator.md)). If the [BreakIterator](../android/icu/text/BreakIterator.md) has not been set, null will be returned. See [setBreakIterator](../android/icu/text/SearchIterator.md))for more information. <br /> | | [SearchIterator.ElementComparisonType](../android/icu/text/SearchIterator.ElementComparisonType.md)! | [getElementComparisonType](../android/icu/text/SearchIterator.md))`()` <br /> Returns the collation element comparison type. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMatchLength](../android/icu/text/SearchIterator.md))`()` <br /> Returns the length of text in the string which matches the search pattern. This call returns a valid result only after a successful call to [first](../android/icu/text/SearchIterator.md)), [next](../android/icu/text/SearchIterator.md)), [previous](../android/icu/text/SearchIterator.md)), or [last](../android/icu/text/SearchIterator.md)). Just after construction, or after a searching method returns [DONE](../android/icu/text/SearchIterator.md), this method will return 0. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMatchStart](../android/icu/text/SearchIterator.md))`()` <br /> Returns the index to the match in the text string that was searched. This call returns a valid result only after a successful call to [first](../android/icu/text/SearchIterator.md)), [next](../android/icu/text/SearchIterator.md)), [previous](../android/icu/text/SearchIterator.md)), or [last](../android/icu/text/SearchIterator.md)). Just after construction, or after a searching method returns [DONE](../android/icu/text/SearchIterator.md), this method will return [DONE](../android/icu/text/SearchIterator.md). Use [getMatchLength](../android/icu/text/SearchIterator.md))to get the matched string length. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMatchedText](../android/icu/text/SearchIterator.md))`()` <br /> Returns the text that was matched by the most recent call to [first](../android/icu/text/SearchIterator.md)), [next](../android/icu/text/SearchIterator.md)), [previous](../android/icu/text/SearchIterator.md)), or [last](../android/icu/text/SearchIterator.md)). If the iterator is not pointing at a valid match (e.g. just after construction or after [DONE](../android/icu/text/SearchIterator.md) has been returned, returns an empty string. <br /> | | [CharacterIterator](../java/text/CharacterIterator.md)! | [getTarget](../android/icu/text/SearchIterator.md))`()` <br /> Return the string text to be searched. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOverlapping](../android/icu/text/SearchIterator.md))`()` <br /> Return true if the overlapping property has been set. See [setOverlapping(boolean)](../android/icu/text/SearchIterator.md))for more information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [last](../android/icu/text/SearchIterator.md))`()` <br /> Returns the last index in the target text at which it matches the search pattern. The iterator is adjusted so that its current index (as returned by [getIndex](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to the index [DONE](../android/icu/text/SearchIterator.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [next](../android/icu/text/SearchIterator.md))`()` <br /> Returns the index of the next point at which the text matches the search pattern, starting from the current position The iterator is adjusted so that its current index (as returned by [getIndex](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to a position after the end of the text string. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [preceding](../android/icu/text/SearchIterator.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns the first index less than position at which the string text matches the search pattern. The iterator is adjusted so that its current index (as returned by [getIndex](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to the index [DONE](../android/icu/text/SearchIterator.md) When the overlapping option ([isOverlapping](../android/icu/text/SearchIterator.md))) is off, the last index of the result match is always less than position. When the overlapping option is on, the result match may span across position. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previous](../android/icu/text/SearchIterator.md))`()` <br /> Returns the index of the previous point at which the string text matches the search pattern, starting at the current position. The iterator is adjusted so that its current index (as returned by [getIndex](../android/icu/text/SearchIterator.md))) is the match position if one was found. If a match is not found, [DONE](../android/icu/text/SearchIterator.md) will be returned and the iterator will be adjusted to the index [DONE](../android/icu/text/SearchIterator.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBreakIterator](../android/icu/text/SearchIterator.md))`(`breakiter:` ` [BreakIterator](../android/icu/text/BreakIterator.md)!`)` <br /> Set the BreakIterator that will be used to restrict the points at which matches are detected. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setElementComparisonType](../android/icu/text/SearchIterator.md))`(`type:` ` [SearchIterator.ElementComparisonType](../android/icu/text/SearchIterator.ElementComparisonType.md)!`)` <br /> Sets the collation element comparison type. The default comparison type is [ElementComparisonType.STANDARD_ELEMENT_COMPARISON](../android/icu/text/SearchIterator.ElementComparisonType.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchLength](../android/icu/text/SearchIterator.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the length of the most recent match in the target text. Subclasses' handleNext() and handlePrevious() methods should call this after they find a match in the target text. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOverlapping](../android/icu/text/SearchIterator.md))`(`allowOverlap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Determines whether overlapping matches are returned. See the class documentation for more information about overlapping matches. The default setting of this property is false <br /> | ||

| Inherited properties ||
|---|---|
| From class [SearchIterator](../android/icu/text/SearchIterator.md) |--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [BreakIterator](../android/icu/text/BreakIterator.md)! | [breakIterator](../android/icu/text/SearchIterator.md) <br /> The BreakIterator to define the boundaries of a logical match. This value can be a null. See class documentation for more information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [matchLength](../android/icu/text/SearchIterator.md) <br /> Length of the most current match in target text. Value 0 is the default value. <br /> | | [CharacterIterator](../java/text/CharacterIterator.md)! | [targetText](../android/icu/text/SearchIterator.md) <br /> Target text for searching. <br /> | ||

## Public constructors

### StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringSearch(
    pattern: String!, 
    target: String!)
```

Initializes the iterator to use the language-specific rules and break iterator rules defined in the default locale to search for argument pattern in the argument target text.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:text to look for. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:target text to search for pattern. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0. ClassCastException thrown if the collator for the default locale is not a RuleBasedCollator. |

### StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringSearch(
    pattern: String!, 
    target: CharacterIterator!, 
    collator: RuleBasedCollator!)
```

Initializes the iterator to use the language-specific rules defined in the argument collator to search for argument pattern in the argument target text. No [BreakIterator](../android/icu/text/BreakIterator.md) s are set to test for logical matches.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:text to look for. |
| `target` | [CharacterIterator](../java/text/CharacterIterator.md)!:target text to search for pattern. |
| `collator` | [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!: [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) that defines the language rules |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0 |

**See Also**

- [android.icu.text.RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) 

### StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringSearch(
    pattern: String!, 
    target: CharacterIterator!, 
    collator: RuleBasedCollator!, 
    breakiter: BreakIterator!)
```

Initializes the iterator to use the language-specific rules defined in the argument collator to search for argument pattern in the argument target text. The argument`breakiter`is used to define logical matches. See super class documentation for more details on the use of the target text and [BreakIterator](../android/icu/text/BreakIterator.md).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:text to look for. |
| `target` | [CharacterIterator](../java/text/CharacterIterator.md)!:target text to search for pattern. |
| `collator` | [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!: [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) that defines the language rules |
| --- | --- |
| `breakiter` | [BreakIterator](../android/icu/text/BreakIterator.md)!:A [BreakIterator](../android/icu/text/BreakIterator.md) that is used to determine the boundaries of a logical match. This argument can be null. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0 |

**See Also**

- [android.icu.text.BreakIterator](../android/icu/text/BreakIterator.md)
- [android.icu.text.RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) 

### StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringSearch(
    pattern: String!, 
    target: CharacterIterator!, 
    locale: ULocale!)
```

Initializes the iterator to use the language-specific rules and break iterator rules defined in the argument locale to search for argument pattern in the argument target text. See super class documentation for more details on the use of the target text and [BreakIterator](../android/icu/text/BreakIterator.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:text to look for. |
| `target` | [CharacterIterator](../java/text/CharacterIterator.md)!:target text to search for pattern. |
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:locale to use for language and break iterator rules |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0. ClassCastException thrown if the collator for the specified locale is not a RuleBasedCollator. |

**See Also**

- [android.icu.text.BreakIterator](../android/icu/text/BreakIterator.md)
- [android.icu.text.RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)
- [android.icu.text.SearchIterator](../android/icu/text/SearchIterator.md) 

### StringSearch

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringSearch(
    pattern: String!, 
    target: CharacterIterator!, 
    locale: Locale!)
```

Initializes the iterator to use the language-specific rules and break iterator rules defined in the argument locale to search for argument pattern in the argument target text.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:text to look for. |
| `target` | [CharacterIterator](../java/text/CharacterIterator.md)!:target text to search for pattern. |
| `locale` | [Locale](../java/util/Locale.md)!:locale to use for language and break iterator rules |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown when argument target is null, or of length 0. ClassCastException thrown if the collator for the specified locale is not a RuleBasedCollator. |

## Public methods

### getCollator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCollator(): RuleBasedCollator!
```

Gets the [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) used for the language rules.

Since StringSearch depends on the returned [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md), any changes to the [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) result should follow with a call to either [reset()](../android/icu/text/StringSearch.md))or [setCollator(android.icu.text.RuleBasedCollator)](../android/icu/text/StringSearch.md))to ensure the correct search behavior.

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)! | [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) used by this StringSearch |

**See Also**

- [android.icu.text.RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)
- [#setCollator](../android/icu/text/StringSearch.md)) 

### getIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIndex(): Int
```

Return the current index in the text being searched. If the iteration has gone past the end of the text (or past the beginning for a backwards search), [DONE](../android/icu/text/SearchIterator.md) is returned.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | current index in the text being searched. |

### getPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPattern(): String!
```

Returns the pattern for which StringSearch is searching for.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern searched for |

### isCanonical

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCanonical(): Boolean
```

Determines whether canonical matches (option 1, as described in the class documentation) is set. See setCanonical(boolean) for more information.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if canonical matches is set, false otherwise |

**See Also**

- [#setCanonical](../android/icu/text/StringSearch.md)) 

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Unit
```

Resets the iteration. Search will begin at the start of the text string if a forward iteration is initiated before a backwards iteration. Otherwise if a backwards iteration is initiated before a forwards iteration, the search will begin at the end of the text string. 

### setCanonical

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCanonical(allowCanonical: Boolean): Unit
```

Set the canonical match mode. See class documentation for details. The default setting for this property is false.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `allowCanonical` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):flag indicator if canonical matches are allowed |

**See Also**

- [#isCanonical](../android/icu/text/StringSearch.md)) 

### setCollator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setCollator(collator: RuleBasedCollator!): Unit
```

Sets the [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) to be used for language-specific searching.

The iterator's position will not be changed by this method.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `collator` | [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md)!:to use for this StringSearch |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | thrown when collator is null |

**See Also**

- [#getCollator](../android/icu/text/StringSearch.md)) 

### setIndex

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIndex(position: Int): Unit
```

Sets the position in the target text at which the next search will start. This method clears any previous match.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):position from which to start the next search |

### setPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPattern(pattern: String!): Unit
```

Set the pattern to search for. The iterator's position will not be changed by this method.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:for searching |

**See Also**

- [#getPattern](../android/icu/text/StringSearch.md))

| Exceptions ||
|--------------------------------------|------------------------------------------|
| `java.lang.IllegalArgumentException` | thrown if pattern is null or of length 0 |

### setTarget

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTarget(text: CharacterIterator!): Unit
```

Set the target text to be searched. Text iteration will then begin at the start of the text string. This method is useful if you want to reuse an iterator to search within a different body of text.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharacterIterator](../java/text/CharacterIterator.md)!:new text iterator to look for match, |

## Protected methods

### handleNext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun handleNext(position: Int): Int
```

Abstract method which subclasses override to provide the mechanism for finding the next match in the target text. This allows different subclasses to provide different search algorithms.

If a match is found, the implementation should return the index at which the match starts and should call [setMatchLength](../android/icu/text/SearchIterator.md))with the number of characters in the target text that make up the match. If no match is found, the method should return [DONE](../android/icu/text/SearchIterator.md).

| Parameters ||
|---------|----------------------------------------------------------------|
| `start` | The index in the target text at which the search should start. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | index at which the match starts, else if match is not found [DONE](../android/icu/text/SearchIterator.md) is returned |

### handlePrevious

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun handlePrevious(position: Int): Int
```

Abstract method which subclasses override to provide the mechanism for finding the previous match in the target text. This allows different subclasses to provide different search algorithms.

If a match is found, the implementation should return the index at which the match starts and should call [setMatchLength](../android/icu/text/SearchIterator.md))with the number of characters in the target text that make up the match. If no match is found, the method should return [DONE](../android/icu/text/SearchIterator.md).

| Parameters ||
|-----------|----------------------------------------------------------------|
| `startAt` | The index in the target text at which the search should start. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | index at which the match starts, else if match is not found [DONE](../android/icu/text/SearchIterator.md) is returned |
