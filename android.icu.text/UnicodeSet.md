Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnicodeSet

```
open class UnicodeSet : UnicodeFilter, Comparable<UnicodeSet!>, Freezable<UnicodeSet!>, MutableIterable<String!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.text.UnicodeFilter](UnicodeFilter.md) ||
| | ↳ | [android.icu.text.UnicodeSet](UnicodeSet.md) |

A mutable set of Unicode characters and multicharacter strings. Objects of this class represent *character classes* used in regular expressions. A character specifies a subset of Unicode code points. Legal code points are U+0000 to U+10FFFF, inclusive. Note: method freeze() will not only make the set immutable, but also makes important methods much higher performance: contains(c), containsNone(...), span(...), spanBack(...) etc. After the object is frozen, any subsequent call that wants to change the object will throw UnsupportedOperationException.

The UnicodeSet class is not designed to be subclassed.

`UnicodeSet` supports two APIs. The first is the *operand* API that allows the caller to modify the value of a `UnicodeSet` object. It conforms to Java 2's `java.util.Set` interface, although `UnicodeSet` does not actually implement that interface. All methods of `Set` are supported, with the modification that they take a character range or single character instead of an `Object`, and they take a `UnicodeSet` instead of a `Collection`. The operand API may be thought of in terms of boolean logic: a boolean OR is implemented by `add`, a boolean AND is implemented by `retain`, a boolean XOR is implemented by `complement` taking an argument, and a boolean NOT is implemented by `complement` with no argument. In terms of traditional set theory function names, `add` is a union, `retain` is an intersection, `remove` is an asymmetric difference, and `complement` with no argument is a set complement with respect to the superset range `MIN_VALUE-MAX_VALUE`

The second API is the `applyPattern()`/`toPattern()` API from the `java.text.Format`-derived classes. Unlike the methods that add characters, add categories, and control the logic of the set, the method `applyPattern()` sets all attributes of a `UnicodeSet` at once, based on a string pattern.

**Pattern syntax**
Patterns are accepted by the constructors and the `applyPattern()` methods and returned by the `toPattern()` method. These patterns follow a syntax similar to that employed by version 8 regular expression character classes. Here are some simple examples:

| `[]` | No characters |
| --- | --- |
| `[a]` | The character 'a' |
| `[ae]` | The characters 'a' and 'e' |
| `[a-e]` | The characters 'a' through 'e' inclusive, in Unicode code point order |
| --- | --- |
| `[\\u4E01]` | The character U+4E01 |
| `[a{ab}{ac}]` | The character 'a' and the multicharacter strings "ab" and "ac" |
| `[\p{Lu}]` | All characters in the general category Uppercase Letter |
| --- | --- |

Any character may be preceded by a backslash in order to remove any special meaning. White space characters, as defined by the Unicode Pattern_White_Space property, are ignored, unless they are escaped.

Property patterns specify a set of characters having a certain property as defined by the Unicode standard. Both the POSIX-like "\[:Lu:\]" and the Perl-like syntax "\\p{Lu}" are recognized. For a complete list of supported property patterns, see the User's Guide for UnicodeSet at <https://unicode-org.github.io/icu/userguide/strings/unicodeset>. Actual determination of property data is defined by the underlying Unicode database as implemented by UCharacter.

Patterns specify individual characters, ranges of characters, and Unicode property sets. When elements are concatenated, they specify their union. To complement a set, place a '\^' immediately after the opening '\['. Property patterns are inverted by modifying their delimiters; "\[:\^foo\]" and "\\P{foo}". In any other location, '\^' has no special meaning.

Since ICU 70, "\[\^...\]", "\[:\^foo\]", "\\P{foo}", and "\[:binaryProperty=No:\]" perform a "code point complement" (all code points minus the original set), removing all multicharacter strings, equivalent to .complement.removeAllStrings . The complement API function continues to perform a symmetric difference with all code points and thus retains all multicharacter strings.

Ranges are indicated by placing two a '-' between two characters, as in "a-z". This specifies the range of all characters from the left to the right, in Unicode order. If the left character is greater than or equal to the right character it is a syntax error. If a '-' occurs as the first character after the opening '\[' or '\[\^', or if it occurs as the last character before the closing '\]', then it is taken as a literal. Thus "\[a\\\\-b\]", "\[-ab\]", and "\[ab-\]" all indicate the same set of three characters, 'a', 'b', and '-'.

Sets may be intersected using the '\&' operator or the asymmetric set difference may be taken using the '-' operator, for example, "\[\[:L:\]\&\[\\\\u0000-\\\\u0FFF\]\]" indicates the set of all Unicode letters with values less than 4096. Operators ('\&' and '|') have equal precedence and bind left-to-right. Thus "\[\[:L:\]-\[a-z\]-\[\\\\u0100-\\\\u01FF\]\]" is equivalent to "\[\[\[:L:\]-\[a-z\]\]-\[\\\\u0100-\\\\u01FF\]\]". This only really matters for difference; intersection is commutative.
| --- | --- |

| `[a]` | The set containing 'a' |
| --- | --- |
| `[a-z]` | The set containing 'a' through 'z' and all letters in between, in Unicode order |
| `[^a-z]` | The set containing all characters but 'a' through 'z', that is, U+0000 through 'a'-1 and 'z'+1 through U+10FFFF |
| `[[pat1][pat2]]` | The union of sets specified by *pat1* and *pat2* |
| --- | --- |
| `[[pat1]&[pat2]]` | The intersection of sets specified by *pat1* and *pat2* |
| `[[pat1]-[pat2]]` | The asymmetric difference of sets specified by *pat1* and *pat2* |
| `[:Lu:] or \p{Lu}` | The set of characters having the specified Unicode property; in this case, Unicode uppercase letters |
| --- | --- |
| `[:^Lu:] or \P{Lu}` | The set of characters *not* having the given Unicode property |

**Formal syntax**

| `pattern := ` | `('[' '^'? item* ']') | property` |
| --- | --- | --- |
| `item := ` | `char | (char '-' char) | pattern-expr ` |
| `pattern-expr := ` | `pattern | pattern-expr pattern | pattern-expr op pattern ` |
| `op := ` | `'&' | '-' ` |
| --- | --- | --- |
| `special := ` | `'[' | ']' | '-' ` |
| `char := ` | *any character that is not* ` special | ('\\' `*any character* `) | ('\u' hex hex hex hex) ` |
| `hex := ` | `'0' | '1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9' | 'A' | 'B' | 'C' | 'D' | 'E' | 'F' | 'a' | 'b' | 'c' | 'd' | 'e' | 'f'` |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `property := ` | *a Unicode property set pattern* |

<br />

| Legend: |---|---|---| | `a := b` | | `a` may be replaced by `b` | | `a?` | | zero or one instance of `a` | | `a*` | | one or more instances of `a` | | `a | b` | | either `a` or `b` | | `'a'` | | the literal string between the quotes | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

To iterate over contents of `UnicodeSet`, the following are available:

- to iterate over the ranges: ranges, rangeStream
- to iterate over the strings: strings, stringStream
- to iterate over the code points: codePoints, codePointStream
- to iterate over the entire contents in a single loop: this class itself is `https://developer.android.com/reference/kotlin/java/lang/Iterable.html#`, or use stream. 
 All of these method are, however, not particularly efficient, since they convert each individual code point to a `String`.

