# RuleBasedCollator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RuleBasedCollator

```
open class RuleBasedCollator : Collator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.text.Collator](../java/text/Collator.md) ||
| | ↳ | [java.text.RuleBasedCollator](../java/text/RuleBasedCollator.md) |

The class is a concrete subclass of`Collator`that provides a simple, data-driven, table collator. With this class you can create a customized table-based`Collator`maps characters to sort keys.

`RuleBasedCollator`has the following restrictions for efficiency (other subclasses may be used for more complex languages) :

1. If a special collation rule controlled by a \<modifier\> is specified it applies to the whole collator object.
2. All non-mentioned characters are at the end of the collation order.

The collation table is composed of a list of collation rules, where each rule is of one of three forms: 

```kotlin
<modifier>
     <relation> <text-argument>
     <reset> <text-argument>
  
```
The definitions of the rule elements is as follows:

- **Text-Argument** : A text-argument is any sequence of characters, excluding special characters (that is, common whitespace characters \[0009-000D, 0020\] and rule syntax characters \[0021-002F, 003A-0040, 005B-0060, 007B-007E\]). If those characters are desired, you can put them in single quotes (e.g. ampersand =\> '\&'). Note that unquoted white space characters are ignored; e.g.`b c`is treated as`bc`.
- **Modifier** : There are currently two modifiers that turn on special collation rules.
 - '@' : Turns on backwards sorting of accents (secondary differences), as in French.
 - '!' : Turns on Thai/Lao vowel-consonant swapping. If this rule is in force when a Thai vowel of the range \\U0E40-\\U0E44 precedes a Thai consonant of the range \\U0E01-\\U0E2E OR a Lao vowel of the range \\U0EC0-\\U0EC4 precedes a Lao consonant of the range \\U0E81-\\U0EAE then the vowel is placed after the consonant for collation purposes.

 '@' : Indicates that accents are sorted backwards, as in French.
- **Relation** : The relations are the following:
 - '\<' : Greater, as a letter difference (primary)
 - ';' : Greater, as an accent difference (secondary)
 - ',' : Greater, as a case difference (tertiary)
 - '=' : Equal
- **Reset** : There is a single reset which is used primarily for contractions and expansions, but which can also be used to add a modification at the end of a set of rules.

 '\&' : Indicates that the next rule follows the position to where the reset text-argument would be sorted.

This sounds more complicated than it is in practice. For example, the following are equivalent ways of expressing the same thing: 

```kotlin
a < b < c
  a < b & b < c
  a < c & a < b
  
```
Notice that the order is important, as the subsequent item goes immediately after the text-argument. The following are not equivalent: 

```kotlin
a < b & a < c
  a < c & a < b
  
```
Either the text-argument must already be present in the sequence, or some initial substring of the text-argument must be present. (e.g. "a \< b \& ae \< e" is valid since "a" is present in the sequence before "ae" is reset). In this latter case, "ae" is not entered and treated as a single character; instead, "e" is sorted as if it were expanded to two characters: "a" followed by an "e". This difference appears in natural languages: in traditional Spanish "ch" is treated as though it contracts to a single character (expressed as "c \< ch \< d"), while in traditional German a-umlaut is treated as though it expanded to two characters (expressed as "a,A \< b,B ... \&ae;\\u00e3\&AE;\\u00c3"). \[\\u00e3 and \\u00c3 are, of course, the escape sequences for a-umlaut.\]

**Ignorable Characters**

For ignorable characters, the first rule must start with a relation (the examples we have used above are really fragments; "a \< b" really should be "\< a \< b"). If, however, the first relation is not "\<", then all the all text-arguments up to the first "\<" are ignorable. For example, ", - \< a \< b" makes "-" an ignorable character, as we saw earlier in the word "black-birds". In the samples for different languages, you see that most accents are ignorable.

**Normalization and Accents**

`RuleBasedCollator`automatically processes its rule table to include both pre-composed and combining-character versions of accented characters. Even if the provided rule string contains only base characters and separate combining accent characters, the pre-composed accented characters matching all canonical combinations of characters from the rule string will be entered in the table.

This allows you to use a RuleBasedCollator to compare accented strings even when the collator is set to NO_DECOMPOSITION. There are two caveats, however. First, if the strings to be collated contain combining sequences that may not be in canonical order, you should set the collator to CANONICAL_DECOMPOSITION or FULL_DECOMPOSITION to enable sorting of combining sequences. Second, if the strings contain characters with compatibility decompositions (such as full-width and half-width forms), you must use FULL_DECOMPOSITION, since the rule tables only include canonical mappings.

**Errors**

The following are errors:

- A text-argument contains unquoted punctuation symbols (e.g. "a \< b-c \< d").
- A relation or reset character not followed by a text-argument (e.g. "a \< ,b").
- A reset where the text-argument (or an initial substring of the text-argument) is not already in the sequence. (e.g. "a \< b \& e \< f")

If you produce one of these errors, a`RuleBasedCollator`throws a`ParseException`.

**Examples**

Simple: "\< a \< b \< c \< d"

Norwegian: "\< a, A \< b, B \< c, C \< d, D \< e, E \< f, F \< g, G \< h, H \< i, I \< j, J \< k, K \< l, L \< m, M \< n, N \< o, O \< p, P \< q, Q \< r, R \< s, S \< t, T \< u, U \< v, V \< w, W \< x, X \< y, Y \< z, Z \< \\u00E6, \\u00C6 \< \\u00F8, \\u00D8 \< \\u00E5 = a\\u030A, \\u00C5 = A\\u030A; aa, AA"

To create a`RuleBasedCollator`object with specialized rules tailored to your needs, you construct the`RuleBasedCollator`with the rules contained in a`String`object. For example: 

```kotlin
String simple = "< a< b< c< d";
  RuleBasedCollator mySimple = new RuleBasedCollator(simple);
  
