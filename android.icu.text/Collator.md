Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collator

Kotlin | [Java](Collator.md)
| --- | --- |

```
abstract class Collator : Cloneable, Comparator<Any!>, Freezable<Collator!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.Collator](Collator.md) |

| Known Direct Subclasses [RuleBasedCollator](RuleBasedCollator.md) |---|---| | [RuleBasedCollator](RuleBasedCollator.md) | RuleBasedCollator is a concrete subclass of Collator. | |
| --- | --- | --- | --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/text/Collator.html#`. Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

Collator performs locale-sensitive string comparison. A concrete subclass, RuleBasedCollator, allows customization of the collation ordering by the use of rule sets.

A Collator is thread-safe only when frozen. See isFrozen and `https://developer.android.com/reference/kotlin/android/icu/util/Freezable.html#`.

Following the [Unicode Consortium](http://www.unicode.org)'s specifications for the [Unicode Collation Algorithm (UCA)](https://www.unicode.org/reports/tr10/), there are 5 different levels of strength used in comparisons:

- PRIMARY strength: Typically, this is used to denote differences between base characters (for example, "a" \< "b"). It is the strongest difference. For example, dictionaries are divided into different sections by base character.
- SECONDARY strength: Accents in the characters are considered secondary differences (for example, "as" \< "às" \< "at"). Other differences between letters can also be considered secondary differences, depending on the language. A secondary difference is ignored when there is a primary difference anywhere in the strings.
- TERTIARY strength: Upper and lower case differences in characters are distinguished at tertiary strength (for example, "ao" \< "Ao" \< "aò"). In addition, a variant of a letter differs from the base form on the tertiary strength (such as "A" and "Ⓐ"). Another example is the difference between large and small Kana. A tertiary difference is ignored when there is a primary or secondary difference anywhere in the strings.
- QUATERNARY strength: When punctuation is ignored (see [Ignoring Punctuations in the User Guide](https://unicode-org.github.io/icu/userguide/collation/concepts#ignoring-punctuation)) at PRIMARY to TERTIARY strength, an additional strength level can be used to distinguish words with and without punctuation (for example, "ab" \< "a-b" \< "aB"). This difference is ignored when there is a PRIMARY, SECONDARY or TERTIARY difference. The QUATERNARY strength should only be used if ignoring punctuation is required.
- IDENTICAL strength: When all other strengths are equal, the IDENTICAL strength is used as a tiebreaker. The Unicode code point values of the NFD form of each string are compared, just in case there is no difference. For example, Hebrew cantillation marks are only distinguished at this strength. This strength should be used sparingly, as only code point value differences between two strings is an extremely rare occurrence. Using this strength substantially decreases the performance for both comparison and collation key generation APIs. This strength also increases the size of the collation key.

Unlike the JDK, ICU4J's Collator deals only with 2 decomposition modes, the canonical decomposition mode and one that does not use any decomposition. The compatibility decomposition mode, java.text.Collator.FULL_DECOMPOSITION is not supported here. If the canonical decomposition mode is set, the Collator handles un-normalized text properly, producing the same results as if the text were normalized in NFD. If canonical decomposition is turned off, it is the user's responsibility to ensure that all text is already in the appropriate form before performing a comparison or before getting a CollationKey.

For more information about the collation service see the [User Guide](https://unicode-org.github.io/icu/userguide/collation).

Examples of use

```kotlin
// Get the Collator for US English and set its strength to PRIMARY
  Collator usCollator = Collator.getInstance(Locale.US);
  usCollator.setStrength(Collator.PRIMARY);
  if (usCollator.compare("abc", "ABC") == 0) {
      System.out.println("Strings are equivalent");
  }
 
  The following example shows how to compare two strings using the
  Collator for the default locale.
 
  // Compare two strings in the default locale
  Collator myCollator = Collator.getInstance();
  myCollator.setDecomposition(NO_DECOMPOSITION);
  if (myCollator.compare("à\u0325", "a\u0325̀") != 0) {
      System.out.println("à\u0325 is not equals to a\u0325̀ without decomposition");
      myCollator.setDecomposition(CANONICAL_DECOMPOSITION);
      if (myCollator.compare("à\u0325", "a\u0325̀") != 0) {
          System.out.println("Error: à\u0325 should be equals to a\u0325̀ with decomposition");
      }
      else {
          System.out.println("à\u0325 is equals to a\u0325̀ with decomposition");
      }
  }
  else {
      System.out.println("Error: à\u0325 should be not equals to a\u0325̀ without decomposition");
  }
  
```

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes` Reordering codes for non-script groups that can be reordered under collation. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int` Decomposition mode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#FULL_DECOMPOSITION:kotlin.Int` **\[icu\] Note:** This is for backwards compatibility with Java APIs only. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int` Smallest Collator strength value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int` Decomposition mode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int` Strongest collator strength value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int` **\[icu\]** Fourth level collator strength value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int` Second level collator strength value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int` Third level collator strength value. |

| Protected constructors ||
|---|---|
| Collator Empty default constructor to make javadocs happy |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Clones the collator. |
| open [Collator](Collator.md)! | cloneAsThawed Provides for the clone operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares the source Object to the target Object. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compare Compares the source text String to the target text String according to this Collator's rules, strength and decomposition mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares the equality of two Collator objects. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Compares the equality of two text Strings using this Collator's rules, strength and decomposition mode. |
| --- | --- |
| open [Collator](Collator.md)! | freeze Freezes the collator. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java.util/Locale.md)!\>! | getAvailableLocales Returns the set of locales, as Locale objects, for which collators are installed. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](../android.icu.util/ULocale.md)!\>! | getAvailableULocales **\[icu\]** Returns the set of locales, as ULocale objects, for which collators are installed. |
| --- | --- |
| abstract [CollationKey](CollationKey.md)! | getCollationKey Transforms the String into a CollationKey suitable for efficient repeated comparison. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDecomposition Returns the decomposition mode of this Collator. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName **\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName **\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName **\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getDisplayName **\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale. |
| --- | --- |
| open static [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getEquivalentReorderCodes Retrieves all the reorder codes that are grouped with the given reorder code. |
| static [ULocale](../android.icu.util/ULocale.md)! | getFunctionalEquivalent **\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service. |
| static [ULocale](../android.icu.util/ULocale.md)! | getFunctionalEquivalent **\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service. |
| --- | --- |
| static [Collator](Collator.md)! | getInstance Returns the Collator for the current default locale. |
| static [Collator](Collator.md)! | getInstance **\[icu\]** Returns the Collator for the desired locale. |
| static [Collator](Collator.md)! | getInstance Returns the Collator for the desired locale. |
| --- | --- |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getKeywordValues **\[icu\]** Given a keyword, returns an array of all values for that keyword that are currently in use. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getKeywordValuesForLocale **\[icu\]** Given a key and a locale, returns an array of string values in a preferred order that would make a difference. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | getKeywords **\[icu\]** Returns an array of all possible keywords that are relevant to collation. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxVariable **\[icu\]** Returns the maximum reordering group whose characters are affected by the alternate handling behavior. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getReorderCodes Retrieves the reordering codes for this collator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStrength Returns this Collator's strength attribute. |
| --- | --- |
| open [UnicodeSet](UnicodeSet.md)! | getTailoredSet **\[icu\]** Returns a UnicodeSet that contains all the characters and sequences tailored in this collator. |
| abstract [VersionInfo](../android.icu.util/VersionInfo.md)! | getUCAVersion **\[icu\]** Returns the UCA version of this collator object. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVariableTop **\[icu\]** Gets the variable top value of a Collator. |
| --- | --- |
| abstract [VersionInfo](../android.icu.util/VersionInfo.md)! | getVersion **\[icu\]** Returns the version of this collator object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Generates a hash code for this Collator object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFrozen Determines whether the object has been frozen or not. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDecomposition Sets the decomposition mode of this Collator. |
| open [Collator](Collator.md)! | setMaxVariable **\[icu\]** Sets the variable top to the top of the specified reordering group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setReorderCodes Sets the reordering codes for this collator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStrength Sets this Collator's strength attribute. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | reversed Returns a comparator that imposes the reverse ordering of this comparator. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparing Returns a lexicographic-order comparator with another comparator. If this `Comparator` considers two elements equal, i.e. `compare(a, b) == 0`, `other` is used to determine the order. The returned comparator is serializable if the specified comparator is also serializable. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparing Returns a lexicographic-order comparator with a function that extracts a `Comparable` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparing Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given `Comparator`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparingDouble Returns a lexicographic-order comparator with a function that extracts a `double` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparingInt Returns a lexicographic-order comparator with a function that extracts an `int` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | thenComparingLong Returns a lexicographic-order comparator with a function that extracts a `long` sort key. <br /> | ||

## Constants

### CANONICAL_DECOMPOSITION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANONICAL_DECOMPOSITION: Int
```

Decomposition mode value. With CANONICAL_DECOMPOSITION set, characters that are canonical variants according to the Unicode standard will be decomposed for collation.

CANONICAL_DECOMPOSITION corresponds to Normalization Form D as described in [Unicode Technical Report #15](https://www.unicode.org/reports/tr15/).

 Value: 17

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`
- getDecomposition
- setDecomposition

### FULL_DECOMPOSITION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FULL_DECOMPOSITION: Int
```

**\[icu\] Note:** This is for backwards compatibility with Java APIs only. It should not be used, IDENTICAL should be used instead. ICU's collation does not support Java's FULL_DECOMPOSITION mode.

 Value: 15

### IDENTICAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IDENTICAL: Int
```

Smallest Collator strength value. When all other strengths are equal, the IDENTICAL strength is used as a tiebreaker. The Unicode code point values of the NFD form of each string are compared, just in case there is no difference. See class documentation for more explanation.

Note this value is different from JDK's

 Value: 15

### NO_DECOMPOSITION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_DECOMPOSITION: Int
```

Decomposition mode value. With NO_DECOMPOSITION set, Strings will not be decomposed for collation. This is the default decomposition setting unless otherwise specified by the locale used to create the Collator.

**Note** this value is different from the JDK's.

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int`
- getDecomposition
- setDecomposition

### PRIMARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIMARY: Int
```

Strongest collator strength value. Typically used to denote differences between base characters. See class documentation for more explanation.

 Value: 0

**See Also**

- setStrength
- getStrength

### QUATERNARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val QUATERNARY: Int
```

**\[icu\]** Fourth level collator strength value. When punctuation is ignored (see [Ignoring Punctuation in the User Guide](https://unicode-org.github.io/icu/userguide/collation/concepts#ignoring-punctuation)) at PRIMARY to TERTIARY strength, an additional strength level can be used to distinguish words with and without punctuation. See class documentation for more explanation.

 Value: 3

**See Also**

- setStrength
- getStrength

### SECONDARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SECONDARY: Int
```

Second level collator strength value. Accents in the characters are considered secondary differences. Other differences between letters can also be considered secondary differences, depending on the language. See class documentation for more explanation.

 Value: 1

**See Also**

- setStrength
- getStrength

### TERTIARY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TERTIARY: Int
```

Third level collator strength value. Upper and lower case differences in characters are distinguished at this strength level. In addition, a variant of a letter differs from the base form on the tertiary level. See class documentation for more explanation.

 Value: 2

**See Also**

- setStrength
- getStrength

## Protected constructors

### Collator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Collator()
```

Empty default constructor to make javadocs happy

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Clones the collator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this collator. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun cloneAsThawed(): Collator!
```

Provides for the clone operation. Any clone is initially unfrozen.

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compare(
    source: Any!, 
    target: Any!
): Int
```

Compares the source Object to the target Object.

| Parameters ||
|---|---|
| `o1` | the first object to be compared. |
| `o2` | the second object to be compared. |
| `source` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the source Object. |
| --- | --- |
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the target Object. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer value. Value is less than zero if source is less than target, value is zero if source and target are equal, value is greater than zero if source is greater than target. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | thrown if either arguments cannot be cast to CharSequence. |
| `java.lang.NullPointerException` | if an argument is null and this comparator does not permit null arguments |

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun compare(
    source: String!, 
    target: String!
): Int
```

Compares the source text String to the target text String according to this Collator's rules, strength and decomposition mode. Returns an integer less than, equal to or greater than zero depending on whether the source String is less than, equal to or greater than the target String. See the Collator class description for an example of use.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the source String. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target String. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer value. Value is less than zero if source is less than target, value is zero if source and target are equal, value is greater than zero if source is greater than target. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if either argument is null. |

**See Also**

- CollationKey
- getCollationKey

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the equality of two Collator objects. Collator objects are equal if they have the same collation (sorting \& searching) behavior.

The base class checks for null and for equal types. Subclasses should override.

| Parameters ||
|---|---|
| `obj` | the Collator to compare to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this Collator has exactly the same collation behavior as obj, false otherwise. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(
    source: String!, 
    target: String!
): Boolean
```

Compares the equality of two text Strings using this Collator's rules, strength and decomposition mode. Convenience method.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the source string to be compared. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target string to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the strings are equal according to the collation rules, otherwise false. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if either arguments is null. |

**See Also**

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun freeze(): Collator!
```

Freezes the collator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator#!` | the collator itself. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns the set of locales, as Locale objects, for which collators are installed. Note that Locale objects do not support RFC 3066.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | the list of locales in which collators are installed. This list includes any that have been registered, in addition to those that are installed with ICU4J. |

### getAvailableULocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableULocales(): Array<ULocale!>!
```

**\[icu\]** Returns the set of locales, as ULocale objects, for which collators are installed. ULocale objects support RFC 3066.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!>!` | the list of locales in which collators are installed. This list includes any that have been registered, in addition to those that are installed with ICU4J. |

### getCollationKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCollationKey(source: String!): CollationKey!
```

Transforms the String into a CollationKey suitable for efficient repeated comparison. The resulting key depends on the collator's rules, strength and decomposition mode.

Note that collation keys are often less efficient than simply doing comparison. For more details, see the ICU User Guide.

See the CollationKey class documentation for more information.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to be transformed into a CollationKey. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey!` | the CollationKey for the given String based on this Collator's collation rules. If the source String is null, a null CollationKey is returned. |

**See Also**

- CollationKey
- compare

### getDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDecomposition(): Int
```

Returns the decomposition mode of this Collator. The decomposition mode determines how Unicode composed characters are handled.

See the Collator class description for more details.

The base class method always returns `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`. Subclasses should override it if appropriate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the decomposition mode |

**See Also**

- setDecomposition
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int`

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(objectLocale: ULocale!): String!
```

**\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale.

| Parameters ||
|---|---|
| `objectLocale` | [ULocale](../android.icu.util/ULocale.md)!: the locale of the collator |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(
    objectLocale: ULocale!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale.

| Parameters ||
|---|---|
| `objectLocale` | [ULocale](../android.icu.util/ULocale.md)!: the locale of the collator |
| `displayLocale` | [ULocale](../android.icu.util/ULocale.md)!: the locale for the collator's display name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(objectLocale: Locale!): String!
```

**\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale.

| Parameters ||
|---|---|
| `objectLocale` | [Locale](../java.util/Locale.md)!: the locale of the collator |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(
    objectLocale: Locale!, 
    displayLocale: Locale!
): String!
```

**\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale.

| Parameters ||
|---|---|
| `objectLocale` | [Locale](../java.util/Locale.md)!: the locale of the collator |
| `displayLocale` | [Locale](../java.util/Locale.md)!: the locale for the collator's display name |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the display name |

### getEquivalentReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getEquivalentReorderCodes(reorderCode: Int): IntArray!
```

Retrieves all the reorder codes that are grouped with the given reorder code. Some reorder codes are grouped and must reorder together. Beginning with ICU 55, scripts only reorder together if they are primary-equal, for example Hiragana and Katakana.

| Parameters ||
|---|---|
| `reorderCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The reorder code to determine equivalence for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | the set of all reorder codes in the same group as the given reorder code. |

**See Also**

- setReorderCodes
- getReorderCodes
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes`
- `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.html#`

### getFunctionalEquivalent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getFunctionalEquivalent(
    keyword: String!, 
    locID: ULocale!
): ULocale!
```

**\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service.

| Parameters ||
|---|---|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a particular keyword as enumerated by getKeywords. |
| `locID` | [ULocale](../android.icu.util/ULocale.md)!: The requested locale |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!` | the locale |

**See Also**

- getFunctionalEquivalent

### getFunctionalEquivalent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getFunctionalEquivalent(
    keyword: String!, 
    locID: ULocale!, 
    isAvailable: BooleanArray!
): ULocale!
```

**\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service. If two locales return the same result, then collators instantiated for these locales will behave equivalently. The converse is not always true; two collators may in fact be equivalent, but return different results, due to internal details. The return result has no other meaning than that stated above, and implies nothing as to the relationship between the two locales. This is intended for use by applications who wish to cache collators, or otherwise reuse collators when possible. The functional equivalent may change over time. For more information, please see the [Locales and Services](https://unicode-org.github.io/icu/userguide/locale#locales-and-services) section of the ICU User Guide.

| Parameters ||
|---|---|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a particular keyword as enumerated by getKeywords. |
| `locID` | [ULocale](../android.icu.util/ULocale.md)!: The requested locale |
| `isAvailable` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!: If non-null, isAvailable\[0\] will receive and output boolean that indicates whether the requested locale was 'available' to the collation service. If non-null, isAvailable must have length \>= 1. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!` | the locale |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(): Collator!
```

Returns the Collator for the current default locale. The default locale is determined by java.util.Locale.getDefault().

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator#!` | the Collator for the default locale (for example, en_US) if it is created successfully. Otherwise if there is no Collator associated with the current locale, the root collator will be returned. |

**See Also**

- getDefault
- getInstance

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(locale: ULocale!): Collator!
```

**\[icu\]** Returns the Collator for the desired locale.

For some languages, multiple collation types are available; for example, "de@collation=phonebook". Starting with ICU 54, collation attributes can be specified via locale keywords as well, in the old locale extension syntax ("el@colCaseFirst=upper") or in language tag syntax ("el-u-kf-upper"). See [User Guide: Collation API](https://unicode-org.github.io/icu/userguide/collation/api).

| Parameters ||
|---|---|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the desired locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator#!` | Collator for the desired locale if it is created successfully. Otherwise if there is no Collator associated with the current locale, the root collator will be returned. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale.html#`
- `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#`
- getInstance
- getInstance

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(locale: Locale!): Collator!
```

Returns the Collator for the desired locale.

For some languages, multiple collation types are available; for example, "de-u-co-phonebk". Starting with ICU 54, collation attributes can be specified via locale keywords as well, in the old locale extension syntax ("el@colCaseFirst=upper", only with `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#`) or in language tag syntax ("el-u-kf-upper"). See [User Guide: Collation API](https://unicode-org.github.io/icu/userguide/collation/api).

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the desired locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator#!` | Collator for the desired locale if it is created successfully. Otherwise if there is no Collator associated with the current locale, the root collator will be returned. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale.html#`
- `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.html#`
- getInstance
- getInstance

### getKeywordValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getKeywordValues(keyword: String!): Array<String!>!
```

**\[icu\]** Given a keyword, returns an array of all values for that keyword that are currently in use.

| Parameters ||
|---|---|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: one of the keywords returned by getKeywords. |

**See Also**

- getKeywords

### getKeywordValuesForLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getKeywordValuesForLocale(
    key: String!, 
    locale: ULocale!, 
    commonlyUsed: Boolean
): Array<String!>!
```

**\[icu\]** Given a key and a locale, returns an array of string values in a preferred order that would make a difference. These are all and only those values where the open (creation) of the service with the locale formed from the input locale plus input keyword and that value has different behavior than creation with the input locale alone.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: one of the keys supported by this service. For now, only "collation" is supported. |
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the locale |
| `commonlyUsed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if set to true it will return only commonly used values with the given locale in preferred order. Otherwise, it will return all the available values for the locale. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of string values for the given key and the locale. |

### getKeywords

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getKeywords(): Array<String!>!
```

**\[icu\]** Returns an array of all possible keywords that are relevant to collation. At this point, the only recognized keyword for this service is "collation".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an array of valid collation keywords. |

**See Also**

- getKeywordValues

### getMaxVariable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxVariable(): Int
```

**\[icu\]** Returns the maximum reordering group whose characters are affected by the alternate handling behavior.

The base class implementation returns Collator.ReorderCodes.PUNCTUATION.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum variable reordering group. |

**See Also**

- setMaxVariable

### getReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReorderCodes(): IntArray!
```

Retrieves the reordering codes for this collator. These reordering codes are a combination of UScript codes and ReorderCodes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | a copy of the reordering codes for this collator; if none are set then returns an empty array |

**See Also**

- setReorderCodes
- getEquivalentReorderCodes
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes`
- `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.html#`

### getStrength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getStrength(): Int
```

Returns this Collator's strength attribute. The strength attribute determines the minimum level of difference considered significant. **\[icu\] Note:** This can return QUATERNARY strength, which is not supported by the JDK version.

See the Collator class description for more details.

The base class method always returns `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`. Subclasses should override it if appropriate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | this Collator's current strength attribute. |

**See Also**

- setStrength
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int`

### getTailoredSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTailoredSet(): UnicodeSet!
```

**\[icu\]** Returns a UnicodeSet that contains all the characters and sequences tailored in this collator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet!` | a pointer to a UnicodeSet object containing all the code points and sequences that may sort differently than in the root collator. |

### getUCAVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getUCAVersion(): VersionInfo!
```

**\[icu\]** Returns the UCA version of this collator object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#!` | the version object associated with this collator |

### getVariableTop

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getVariableTop(): Int
```

**\[icu\]** Gets the variable top value of a Collator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the variable top primary weight |

**See Also**

- getMaxVariable

### getVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getVersion(): VersionInfo!
```

**\[icu\]** Returns the version of this collator object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#!` | the version object associated with this collator |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Generates a hash code for this Collator object.

The implementation exists just for consistency with equals implementation in this class and does not generate a useful hash code. Subclasses should override this implementation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value. |

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

An unfrozen Collator is mutable and not thread-safe. A frozen Collator is immutable and thread-safe.

### setDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecomposition(decomposition: Int): Unit
```

Sets the decomposition mode of this Collator. Setting this decomposition attribute with CANONICAL_DECOMPOSITION allows the Collator to handle un-normalized text properly, producing the same results as if the text were normalized. If NO_DECOMPOSITION is set, it is the user's responsibility to insure that all text is already in the appropriate form before a comparison or before getting a CollationKey. Adjusting decomposition mode allows the user to select between faster and more complete collation behavior.

Since a great many of the world's languages do not require text normalization, most locales set NO_DECOMPOSITION as the default decomposition mode.

The base class method does nothing. Subclasses should override it if appropriate.

See getDecomposition for a description of decomposition mode.

| Parameters ||
|---|---|
| `decomposition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new decomposition mode |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given value is not a valid decomposition mode. |

**See Also**

- getDecomposition
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int`

### setMaxVariable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaxVariable(group: Int): Collator!
```

**\[icu\]** Sets the variable top to the top of the specified reordering group. The variable top determines the highest-sorting character which is affected by the alternate handling behavior. If that attribute is set to UCOL_NON_IGNORABLE, then the variable top has no effect.

The base class implementation throws an UnsupportedOperationException.

| Parameters ||
|---|---|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of Collator.ReorderCodes.SPACE, Collator.ReorderCodes.PUNCTUATION, Collator.ReorderCodes.SYMBOL, Collator.ReorderCodes.CURRENCY; or Collator.ReorderCodes.DEFAULT to restore the default max variable group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator#!` | this |

**See Also**

- getMaxVariable

### setReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReorderCodes(vararg order: Int): Unit
```

Sets the reordering codes for this collator. Collation reordering allows scripts and some other groups of characters to be moved relative to each other. This reordering is done on top of the DUCET/CLDR standard collation order. Reordering can specify groups to be placed at the start and/or the end of the collation order. These groups are specified using UScript codes and `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes` entries.

By default, reordering codes specified for the start of the order are placed in the order given after several special non-script blocks. These special groups of characters are space, punctuation, symbol, currency, and digit. These special groups are represented with `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes` entries. Script groups can be intermingled with these special non-script groups if those special groups are explicitly specified in the reordering.

The special code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#OTHERS:kotlin.Int` stands for any script that is not explicitly mentioned in the list of reordering codes given. Anything that is after OTHERS will go at the very end of the reordering in the order given.

The special reorder code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#DEFAULT:kotlin.Int` will reset the reordering for this collator to the default for this collator. The default reordering may be the DUCET/CLDR order or may be a reordering that was specified when this collator was created from resource data or from rules. The DEFAULT code **must** be the sole code supplied when it is used. If not, then an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

The special reorder code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#NONE:kotlin.Int` will remove any reordering for this collator. The result of setting no reordering will be to have the DUCET/CLDR ordering used. The NONE code **must** be the sole code supplied when it is used.

| Parameters ||
|---|---|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reordering codes to apply to this collator; if this is null or an empty array then this clears any existing reordering |

**See Also**

- getReorderCodes
- getEquivalentReorderCodes
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes`
- `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.html#`

### setStrength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStrength(newStrength: Int): Unit
```

Sets this Collator's strength attribute. The strength attribute determines the minimum level of difference considered significant during comparison.

The base class method does nothing. Subclasses should override it if appropriate.

See the Collator class description for an example of use.

| Parameters ||
|---|---|
| `newStrength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new strength value. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the new strength value is not valid. |

**See Also**

- getStrength
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int`