The iterators and streams methods work as expected in idiomatic Java usage. 
The UnicodeSetIterator cannot be used in **for** loops, and it is not very Java-idiomatic, because it is old. But it might be faster in certain use cases. We recommend that you measure in performance sensitive code. 

To replace, count elements, or delete spans, see UnicodeSetSpanner.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.ComparisonStyle` Comparison style enums used by compareTo. |
| open | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange` A struct-like class used for iteration through ranges, for faster iteration than by String. |
| | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.SpanCondition` Argument values for whether span() and similar functions continue while the current character is contained vs. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ADD_CASE_MAPPINGS:kotlin.Int` Adds all case mappings for each element in the set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE:kotlin.Int` Alias for `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int` Enable case insensitive matching. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#IGNORE_SPACE:kotlin.Int` Bitmask for constructor and applyPattern() indicating that white space should be ignored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#MAX_VALUE:kotlin.Int` Maximum value that can be stored in a UnicodeSet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#MIN_VALUE:kotlin.Int` Minimum value that can be stored in a UnicodeSet. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#SIMPLE_CASE_INSENSITIVE:kotlin.Int` Enable case insensitive matching. |

| Public constructors ||
|---|---|
| UnicodeSet Constructs an empty set. |
| UnicodeSet Constructs a copy of an existing set. |
| UnicodeSet Constructs a set containing the given range. |
| UnicodeSet Quickly constructs a set from a set of ranges \<s0, e0, s1, e1, s2, e2, . |
| UnicodeSet Constructs a set from the given pattern. |
| UnicodeSet Constructs a set from the given pattern. |
| UnicodeSet Constructs a set from the given pattern. |
| UnicodeSet Constructs a set from the given pattern. |
| UnicodeSet Constructs a set from the given pattern. |