```
Or: 

```kotlin
String Norwegian = "< a, A < b, B < c, C < d, D < e, E < f, F < g, G < h, H < i, I" +
                     "< j, J < k, K < l, L < m, M < n, N < o, O < p, P < q, Q < r, R" +
                     "< s, S < t, T < u, U < v, V < w, W < x, X < y, Y < z, Z" +
                     "< \u00E6, \u00C6" +     // Latin letter ae & AE
                     "< \u00F8, \u00D8" +     // Latin letter o & O with stroke
                     "< \u00E5 = a\u030A," +  // Latin letter a with ring above
                     "  \u00C5 = A\u030A;" +  // Latin letter A with ring above
                     "  aa, AA";
  RuleBasedCollator myNorwegian = new RuleBasedCollator(Norwegian);
  
```

A new collation rules string can be created by concatenating rules strings. For example, the rules returned by [getRules()](../java/text/RuleBasedCollator.md))could be concatenated to combine multiple`RuleBasedCollator`s.

The following example demonstrates how to change the order of non-spacing accents, 

```kotlin
// old rule
  String oldRules = "=\u0301;\u0300;\u0302;\u0308"    // main accents
                  + ";\u0327;\u0303;\u0304;\u0305"    // main accents
                  + ";\u0306;\u0307;\u0309;\u030A"    // main accents
                  + ";\u030B;\u030C;\u030D;\u030E"    // main accents
                  + ";\u030F;\u0310;\u0311;\u0312"    // main accents
                  + "< a , A ; ae, AE ; \u00e6 , \u00c6"
                  + "< b , B < c, C < e, E & C < d, D";
  // change the order of accent characters
  String addOn = "& \u0300 ; \u0308 ; \u0302";
  RuleBasedCollator myCollator = new RuleBasedCollator(oldRules + addOn);
  