| Public methods ||
|---|---|
| open [StringBuffer](../java.lang/StringBuffer.md)! | _generatePattern Generate and append a string representation of this set to result. |
| open [StringBuffer](../java.lang/StringBuffer.md)! | _generatePattern Generate and append a string representation of this set to result. |
| [UnicodeSet](UnicodeSet.md)! | add Adds the specified character to this set if it is not already present. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | add Adds the specified range to this set if it is not already present. |
| [UnicodeSet](UnicodeSet.md)! | add Adds the specified multicharacter to this set if it is not already present. |
| open [UnicodeSet](UnicodeSet.md)! | add Add the contents of the collection (as strings) into this UnicodeSet. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | addAll Adds all of the elements in the specified set to this set if they're not already present. |
| open [UnicodeSet](UnicodeSet.md)! | addAll Adds all characters in range (uses preferred naming convention). |
| [UnicodeSet](UnicodeSet.md)! | addAll Adds each of the characters in this string to the set. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | addAll Add a collection (as strings) into this UnicodeSet. |
| open [UnicodeSet](UnicodeSet.md)! | addAll <br /> |
| open T | addAllTo Add the contents of the UnicodeSet (as strings) into a collection. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addMatchSetTo Implementation of UnicodeMatcher API. |
| open [UnicodeSet](UnicodeSet.md)! | applyIntPropertyValue Modifies this set to contain those code points which have the given value for the given binary or enumerated property, as returned by UCharacter. |
| [UnicodeSet](UnicodeSet.md)! | applyPattern Modifies this set to represent the set specified by the given pattern. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | applyPattern Modifies this set to represent the set specified by the given pattern, optionally ignoring whitespace. |
| open [UnicodeSet](UnicodeSet.md)! | applyPattern Modifies this set to represent the set specified by the given pattern, optionally ignoring whitespace. |
| open [UnicodeSet](UnicodeSet.md)! | applyPropertyAlias Modifies this set to contain those code points which have the given value for the given property. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | applyPropertyAlias Modifies this set to contain those code points which have the given value for the given property. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | charAt Returns the character at the given index within this set, where the set is ordered by ascending code point. |
| open [UnicodeSet](UnicodeSet.md)! | clear Removes all of the elements from this set. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Return a new set that is equivalent to this one. |
| open [UnicodeSet](UnicodeSet.md)! | cloneAsThawed Clone a thawed version of this class, according to the Freezable interface. |
| open [UnicodeSet](UnicodeSet.md)! | closeOver Close this set over the given attribute. |
| --- | --- |
| open [IntStream](../java.util.stream/IntStream.md)! | codePointStream Returns an `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` of Unicode code point values from this `UnicodeSet`. |
| open [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>! | codePoints Returns an `https://developer.android.com/reference/kotlin/java/lang/Iterable.html#` for iteration over all the code points in this set. |
| open [UnicodeSet](UnicodeSet.md)! | compact Reallocate this objects internal structures to take up the least possible space, without changing this object's value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares UnicodeSets, where shorter come first, and otherwise lexicographically (according to the comparison of the first characters that differ). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares UnicodeSets, in three different ways. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo <br /> |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | complement This is equivalent to `complement(MIN_VALUE, MAX_VALUE)`. |
| [UnicodeSet](UnicodeSet.md)! | complement Complements the specified character in this set. |
| open [UnicodeSet](UnicodeSet.md)! | complement Complements the specified range in this set. |
| --- | --- |
| [UnicodeSet](UnicodeSet.md)! | complement Complement the specified string in this set. |
| open [UnicodeSet](UnicodeSet.md)! | complementAll Complements in this set all elements contained in the specified set. |
| [UnicodeSet](UnicodeSet.md)! | complementAll Complement EACH of the characters in this string. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns true if this set contains the given character. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns true if this set contains every character of the given range. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns `true` if this set contains the given multicharacter string. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsAll Returns true if this set contains all the characters and strings of the given set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsAll <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsAll Returns true if there is a partition of the string such that this set contains each of the partitioned strings. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsNone Returns true if none of the characters or strings in this UnicodeSet appears in the string. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsNone Returns true if this set contains none of the characters of the given range. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsNone Returns true if this set contains none of the characters of the given string. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsNone <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsSome Returns true if this set contains one or more of the characters and strings of the given set. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsSome Returns true if this set contains one or more of the characters in the given range. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsSome Returns true if this set contains one or more of the characters of the given string. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | containsSome <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares the specified object with this set for equality. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | freeze Freeze this class, according to the Freezable interface. |
| open static [UnicodeSet](UnicodeSet.md)! | from Makes a set from a multicharacter string. |
| open static [UnicodeSet](UnicodeSet.md)! | fromAll Makes a set from each of the characters in the string. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRangeCount Iteration method that returns the number of ranges contained in this set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRangeEnd Iteration method that returns the last character in the specified range of this set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRangeStart Iteration method that returns the first character in the specified range of this set. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasStrings <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns the hash code value for this set. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | indexOf Returns the index of the given character within this set, where the set is ordered by ascending code point. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Returns `true` if this set contains no elements. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFrozen Is this frozen, according to the Freezable interface? |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | iterator Returns a string iterator. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | matches Implementation of UnicodeMatcher. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | matchesIndexValue Implementation of UnicodeMatcher API. |
| open [Stream](../java.util.stream/Stream.md)\< [UnicodeSet.EntryRange](../android/icu/text/UnicodeSet.EntryRange.md)!\>! | rangeStream Returns a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange` values from this `UnicodeSet`. |
| --- | --- |
| open [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [UnicodeSet.EntryRange](../android/icu/text/UnicodeSet.EntryRange.md)!\>! | ranges Provide for faster iteration than by String. |
| [UnicodeSet](UnicodeSet.md)! | remove Removes the specified character from this set if it is present. |
| open [UnicodeSet](UnicodeSet.md)! | remove Removes the specified range from this set if it is present. |
| --- | --- |
| [UnicodeSet](UnicodeSet.md)! | remove Removes the specified string from this set if it is present. |
| open [UnicodeSet](UnicodeSet.md)! | removeAll Removes from this set all of its elements that are contained in the specified set. |
| [UnicodeSet](UnicodeSet.md)! | removeAll Remove EACH of the characters in this string. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | removeAll <br /> |
| [UnicodeSet](UnicodeSet.md)! | removeAllStrings Remove all strings from this UnicodeSet |
| [UnicodeSet](UnicodeSet.md)! | retain Retain the specified character from this set if it is present. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | retain Retain only the elements in this set that are contained in the specified range. |
| [UnicodeSet](UnicodeSet.md)! | retain Retain the specified string in this set if it is present. |
| open [UnicodeSet](UnicodeSet.md)! | retainAll Retains only the elements in this set that are contained in the specified set. |
| --- | --- |
| [UnicodeSet](UnicodeSet.md)! | retainAll Retains EACH of the characters in this string. |
| open [UnicodeSet](UnicodeSet.md)! | retainAll <br /> |
| open [UnicodeSet](UnicodeSet.md)! | set Make this object represent the same set as `other`. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | set Make this object represent the range `start - end`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | size Returns the number of elements in this set (its cardinality) Note than the elements of a set may include both individual codepoints and strings. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | span Span a string using this UnicodeSet. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | span Span a string using this UnicodeSet. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | spanBack Span a string backwards (from the end) using this UnicodeSet. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | spanBack Span a string backwards (from the fromIndex) using this UnicodeSet. |
| --- | --- |
| open [Stream](../java.util.stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | stream Returns a stream of `String` values from this `UnicodeSet`. |
| open [Stream](../java.util.stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | stringStream Returns a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `String` values from this `UnicodeSet`. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | strings For iterating through the strings in the set. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | toPattern Returns a string representation of this set. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Return a programmer-readable string representation of this object. |

| Properties ||
|---|---|
| static [UnicodeSet](UnicodeSet.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ALL_CODE_POINTS:android.icu.text.UnicodeSet` Constant for the set of all code points. |
| static [UnicodeSet](UnicodeSet.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#EMPTY:android.icu.text.UnicodeSet` Constant for the empty set. |

## Constants

### ADD_CASE_MAPPINGS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADD_CASE_MAPPINGS: Int
```

Adds all case mappings for each element in the set. This adds the full lower-, title-, and uppercase mappings as well as the full case folding of each existing element in the set.

This value is an options bit set value for some constructors, applyPattern(), and closeOver(). It can be ORed together with other, unrelated options.

Unlike the "case insensitive" options, this does not perform a closure. For example, it does not add 'ſ' (U+017F long s) for 's', 'K' (U+212A Kelvin sign) for 'k', or replace set strings by their case-folded versions.

 Value: 4

### CASE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE: Int
```

**Deprecated:** *ICU 73 Use `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int` instead.*

Alias for `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`.

 Value: 2

### CASE_INSENSITIVE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_INSENSITIVE: Int
```

Enable case insensitive matching. E.g., "\[ab\]" with this flag will match 'a', 'A', 'b', and 'B'. "\[\^ab\]" with this flag will match all except 'a', 'A', 'b', and 'B'. This performs a full closure over case mappings, e.g. 'ſ' (U+017F long s) for 's'.

This value is an options bit set value for some constructors, applyPattern(), and closeOver(). It can be ORed together with other, unrelated options.

The resulting set is a superset of the input for the code points but not for the strings. It performs a case mapping closure of the code points and adds full case folding strings for the code points, and reduces strings of the original set to their full case folding equivalents.

This is designed for case-insensitive matches, for example in regular expressions. The full code point case closure allows checking of an input character directly against the closure set. Strings are matched by comparing the case-folded form from the closure set with an incremental case folding of the string in question.

The closure set will also contain single code points if the original set contained case-equivalent strings (like U+00DF for "ss" or "Ss" etc.). This is not necessary (that is, redundant) for the above matching method but results in the same closure sets regardless of whether the original set contained the code point or a string.

 Value: 2

### IGNORE_SPACE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IGNORE_SPACE: Int
```

Bitmask for constructor and applyPattern() indicating that white space should be ignored. If set, ignore Unicode Pattern_White_Space characters, unless they are quoted or escaped. This may be ORed together with other selectors.

 Value: 1

### MAX_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_VALUE: Int
```

Maximum value that can be stored in a UnicodeSet.

 Value: 1114111

### MIN_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_VALUE: Int
```

Minimum value that can be stored in a UnicodeSet.

 Value: 0

### SIMPLE_CASE_INSENSITIVE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIMPLE_CASE_INSENSITIVE: Int
```

Enable case insensitive matching. Same as `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int` but using only Simple_Case_Folding (scf) mappings, which map each code point to one code point, not full Case_Folding (cf) mappings, which map some code points to multiple code points.

This is designed for case-insensitive matches, for example in certain regular expression implementations where only Simple_Case_Folding mappings are used, such as in ECMAScript (JavaScript) regular expressions.

This value is an options bit set value for some constructors, applyPattern(), and closeOver(). It can be ORed together with other, unrelated options.

 Value: 6

## Public constructors

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet()
```

Constructs an empty set.

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(other: UnicodeSet!)
```

Constructs a copy of an existing set.

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(
    start: Int, 
    end: Int)
```

Constructs a set containing the given range. If `end > start` then an empty set is created.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of range |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(vararg pairs: Int)
```

Quickly constructs a set from a set of ranges \<s0, e0, s1, e1, s2, e2, ..., sn, en\>. There must be an even number of integers, and they must be all greater than zero, all less than or equal to Character.MAX_CODE_POINT. In each pair (..., si, ei, ...) it must be true that si \<= ei Between adjacent pairs (...ei, sj...), it must be true that ei+1 \< sj

| Parameters ||
|---|---|
| `pairs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): pairs of character representing ranges |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(pattern: String!)
```

Constructs a set from the given pattern. See the class description for the syntax of the pattern language. Whitespace is ignored.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(
    pattern: String!, 
    ignoreWhitespace: Boolean)
```

Constructs a set from the given pattern. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `ignoreWhitespace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, ignore Unicode Pattern_White_Space characters |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(
    pattern: String!, 
    options: Int)
```

Constructs a set from the given pattern. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a bitmask indicating which options to apply. Valid options are `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#IGNORE_SPACE:kotlin.Int` and at most one of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ADD_CASE_MAPPINGS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#SIMPLE_CASE_INSENSITIVE:kotlin.Int`. These case options are mutually exclusive. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(
    pattern: String!, 
    pos: ParsePosition!, 
    symbols: SymbolTable!)
```

Constructs a set from the given pattern. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `pos` | [ParsePosition](../java.text/ParsePosition.md)!: on input, the position in pattern at which to start parsing. On output, the position after the last character parsed. |
| `symbols` | [SymbolTable](SymbolTable.md)!: a symbol table mapping variables to char\[\] arrays and chars to UnicodeSets |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### UnicodeSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnicodeSet(
    pattern: String!, 
    pos: ParsePosition!, 
    symbols: SymbolTable!, 
    options: Int)
```

Constructs a set from the given pattern. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `pos` | [ParsePosition](../java.text/ParsePosition.md)!: on input, the position in pattern at which to start parsing. On output, the position after the last character parsed. |
| `symbols` | [SymbolTable](SymbolTable.md)!: a symbol table mapping variables to char\[\] arrays and chars to UnicodeSets |
| --- | --- |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a bitmask indicating which options to apply. Valid options are `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#IGNORE_SPACE:kotlin.Int` and at most one of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ADD_CASE_MAPPINGS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#SIMPLE_CASE_INSENSITIVE:kotlin.Int`. These case options are mutually exclusive. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

## Public methods

### _generatePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun _generatePattern(
    result: StringBuffer!, 
    escapeUnprintable: Boolean
): StringBuffer!
```

Generate and append a string representation of this set to result. This does not use this.pat, the cleaned up copy of the string passed to applyPattern().

| Parameters ||
|---|---|
| `result` | [StringBuffer](../java.lang/StringBuffer.md)!: the buffer into which to generate the pattern |
| `escapeUnprintable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): escape unprintable characters if true |

### _generatePattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun _generatePattern(
    result: StringBuffer!, 
    escapeUnprintable: Boolean, 
    includeStrings: Boolean
): StringBuffer!
```

Generate and append a string representation of this set to result. This does not use this.pat, the cleaned up copy of the string passed to applyPattern().

| Parameters ||
|---|---|
| `result` | [StringBuffer](../java.lang/StringBuffer.md)!: the buffer into which to generate the pattern |
| `escapeUnprintable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): escape unprintable characters if true |
| `includeStrings` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if false, doesn't include the strings. |
| --- | --- |

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun add(c: Int): UnicodeSet!
```

Adds the specified character to this set if it is not already present. If this set already contains the specified character, the call leaves this set unchanged.

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(
    start: Int, 
    end: Int
): UnicodeSet!
```

Adds the specified range to this set if it is not already present. If this set already contains the specified range, the call leaves this set unchanged. If `start > end` then an empty range is added, leaving the set unchanged.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of range to be added to this set. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of range to be added to this set. |

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun add(s: CharSequence!): UnicodeSet!
```

Adds the specified multicharacter to this set if it is not already present. If this set already contains the multicharacter, the call leaves this set unchanged. Thus "ch" =\> {"ch"}

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(source: MutableIterable<*>!): UnicodeSet!
```

Add the contents of the collection (as strings) into this UnicodeSet. The collection must not contain null.