```

## Summary

| Inherited constants ||
|---|---|
| From class [Collator](../java/text/Collator.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CANONICAL_DECOMPOSITION](../java/text/Collator.md) <br /> Decomposition mode value. With CANONICAL_DECOMPOSITION set, characters that are canonical variants according to Unicode standard will be decomposed for collation. This should be used to get correct collation of accented characters. CANONICAL_DECOMPOSITION corresponds to Normalization Form D as described in [Unicode Standard Annex #15: Unicode Normalization Forms](http://www.unicode.org/reports/tr15/). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL_DECOMPOSITION](../java/text/Collator.md) <br /> Decomposition mode value. With FULL_DECOMPOSITION set, both Unicode canonical variants and Unicode compatibility variants will be decomposed for collation. This causes not only accented characters to be collated, but also characters that have special formats to be collated with their norminal form. For example, the half-width and full-width ASCII and Katakana characters are then collated together. FULL_DECOMPOSITION is the most complete and therefore the slowest decomposition mode. FULL_DECOMPOSITION corresponds to Normalization Form KD as described in [Unicode Standard Annex #15: Unicode Normalization Forms](http://www.unicode.org/reports/tr15/). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDENTICAL](../java/text/Collator.md) <br /> Collator strength value. When set, all differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for control characters ("\\u0001" vs "\\u0002") to be considered equal at the PRIMARY, SECONDARY, and TERTIARY levels but different at the IDENTICAL level. Additionally, differences between pre-composed accents such as "\\u00C0" (A-grave) and combining accents such as "A\\u0300" (A, combining-grave) will be considered significant at the IDENTICAL level if decomposition is set to NO_DECOMPOSITION. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_DECOMPOSITION](../java/text/Collator.md) <br /> Decomposition mode value. With NO_DECOMPOSITION set, accented characters will not be decomposed for collation. This is the default setting and provides the fastest collation but will only produce correct results for languages that do not use accents. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIMARY](../java/text/Collator.md) <br /> Collator strength value. When set, only PRIMARY differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for different base letters ("a" vs "b") to be considered a PRIMARY difference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECONDARY](../java/text/Collator.md) <br /> Collator strength value. When set, only SECONDARY and above differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for different accented forms of the same base letter ("a" vs "\\u00E4") to be considered a SECONDARY difference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TERTIARY](../java/text/Collator.md) <br /> Collator strength value. When set, only TERTIARY and above differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for case differences ("a" vs "A") to be considered a TERTIARY difference. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RuleBasedCollator](../java/text/RuleBasedCollator.md))`(`rules:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` RuleBasedCollator constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/RuleBasedCollator.md))`()` Standard override; no change in semantics. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](../java/text/RuleBasedCollator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compares the character data stored in two different strings based on the collation rules. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/RuleBasedCollator.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the equality of two collation objects. |
| --- | --- |
| open [CollationElementIterator](../java/text/CollationElementIterator.md)! | [getCollationElementIterator](../java/text/RuleBasedCollator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a CollationElementIterator for the given String. |
| open [CollationElementIterator](../java/text/CollationElementIterator.md)! | [getCollationElementIterator](../java/text/RuleBasedCollator.md))`(`source:` ` [CharacterIterator](../java/text/CharacterIterator.md)!`)` Returns a CollationElementIterator for the given CharacterIterator. |
| open [CollationKey](../java/text/CollationKey.md)! | [getCollationKey](../java/text/RuleBasedCollator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Transforms the string into a series of characters that can be compared with CollationKey. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getRules](../java/text/RuleBasedCollator.md))`()` Gets the table-based rules for the collation object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/text/RuleBasedCollator.md))`()` Generates the hash code for the table-based collation object |