| Parameters ||
|---|---|
| `source` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\<\*\>!: the collection to add |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this object |

### addAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(c: UnicodeSet!): UnicodeSet!
```

Adds all of the elements in the specified set to this set if they're not already present. This operation effectively modifies this set so that its value is the *union* of the two sets. The behavior of this operation is unspecified if the specified collection is modified while the operation is in progress.

| Parameters ||
|---|---|
| `c` | [UnicodeSet](UnicodeSet.md)!: set whose elements are to be added to this set. |

### addAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(
    start: Int, 
    end: Int
): UnicodeSet!
```

Adds all characters in range (uses preferred naming convention).

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of where to start on adding all characters. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of where to end on adding all characters. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this object |

### addAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addAll(s: CharSequence!): UnicodeSet!
```

Adds each of the characters in this string to the set. Thus "ch" =\> {"c", "h"} If this set already any particular character, it has no effect on that character.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### addAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(source: MutableIterable<*>!): UnicodeSet!
```

Add a collection (as strings) into this UnicodeSet. Uses standard naming convention.

| Parameters ||
|---|---|
| `source` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\<\*\>!: collection to add into |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this object |

### addAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : CharSequence!> addAll(vararg collection: T): UnicodeSet!
```
**See Also**

- addAll

### addAllTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : MutableCollection<String!>!> addAllTo(target: T): T
```

Add the contents of the UnicodeSet (as strings) into a collection.

| Parameters ||
|---|---|
| `target` | T: collection to add into |

### addMatchSetTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addMatchSetTo(toUnionTo: UnicodeSet!): Unit
```

Implementation of UnicodeMatcher API. Union the set of all characters that may be matched by this object into the given set.

| Parameters ||
|---|---|
| `toUnionTo` | [UnicodeSet](UnicodeSet.md)!: the set into which to union the source characters |

### applyIntPropertyValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyIntPropertyValue(
    prop: Int, 
    value: Int
): UnicodeSet!
```

Modifies this set to contain those code points which have the given value for the given binary or enumerated property, as returned by UCharacter.getIntPropertyValue. Prior contents of this set are lost.

| Parameters ||
|---|---|
| `prop` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a property in the range UProperty.BIN_START..UProperty.BIN_LIMIT-1 or UProperty.INT_START..UProperty.INT_LIMIT-1 or. UProperty.MASK_START..UProperty.MASK_LIMIT-1. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a value in the range UCharacter.getIntPropertyMinValue(prop).. UCharacter.getIntPropertyMaxValue(prop), with one exception. If prop is UProperty.GENERAL_CATEGORY_MASK, then value should not be a UCharacter.getType() result, but rather a mask value produced by logically ORing (1 \<\< UCharacter.getType()) values together. This allows grouped categories such as \[:L:\] to be represented. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this set |

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun applyPattern(pattern: String!): UnicodeSet!
```

Modifies this set to represent the set specified by the given pattern. See the class description for the syntax of the pattern language. Whitespace is ignored.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyPattern(
    pattern: String!, 
    ignoreWhitespace: Boolean
): UnicodeSet!
```

Modifies this set to represent the set specified by the given pattern, optionally ignoring whitespace. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `ignoreWhitespace` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then Unicode Pattern_White_Space characters are ignored |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyPattern(
    pattern: String!, 
    options: Int
): UnicodeSet!
```

Modifies this set to represent the set specified by the given pattern, optionally ignoring whitespace. See the class description for the syntax of the pattern language.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying what characters are in the set |
| `options` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a bitmask indicating which options to apply. Valid options are `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#IGNORE_SPACE:kotlin.Int` and at most one of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ADD_CASE_MAPPINGS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#SIMPLE_CASE_INSENSITIVE:kotlin.Int`. These case options are mutually exclusive. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pattern contains a syntax error. |

### applyPropertyAlias

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyPropertyAlias(
    propertyAlias: String!, 
    valueAlias: String!
): UnicodeSet!
```

Modifies this set to contain those code points which have the given value for the given property. Prior contents of this set are lost.

| Parameters ||
|---|---|
| `propertyAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a property alias, either short or long. The name is matched loosely. See PropertyAliases.txt for names and a description of loose matching. If the value string is empty, then this string is interpreted as either a General_Category value alias, a Script value alias, a binary property alias, or a special ID. Special IDs are matched loosely and correspond to the following sets: "ANY" = \[\\\\u0000-\\\\U0010FFFF\], "ASCII" = \[\\\\u0000-\\\\u007F\]. |
| `valueAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a value alias, either short or long. The name is matched loosely. See PropertyValueAliases.txt for names and a description of loose matching. In addition to aliases listed, numeric values and canonical combining classes may be expressed numerically, e.g., ("nv", "0.5") or ("ccc", "220"). The value string may also be empty. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this set |

### applyPropertyAlias

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyPropertyAlias(
    propertyAlias: String!, 
    valueAlias: String!, 
    symbols: SymbolTable!
): UnicodeSet!
```

Modifies this set to contain those code points which have the given value for the given property. Prior contents of this set are lost.

| Parameters ||
|---|---|
| `propertyAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string of the property alias. |
| `valueAlias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string of the value alias. |
| `symbols` | [SymbolTable](SymbolTable.md)!: if not null, then symbols are first called to see if a property is available. If true, then everything else is skipped. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this set |

### charAt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun charAt(index: Int): Int
```

Returns the character at the given index within this set, where the set is ordered by ascending code point. If the index is out of range, return -1. The inverse of this method is `indexOf()`.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an index from 0..size()-1 |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the character at the given index, or -1. |

### clear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): UnicodeSet!
```

Removes all of the elements from this set. This set will be empty after this call returns.

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Return a new set that is equivalent to this one.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): UnicodeSet!
```

Clone a thawed version of this class, according to the Freezable interface.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | the clone, not frozen |

### closeOver

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun closeOver(attribute: Int): UnicodeSet!
```

Close this set over the given attribute. For the attribute `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`, the result is to modify this set so that:

1. For each character or string 'a' in this set, all strings 'b' such that foldCase(a) == foldCase(b) are added to this set. (For most 'a' that are single characters, 'b' will have b.length() == 1.)
2. For each string 'e' in the resulting set, if e != foldCase(e), 'e' will be removed.