| Inherited functions ||
|---|---|
| From class [Collator](../java/text/Collator.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](../java/text/Collator.md))`(`o1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `o2:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Compares its two arguments for order. Returns a negative integer, zero, or a positive integer as the first argument is less than, equal to, or greater than the second. This implementation merely returns`compare((String)o1, (String)o2) `. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/Collator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Convenience method for comparing the equality of two strings based on this Collator's collation rules. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | [getAvailableLocales](../java/text/Collator.md))`()` <br /> Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDecomposition](../java/text/Collator.md))`()` <br /> Get the decomposition mode of this Collator. Decomposition mode determines how Unicode composed characters are handled. Adjusting decomposition mode allows the user to select between faster and more complete collation behavior. The three values for decomposition mode are: - NO_DECOMPOSITION, - CANONICAL_DECOMPOSITION - FULL_DECOMPOSITION. See the documentation for these three constants for a description of their meaning. <br /> | | [Collator](../java/text/Collator.md)! | [getInstance](../java/text/Collator.md))`()` <br /> Gets the Collator for the current default locale. The default locale is determined by java.util.Locale.getDefault. <br /> | | [Collator](../java/text/Collator.md)! | [getInstance](../java/text/Collator.md))`(`desiredLocale:` ` [Locale](../java/util/Locale.md)!`)` <br /> Gets the Collator for the desired locale. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrength](../java/text/Collator.md))`()` <br /> Returns this Collator's strength property. The strength property determines the minimum level of difference considered significant during comparison. See the Collator class description for an example of use. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecomposition](../java/text/Collator.md))`(`decompositionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Set the decomposition mode of this Collator. See getDecomposition for a description of decomposition mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrength](../java/text/Collator.md))`(`newStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets this Collator's strength property. The strength property determines the minimum level of difference considered significant during comparison. See the Collator class description for an example of use. <br /> | ||
| From class [Comparator](../java/util/Comparator.md) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Comparator](../java/util/Comparator.md)<T>! | [reversed](../java/util/Comparator.md))`()` <br /> Returns a comparator that imposes the reverse ordering of this comparator. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`other:` ` [Comparator](../java/util/Comparator.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with another comparator. If this`Comparator`considers two elements equal, i.e.`compare(a, b) == 0`,`other`is used to determine the order. The returned comparator is serializable if the specified comparator is also serializable. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`keyExtractor:` ` [Function](../java/util/function/Function.md)<in` `T,` `out` `U>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`Comparable`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`keyExtractor:` ` [Function](../java/util/function/Function.md)<in` `T,` `out` `U>!`, `keyComparator:` ` [Comparator](../java/util/Comparator.md)<in` `U>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given`Comparator`. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingDouble](../java/util/Comparator.md))`(`keyExtractor:` ` [ToDoubleFunction](../java/util/function/ToDoubleFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`double`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingInt](../java/util/Comparator.md))`(`keyExtractor:` ` [ToIntFunction](../java/util/function/ToIntFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts an`int`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingLong](../java/util/Comparator.md))`(`keyExtractor:` ` [ToLongFunction](../java/util/function/ToLongFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`long`sort key. <br /> | ||

## Public constructors

### RuleBasedCollator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RuleBasedCollator(rules: String!)
```

RuleBasedCollator constructor. This takes the table rules and builds a collation table out of them. Please see RuleBasedCollator class description for more details on the collation rule syntax.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `rules` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the collation rules to build the collation table from. |

| Exceptions ||
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.text.ParseException` | A format exception will be thrown if the build process of the rules fails. For example, build rule "a \< ? \< d" will cause the constructor to throw the ParseException because the '?' is not quoted. |

**See Also**

- [java.util.Locale](../java/util/Locale.md)

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Standard override; no change in semantics.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this collator. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compare(
    source: String!, 
    target: String!
): Int
```

Compares the character data stored in two different strings based on the collation rules. Returns information about whether a string is less than, greater than or equal to another string in a language. This can be overridden in a subclass.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source string. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the target string. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns an integer value. Value is less than zero if source is less than target, value is zero if source and target are equal, value is greater than zero if source is greater than target. |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.NullPointerException` | if`source`or`target`is null. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the equality of two collation objects.

| Parameters ||
|--------|------------------------------------------------------------|
| `obj` | the table-based collation object to be compared with this. |
| `that` | the Collator to be compared with this. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the current table-based collation object is the same as the table-based collation object obj; false otherwise. |

### getCollationElementIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCollationElementIterator(source: String!): CollationElementIterator!
```

Returns a CollationElementIterator for the given String.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be collated |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [CollationElementIterator](../java/text/CollationElementIterator.md)! | a`CollationElementIterator`object |

**See Also**

- [java.text.CollationElementIterator](../java/text/CollationElementIterator.md) 

### getCollationElementIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCollationElementIterator(source: CharacterIterator!): CollationElementIterator!
```

Returns a CollationElementIterator for the given CharacterIterator.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [CharacterIterator](../java/text/CharacterIterator.md)!:the character iterator to be collated |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [CollationElementIterator](../java/text/CollationElementIterator.md)! | a`CollationElementIterator`object |

**See Also**

- [java.text.CollationElementIterator](../java/text/CollationElementIterator.md) 

### getCollationKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCollationKey(source: String!): CollationKey!
```

Transforms the string into a series of characters that can be compared with CollationKey.compareTo. This overrides java.text.Collator.getCollationKey. It can be overridden in a subclass.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be transformed into a collation key. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [CollationKey](../java/text/CollationKey.md)! | the CollationKey for the given String based on this Collator's collation rules. If the source String is null, a null CollationKey is returned. |

### getRules

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRules(): String!
```

Gets the table-based rules for the collation object.

On Android, the returned string will be empty unless this instance was constructed using [RuleBasedCollator(java.lang.String)](../java/text/RuleBasedCollator.md)).

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | returns the collation rules that the table collation object was created from. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generates the hash code for the table-based collation object

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