<br />

Example: \[aq\\u00DF{Bc}{bC}{Fi}\] =\> \[aAqQ\\u00DF\\uFB01{ss}{bc}{fi}\]

(Here foldCase(x) refers to the operation UCharacter.foldCase(x, true), and a == b actually denotes a.equals(b), not pointer comparison.)

| Parameters ||
|---|---|
| `attribute` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): bitmask for attributes to close over. Valid options: At most one of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#CASE_INSENSITIVE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#ADD_CASE_MAPPINGS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#SIMPLE_CASE_INSENSITIVE:kotlin.Int`. These case options are mutually exclusive. Unrelated options bits are ignored. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a reference to this set. |

### codePointStream

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun codePointStream(): IntStream!
```

Returns an `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` of Unicode code point values from this `UnicodeSet`.

**Warnings:**

- To iterate over the full contents, you have to also iterate over the strings.
- For speed, `UnicodeSet` iteration does not check for concurrent modification. 
 Do not alter the `UnicodeSet` while iterating.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#!` | an `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` of Unicode code point values |

### codePoints

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun codePoints(): MutableIterable<Int!>!
```

Returns an `https://developer.android.com/reference/kotlin/java/lang/Iterable.html#` for iteration over all the code points in this set.

**Warnings:**

- This is a convenience method, but comes with a performance penalty because it boxes `int` into `Integer`. 
 For an efficient but old alternative use next.
- To iterate over the full contents, you have to also iterate over the strings.
- For speed, `UnicodeSet` iteration does not check for concurrent modification. 
 Do not alter the `UnicodeSet` while iterating.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>!` | an `https://developer.android.com/reference/kotlin/java/lang/Iterable.html#` over all the code points |

### compact

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compact(): UnicodeSet!
```

Reallocate this objects internal structures to take up the least possible space, without changing this object's value.

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: UnicodeSet!): Int
```

Compares UnicodeSets, where shorter come first, and otherwise lexicographically (according to the comparison of the first characters that differ).

| Parameters ||
|---|---|
| `o` | the object to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative integer, zero, or a positive integer as this object is less than, equal to, or greater than the specified object. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

**See Also**

- compareTo

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(
    o: UnicodeSet!, 
    style: UnicodeSet.ComparisonStyle!
): Int
```

Compares UnicodeSets, in three different ways.
**See Also**

- compareTo

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: MutableIterable<String!>!): Int
```

### complement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun complement(): UnicodeSet!
```

This is equivalent to `complement(MIN_VALUE, MAX_VALUE)`.

**Note:** This performs a symmetric difference with all code points *and thus retains all multicharacter strings* . In order to achieve a "code point complement" (all code points minus this set), the easiest is to .complement.removeAllStrings .

### complement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun complement(c: Int): UnicodeSet!
```

Complements the specified character in this set. The character will be removed if it is in this set, or will be added if it is not in this set.

### complement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun complement(
    start: Int, 
    end: Int
): UnicodeSet!
```

Complements the specified range in this set. Any character in the range will be removed if it is in this set, or will be added if it is not in this set. If `start > end` then an empty range is complemented, leaving the set unchanged.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of range |

### complement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun complement(s: CharSequence!): UnicodeSet!
```

Complement the specified string in this set. The set will not contain the specified string once the call returns.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the string to complement |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### complementAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun complementAll(c: UnicodeSet!): UnicodeSet!
```

Complements in this set all elements contained in the specified set. Any character in the other set will be removed if it is in this set, or will be added if it is not in this set.

| Parameters ||
|---|---|
| `c` | [UnicodeSet](UnicodeSet.md)!: set that defines which elements will be complemented from this set. |

### complementAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun complementAll(s: CharSequence!): UnicodeSet!
```

Complement EACH of the characters in this string. Note: "ch" == {"c", "h"} If this set already any particular character, it has no effect on that character.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### contains

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(c: Int): Boolean
```

Returns true if this set contains the given character.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): character to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### contains

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(
    start: Int, 
    end: Int
): Boolean
```

Returns true if this set contains every character of the given range.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of the range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### contains

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contains(s: CharSequence!): Boolean
```

Returns `true` if this set contains the given multicharacter string.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: string to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this set contains the specified string |

### containsAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsAll(b: UnicodeSet!): Boolean
```

Returns true if this set contains all the characters and strings of the given set.

| Parameters ||
|---|---|
| `b` | [UnicodeSet](UnicodeSet.md)!: set to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### containsAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : CharSequence!> containsAll(collection: MutableIterable<T>!): Boolean
```
**See Also**

- containsAll

### containsAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsAll(s: String!): Boolean
```

Returns true if there is a partition of the string such that this set contains each of the partitioned strings. For example, for the Unicode set \[a{bc}{cd}\] 
containsAll is true for each of: "a", "bc", ""cdbca" 
containsAll is false for each of: "acb", "bcda", "bcx" 

| Parameters ||
|---|---|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: string containing characters to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### containsNone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsNone(b: UnicodeSet!): Boolean
```

Returns true if none of the characters or strings in this UnicodeSet appears in the string. For example, for the Unicode set \[a{bc}{cd}\] 
containsNone is true for: "xy", "cb" 
containsNone is false for: "a", "bc", "bcd" 

| Parameters ||
|---|---|
| `b` | [UnicodeSet](UnicodeSet.md)!: set to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### containsNone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsNone(
    start: Int, 
    end: Int
): Boolean
```

Returns true if this set contains none of the characters of the given range.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of the range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### containsNone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsNone(s: CharSequence!): Boolean
```

Returns true if this set contains none of the characters of the given string.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: string containing characters to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the test condition is met |

### containsNone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : CharSequence!> containsNone(collection: MutableIterable<T>!): Boolean
```
**See Also**

- containsNone

### containsSome

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsSome(s: UnicodeSet!): Boolean
```

Returns true if this set contains one or more of the characters and strings of the given set.

| Parameters ||
|---|---|
| `s` | [UnicodeSet](UnicodeSet.md)!: set to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the condition is met |

### containsSome

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsSome(
    start: Int, 
    end: Int
): Boolean
```

Returns true if this set contains one or more of the characters in the given range.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of the range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of the range |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the condition is met |

### containsSome

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsSome(s: CharSequence!): Boolean
```

Returns true if this set contains one or more of the characters of the given string.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: string containing characters to be checked for containment |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the condition is met |

### containsSome

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : CharSequence!> containsSome(collection: MutableIterable<T>!): Boolean
```
**See Also**

- containsAll

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this set for equality. Returns `true` if the specified object is also a set, the two sets have the same size, and every member of the specified set is contained in this set (or equivalently, every member of this set is contained in the specified set).

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | Object to be compared for equality with this set. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified Object is equal to this set. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): UnicodeSet!
```

Freeze this class, according to the Freezable interface.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this |

### from

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun from(s: CharSequence!): UnicodeSet!
```

Makes a set from a multicharacter string. Thus "ch" =\> {"ch"}

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a newly created set containing the given string |

### fromAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun fromAll(s: CharSequence!): UnicodeSet!
```

Makes a set from each of the characters in the string. Thus "ch" =\> {"c", "h"}

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | a newly created set containing the given characters |

### getRangeCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRangeCount(): Int
```

Iteration method that returns the number of ranges contained in this set.
**See Also**

- getRangeStart
- getRangeEnd

### getRangeEnd

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRangeEnd(index: Int): Int
```

Iteration method that returns the last character in the specified range of this set.

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if index is outside the range `0..getRangeCount()-1` |

**See Also**

- getRangeStart
- getRangeEnd

### getRangeStart

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRangeStart(index: Int): Int
```

Iteration method that returns the first character in the specified range of this set.

| Exceptions ||
|---|---|
| `java.lang.ArrayIndexOutOfBoundsException` | if index is outside the range `0..getRangeCount()-1` |

**See Also**

- getRangeCount
- getRangeEnd

### hasStrings

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasStrings(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this set contains multi-character strings or the empty string. |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the hash code value for this set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this set. |

**See Also**

- hashCode

### indexOf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOf(c: Int): Int
```

Returns the index of the given character within this set, where the set is ordered by ascending code point. If the character is not in this set, return -1. The inverse of this method is `charAt()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | an index from 0..size()-1, or -1 |

### isEmpty

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this set contains no elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this set contains no elements. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Is this frozen, according to the Freezable interface?

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | value |

### iterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iterator(): MutableIterator<String!>
```

Returns a string iterator. Uses the same order of iteration as UnicodeSetIterator.

**Warning:**For speed, UnicodeSet iteration does not check for concurrent modification. Do not alter the UnicodeSet while iterating.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | an Iterator. |

**See Also**

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

Implementation of UnicodeMatcher.matches(). Always matches the longest possible multichar string.

| Parameters ||
|---|---|
| `text` | [Replaceable](Replaceable.md)!: the text to be matched |
| `offset` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: on input, the index into text at which to begin matching. On output, the limit of the matched text. The number of matched characters is the output value of offset minus the input value. Offset should always point to the HIGH SURROGATE (leading code unit) of a pair of surrogates, both on entry and upon return. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the limit index of text to be matched. Greater than offset for a forward direction match, less than offset for a backward direction match. The last character to be considered for matching will be text.charAt(limit-1) in the forward direction or text.charAt(limit+1) in the backward direction. |
| --- | --- |
| `incremental` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, then assume further characters may be inserted at limit and check for partial matching. Otherwise assume the text as given is complete. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a match degree value indicating a full match, a partial match, or a mismatch. If incremental is false then U_PARTIAL_MATCH should never be returned. |

### matchesIndexValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun matchesIndexValue(v: Int): Boolean
```

Implementation of UnicodeMatcher API. Returns `true` if this set contains any character whose low byte is the given value. This is used by `RuleBasedTransliterator` for indexing.

### rangeStream

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun rangeStream(): Stream<UnicodeSet.EntryRange!>!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange` values from this `UnicodeSet`.

**Warnings:**

- The `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange` instance is the same each time; the contents are just reset.
- To iterate over the full contents, you have to also iterate over the strings.
- For speed, `UnicodeSet` iteration does not check for concurrent modification. 
 Do not alter the `UnicodeSet` while iterating.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange!>!` | a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet.EntryRange` |

### ranges

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ranges(): MutableIterable<UnicodeSet.EntryRange!>!
```

Provide for faster iteration than by String. Returns an Iterable/Iterator over ranges of code points. The UnicodeSet must not be altered during the iteration. The EntryRange instance is the same each time; the contents are just reset.

**Warning:**To iterate over the full contents, you have to also iterate over the strings.

**Warning:**For speed, UnicodeSet iteration does not check for concurrent modification. Do not alter the UnicodeSet while iterating.

```kotlin
// Sample code
  for (EntryRange range : us1.ranges()) {
      // do something with code points between range.codepoint and range.codepointEnd;
  }
  for (String s : us1.strings()) {
      // do something with each string;
  }
  
```

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(c: Int): UnicodeSet!
```

Removes the specified character from this set if it is present. The set will not contain the specified character once the call returns.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character to be removed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(
    start: Int, 
    end: Int
): UnicodeSet!
```

Removes the specified range from this set if it is present. The set will not contain the specified range once the call returns. If `start > end` then an empty range is removed, leaving the set unchanged.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of range to be removed from this set. |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of range to be removed from this set. |

### remove

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(s: CharSequence!): UnicodeSet!
```

Removes the specified string from this set if it is present. The set will not contain the specified string once the call returns.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the string to be removed |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### removeAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAll(c: UnicodeSet!): UnicodeSet!
```

Removes from this set all of its elements that are contained in the specified set. This operation effectively modifies this set so that its value is the *asymmetric set difference* of the two sets.

| Parameters ||
|---|---|
| `c` | [UnicodeSet](UnicodeSet.md)!: set that defines which elements will be removed from this set. |

### removeAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAll(s: CharSequence!): UnicodeSet!
```

Remove EACH of the characters in this string. Note: "ch" == {"c", "h"} If this set already any particular character, it has no effect on that character.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### removeAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : CharSequence!> removeAll(collection: MutableIterable<T>!): UnicodeSet!
```
**See Also**

- removeAll

### removeAllStrings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeAllStrings(): UnicodeSet!
```

Remove all strings from this UnicodeSet

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### retain

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun retain(c: Int): UnicodeSet!
```

Retain the specified character from this set if it is present. Upon return this set will be empty if it did not contain c, or will only contain c if it did contain c.

| Parameters ||
|---|---|
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character to be retained |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### retain

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun retain(
    start: Int, 
    end: Int
): UnicodeSet!
```

Retain only the elements in this set that are contained in the specified range. If `start > end` then an empty range is retained, leaving the set empty.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character, inclusive, of range |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character, inclusive, of range |

### retain

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun retain(cs: CharSequence!): UnicodeSet!
```

Retain the specified string in this set if it is present. Upon return this set will be empty if it did not contain s, or will only contain s if it did contain s.

| Parameters ||
|---|---|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the string to be retained |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### retainAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun retainAll(c: UnicodeSet!): UnicodeSet!
```

Retains only the elements in this set that are contained in the specified set. In other words, removes from this set all of its elements that are not contained in the specified set. This operation effectively modifies this set so that its value is the *intersection* of the two sets.

| Parameters ||
|---|---|
| `c` | [UnicodeSet](UnicodeSet.md)!: set that defines which elements this set will retain. |

### retainAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun retainAll(s: CharSequence!): UnicodeSet!
```

Retains EACH of the characters in this string. Note: "ch" == {"c", "h"} If this set already any particular character, it has no effect on that character.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the source string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet#!` | this object, for chaining |

### retainAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : CharSequence!> retainAll(collection: MutableIterable<T>!): UnicodeSet!
```
**See Also**

- retainAll

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(other: UnicodeSet!): UnicodeSet!
```

Make this object represent the same set as `other`.

| Parameters ||
|---|---|
| `other` | [UnicodeSet](UnicodeSet.md)!: a `UnicodeSet` whose value will be copied to this object |

### set

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun set(
    start: Int, 
    end: Int
): UnicodeSet!
```

Make this object represent the range `start - end`. If `start > end` then this object is set to an empty range.

| Parameters ||
|---|---|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): first character in the set, inclusive |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): last character in the set, inclusive |

### size

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun size(): Int
```

Returns the number of elements in this set (its cardinality) Note than the elements of a set may include both individual codepoints and strings.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this set (its cardinality). |

### span

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun span(
    s: CharSequence!, 
    spanCondition: UnicodeSet.SpanCondition!
): Int
```

Span a string using this UnicodeSet.

To replace, count elements, or delete spans, see UnicodeSetSpanner.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The string to be spanned |
| `spanCondition` | [UnicodeSet.SpanCondition](../android/icu/text/UnicodeSet.SpanCondition.md)!: The span condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the span |

### span

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun span(
    s: CharSequence!, 
    start: Int, 
    spanCondition: UnicodeSet.SpanCondition!
): Int
```

Span a string using this UnicodeSet. If the start index is less than 0, span will start from 0. If the start index is greater than the string length, span returns the string length.

To replace, count elements, or delete spans, see UnicodeSetSpanner.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The string to be spanned |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The start index that the span begins |
| `spanCondition` | [UnicodeSet.SpanCondition](../android/icu/text/UnicodeSet.SpanCondition.md)!: The span condition |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the string index which ends the span (i.e. exclusive) |

### spanBack

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spanBack(
    s: CharSequence!, 
    spanCondition: UnicodeSet.SpanCondition!
): Int
```

Span a string backwards (from the end) using this UnicodeSet.

To replace, count elements, or delete spans, see UnicodeSetSpanner.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The string to be spanned |
| `spanCondition` | [UnicodeSet.SpanCondition](../android/icu/text/UnicodeSet.SpanCondition.md)!: The span condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The string index which starts the span (i.e. inclusive). |

### spanBack

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spanBack(
    s: CharSequence!, 
    fromIndex: Int, 
    spanCondition: UnicodeSet.SpanCondition!
): Int
```

Span a string backwards (from the fromIndex) using this UnicodeSet. If the fromIndex is less than 0, spanBack will return 0. If fromIndex is greater than the string length, spanBack will start from the string length.

To replace, count elements, or delete spans, see UnicodeSetSpanner.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The string to be spanned |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the char (exclusive) that the string should be spanned backwards |
| `spanCondition` | [UnicodeSet.SpanCondition](../android/icu/text/UnicodeSet.SpanCondition.md)!: The span condition |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The string index which starts the span (i.e. inclusive). |

### stream

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stream(): Stream<String!>!
```

Returns a stream of `String` values from this `UnicodeSet`.

**Warnings:**

- To iterate over the full contents, you have to also iterate over the strings.
- For speed, `UnicodeSet` iteration does not check for concurrent modification. 
 Do not alter the `UnicodeSet` while iterating.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `String` |

### stringStream

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun stringStream(): Stream<String!>!
```

Returns a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `String` values from this `UnicodeSet`.

**Warnings:**

- To iterate over the full contents, you have to also iterate over the ranges or code points.
- For speed, `UnicodeSet` iteration does not check for concurrent modification. 
 Do not alter the `UnicodeSet` while iterating.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#` of `String` |

### strings

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun strings(): MutableCollection<String!>!
```

For iterating through the strings in the set. Example:

```kotlin
for (String key : myUnicodeSet.strings()) {
    doSomethingWith(key);
  }
  
```

<br />

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toPattern(escapeUnprintable: Boolean): String!
```

Returns a string representation of this set. If the result of calling this function is passed to a UnicodeSet constructor, it will produce another set that is equal to this one.

| Parameters ||
|---|---|
| `escapeUnprintable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then convert unprintable character to their hex escape representations, \\\\uxxxx or \\\\Uxxxxxxxx. Unprintable characters are those other than U+000A, U+0020..U+007E. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Return a programmer-readable string representation of this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### ALL_CODE_POINTS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALL_CODE_POINTS: UnicodeSet!
```

Constant for the set of all code points. (Since UnicodeSets can include strings, does not include everything that a UnicodeSet can.)

### EMPTY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMPTY: UnicodeSet!
```

Constant for the empty set.
