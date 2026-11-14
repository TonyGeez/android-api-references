Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RuleBasedCollator

Kotlin | [Java](https://developer.android.com/reference/android/icu/text/RuleBasedCollator "View this page in Java")

```
class RuleBasedCollator : Collator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.icu.text.Collator](https://developer.android.com/reference/kotlin/android/icu/text/Collator) ||
| | ↳ | [android.icu.text.RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#) |

RuleBasedCollator is a concrete subclass of Collator. It allows customization of the Collator via user-specified rule sets. RuleBasedCollator is designed to be fully compliant to the [Unicode Collation Algorithm (UCA)](https://www.unicode.org/reports/tr10/) and conforms to ISO 14651.

A Collator is thread-safe only when frozen. See #isFrozen() and `https://developer.android.com/reference/kotlin/android/icu/util/Freezable.html#`.

Users are strongly encouraged to read the [User Guide](https://unicode-org.github.io/icu/userguide/collation) for more information about the collation service before using this class.

Create a RuleBasedCollator from a locale by calling the getInstance(Locale) factory method in the base class Collator. Collator.getInstance(Locale) creates a RuleBasedCollator object based on the collation rules defined by the argument locale. If a customized collation ordering or attributes is required, use the RuleBasedCollator(String) constructor with the appropriate rules. The customized RuleBasedCollator will base its ordering on the CLDR root collation, while re-adjusting the attributes and orders of the characters in the specified rule accordingly.

RuleBasedCollator provides correct collation orders for most locales supported in ICU. If specific data for a locale is not available, the orders eventually falls back to the [CLDR root sort order](http://www.unicode.org/reports/tr35/tr35-collation.html#Root_Collation).

For information about the collation rule syntax and details about customization, please refer to the [Collation customization](https://unicode-org.github.io/icu/userguide/collation/customization) section of the User Guide.

**Note** that there are some differences between the Collation rule syntax used in Java and ICU4J:

- According to the JDK documentation: 
 *Modifier '!' : Turns on Thai/Lao vowel-consonant swapping. If this rule is in force when a Thai vowel of the range \\U0E40-\\U0E44 precedes a Thai consonant of the range \\U0E01-\\U0E2E OR a Lao vowel of the range \\U0EC0-\\U0EC4 precedes a Lao consonant of the range \\U0E81-\\U0EAE then the vowel is placed after the consonant for collation purposes.
 If a rule is without the modifier '!', the Thai/Lao vowel-consonant swapping is not turned on.* 
 ICU4J's RuleBasedCollator does not support turning off the Thai/Lao vowel-consonant swapping, since the UCA clearly states that it has to be supported to ensure a correct sorting order. If a '!' is encountered, it is ignored.
- As mentioned in the documentation of the base class Collator, compatibility decomposition mode is not supported.

**Examples**

Creating Customized RuleBasedCollators:

```kotlin
String simple = "& a < b < c < d";
  RuleBasedCollator simpleCollator = new RuleBasedCollator(simple);
 
  String norwegian = "& a , A < b , B < c , C < d , D < e , E "
                     + "< f , F < g , G < h , H < i , I < j , "
                     + "J < k , K < l , L < m , M < n , N < "
                     + "o , O < p , P < q , Q <r , R <s , S < "
                     + "t , T < u , U < v , V < w , W < x , X "
                     + "< y , Y < z , Z < \u00E5 = a\u030A "
                     + ", \u00C5 = A\u030A ; aa , AA < \u00E6 "
                     + ", \u00C6 < \u00F8 , \u00D8";
  RuleBasedCollator norwegianCollator = new RuleBasedCollator(norwegian);
  
```
Concatenating rules to combine `Collator`s:

```kotlin
// Create an en_US Collator object
  RuleBasedCollator en_USCollator = (RuleBasedCollator)
      Collator.getInstance(new Locale("en", "US", ""));
  // Create a da_DK Collator object
  RuleBasedCollator da_DKCollator = (RuleBasedCollator)
      Collator.getInstance(new Locale("da", "DK", ""));
  // Combine the two
  // First, get the collation rules from en_USCollator
  String en_USRules = en_USCollator.getRules();
  // Second, get the collation rules from da_DKCollator
  String da_DKRules = da_DKCollator.getRules();
  RuleBasedCollator newCollator =
                              new RuleBasedCollator(en_USRules + da_DKRules);
  // newCollator has the combined rules
  
```
Making changes to an existing RuleBasedCollator to create a new `Collator` object, by appending changes to the existing rule:

```kotlin
// Create a new Collator object with additional rules
  String addRules = "& C < ch, cH, Ch, CH";
  RuleBasedCollator myCollator =
      new RuleBasedCollator(en_USCollator.getRules() + addRules);
  // myCollator contains the new rules
  
```
How to change the order of non-spacing accents:

```kotlin
// old rule with main accents
  String oldRules = "= \u0301 ; \u0300 ; \u0302 ; \u0308 "
                  + "; \u0327 ; \u0303 ; \u0304 ; \u0305 "
                  + "; \u0306 ; \u0307 ; \u0309 ; \u030A "
                  + "; \u030B ; \u030C ; \u030D ; \u030E "
                  + "; \u030F ; \u0310 ; \u0311 ; \u0312 "
                  + "< a , A ; ae, AE ; \u00e6 , \u00c6 "
                  + "< b , B < c, C < e, E & C < d , D";
  // change the order of accent characters
  String addOn = "& \u0300 ; \u0308 ; \u0302";
  RuleBasedCollator myCollator = new RuleBasedCollator(oldRules + addOn);
  
```
Putting in a new primary ordering before the default setting, e.g. sort English characters before or after Japanese characters in the Japanese `Collator`:

```kotlin
// get en_US Collator rules
  RuleBasedCollator en_USCollator
                         = (RuleBasedCollator)Collator.getInstance(Locale.US);
  // add a few Japanese characters to sort before English characters
  // suppose the last character before the first base letter 'a' in
  // the English collation rule is \u2212
  String jaString = "& \u2212 <\u3041, \u3042 <\u3043, "
                    + "\u3044";
  RuleBasedCollator myJapaneseCollator
               = new RuleBasedCollator(en_USCollator.getRules() + jaString);
  
```

This class is not subclassable

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/icu/text/Collator` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int` Decomposition mode value. With CANONICAL_DECOMPOSITION set, characters that are canonical variants according to the Unicode standard will be decomposed for collation. CANONICAL_DECOMPOSITION corresponds to Normalization Form D as described in [Unicode Technical Report #15](https://www.unicode.org/reports/tr15/). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#FULL_DECOMPOSITION:kotlin.Int` **\[icu\] Note:** This is for backwards compatibility with Java APIs only. It should not be used, IDENTICAL should be used instead. ICU's collation does not support Java's FULL_DECOMPOSITION mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int` Smallest Collator strength value. When all other strengths are equal, the IDENTICAL strength is used as a tiebreaker. The Unicode code point values of the NFD form of each string are compared, just in case there is no difference. See class documentation for more explanation. Note this value is different from JDK's <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int` Decomposition mode value. With NO_DECOMPOSITION set, Strings will not be decomposed for collation. This is the default decomposition setting unless otherwise specified by the locale used to create the Collator. **Note** this value is different from the JDK's. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int` Strongest collator strength value. Typically used to denote differences between base characters. See class documentation for more explanation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int` **\[icu\]** Fourth level collator strength value. When punctuation is ignored (see [Ignoring Punctuation in the User Guide](https://unicode-org.github.io/icu/userguide/collation/concepts#ignoring-punctuation)) at PRIMARY to TERTIARY strength, an additional strength level can be used to distinguish words with and without punctuation. See class documentation for more explanation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int` Second level collator strength value. Accents in the characters are considered secondary differences. Other differences between letters can also be considered secondary differences, depending on the language. See class documentation for more explanation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int` Third level collator strength value. Upper and lower case differences in characters are distinguished at this strength level. In addition, a variant of a letter differs from the base form on the tertiary level. See class documentation for more explanation. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#RuleBasedCollator(kotlin.String)(rules: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructor that takes the argument rules for customization. |

| Public methods ||
|---|---|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#clone()()` Clones the RuleBasedCollator |
| [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#cloneAsThawed()()` Provides for the clone operation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#compare(kotlin.String,%20kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Compares the source text String to the target text String according to the collation rules, strength and decomposition mode for this RuleBasedCollator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the equality of two Collator objects. |
| [Collator](https://developer.android.com/reference/kotlin/android/icu/text/Collator)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#freeze()()` Freezes the collator. |
| [CollationElementIterator](https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getCollationElementIterator(android.icu.text.UCharacterIterator)(source: https://developer.android.com/reference/kotlin/android/icu/text/UCharacterIterator!)` Return a CollationElementIterator for the given UCharacterIterator. |
| [CollationElementIterator](https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getCollationElementIterator(kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Return a CollationElementIterator for the given String. |
| [CollationElementIterator](https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getCollationElementIterator(java.text.CharacterIterator)(source: https://developer.android.com/reference/kotlin/java/text/CharacterIterator.html#!)` Return a CollationElementIterator for the given CharacterIterator. |
| [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getCollationKey(kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Get a Collation key for the argument String source from this RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getContractionsAndExpansions(android.icu.text.UnicodeSet,%20android.icu.text.UnicodeSet,%20kotlin.Boolean)(contractions: https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet!, expansions: https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet!, addPrefixes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Gets unicode sets containing contractions and/or expansions of a collator |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getDecomposition()()` Returns the decomposition mode of this Collator. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getMaxVariable()()` **\[icu\]** Returns the maximum reordering group whose characters are affected by the alternate handling behavior. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getNumericCollation()()` Method to retrieve the numeric collation value. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getReorderCodes()()` Retrieves the reordering codes for this collator. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getRules()()` Gets the collation tailoring rules for this RuleBasedCollator. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getRules(kotlin.Boolean)(fullrules: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns current rules. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getStrength()()` Returns this Collator's strength attribute. |
| [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getTailoredSet()()` Get a UnicodeSet that contains all the characters and sequences tailored in this collator. |
| [VersionInfo](https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getUCAVersion()()` Get the UCA version of this collator object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getVariableTop()()` **\[icu\]** Gets the variable top value of a Collator. |
| [VersionInfo](https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getVersion()()` Get the version of this collator object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#hashCode()()` Generates a unique hash code for this RuleBasedCollator. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isAlternateHandlingShifted()()` Checks if the alternate handling behavior is the UCA defined SHIFTED or NON_IGNORABLE. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isCaseLevel()()` Checks if case level is set to true. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isFrenchCollation()()` Checks if French Collation is set to true. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isFrozen()()` Determines whether the object has been frozen or not. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isLowerCaseFirst()()` Return true if a lowercase character is sorted before the corresponding uppercase character. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isUpperCaseFirst()()` Return true if an uppercase character is sorted before the corresponding lowercase character. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingDefault()()` Sets the alternate handling mode to the initial mode set during construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingShifted(kotlin.Boolean)(shifted: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the alternate handling for QUATERNARY strength to be either shifted or non-ignorable. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseFirstDefault()()` Sets the case first mode to the initial mode set during construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevel(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` When case level is set to true, an additional weight is formed between the SECONDARY and TERTIARY weight, known as the case level. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevelDefault()()` Sets the case level mode to the initial mode set during construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setDecomposition(kotlin.Int)(decomposition: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the decomposition mode of this Collator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setDecompositionDefault()()` Sets the decomposition mode to the initial mode set during construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollation(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the mode for the direction of SECONDARY weights to be used in French collation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollationDefault()()` Sets the French collation mode to the initial mode set during construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setLowerCaseFirst(kotlin.Boolean)(lowerfirst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the orders of lower cased characters to sort before upper cased characters, in strength TERTIARY. |
| [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#)! | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setMaxVariable(kotlin.Int)(group: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** Sets the variable top to the top of the specified reordering group. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollation(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** When numeric collation is turned on, this Collator makes substrings of digits sort according to their numeric values. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollationDefault()()` Method to set numeric collation to its default value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setReorderCodes(kotlin.Int)(vararg order: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the reordering codes for this collator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setStrength(kotlin.Int)(newStrength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets this Collator's strength attribute. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setStrengthDefault()()` Sets the collation strength to the initial mode set during the construction of the RuleBasedCollator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setUpperCaseFirst(kotlin.Boolean)(upperfirst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether uppercase characters sort before lowercase characters or vice versa, in strength TERTIARY. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/icu/text/Collator` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#compare(kotlin.Any,%20kotlin.Any)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Compares the source Object to the target Object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#equals(kotlin.String,%20kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Compares the equality of two text Strings using this Collator's rules, strength and decomposition mode. Convenience method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getAvailableLocales()()` Returns the set of locales, as Locale objects, for which collators are installed. Note that Locale objects do not support RFC 3066. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getAvailableULocales()()` **\[icu\]** Returns the set of locales, as ULocale objects, for which collators are installed. ULocale objects support RFC 3066. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getDisplayName(android.icu.util.ULocale)(objectLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getDisplayName(android.icu.util.ULocale,%20android.icu.util.ULocale)(objectLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, displayLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getDisplayName(java.util.Locale)(objectLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Returns the name of the collator for the objectLocale, localized for the default `DISPLAY` locale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getDisplayName(java.util.Locale,%20java.util.Locale)(objectLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!, displayLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **\[icu\]** Returns the name of the collator for the objectLocale, localized for the displayLocale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getEquivalentReorderCodes(kotlin.Int)(reorderCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieves all the reorder codes that are grouped with the given reorder code. Some reorder codes are grouped and must reorder together. Beginning with ICU 55, scripts only reorder together if they are primary-equal, for example Hiragana and Katakana. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getFunctionalEquivalent(kotlin.String,%20android.icu.util.ULocale)(keyword: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locID: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getFunctionalEquivalent(kotlin.String,%20android.icu.util.ULocale,%20kotlin.BooleanArray)(keyword: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locID: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, isAvailable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!)` **\[icu\]** Returns the functionally equivalent locale for the given requested locale, with respect to given keyword, for the collation service. If two locales return the same result, then collators instantiated for these locales will behave equivalently. The converse is not always true; two collators may in fact be equivalent, but return different results, due to internal details. The return result has no other meaning than that stated above, and implies nothing as to the relationship between the two locales. This is intended for use by applications who wish to cache collators, or otherwise reuse collators when possible. The functional equivalent may change over time. For more information, please see the [Locales and Services](https://unicode-org.github.io/icu/userguide/locale#locales-and-services) section of the ICU User Guide. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/Collator!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getInstance()()` Returns the Collator for the current default locale. The default locale is determined by java.util.Locale.getDefault(). <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/Collator!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getInstance(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **\[icu\]** Returns the Collator for the desired locale. For some languages, multiple collation types are available; for example, "de@collation=phonebook". Starting with ICU 54, collation attributes can be specified via locale keywords as well, in the old locale extension syntax ("el@colCaseFirst=upper") or in language tag syntax ("el-u-kf-upper"). See [User Guide: Collation API](https://unicode-org.github.io/icu/userguide/collation/api). <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/Collator!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getInstance(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns the Collator for the desired locale. For some languages, multiple collation types are available; for example, "de-u-co-phonebk". Starting with ICU 54, collation attributes can be specified via locale keywords as well, in the old locale extension syntax ("el@colCaseFirst=upper", only with `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#`) or in language tag syntax ("el-u-kf-upper"). See [User Guide: Collation API](https://unicode-org.github.io/icu/userguide/collation/api). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getKeywordValues(kotlin.String)(keyword: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **\[icu\]** Given a keyword, returns an array of all values for that keyword that are currently in use. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getKeywordValuesForLocale(kotlin.String,%20android.icu.util.ULocale,%20kotlin.Boolean)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, commonlyUsed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** Given a key and a locale, returns an array of string values in a preferred order that would make a difference. These are all and only those values where the open (creation) of the service with the locale formed from the input locale plus input keyword and that value has different behavior than creation with the input locale alone. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getKeywords()()` **\[icu\]** Returns an array of all possible keywords that are relevant to collation. At this point, the only recognized keyword for this service is "collation". <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#reversed()()` Returns a comparator that imposes the reverse ordering of this comparator. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparing(java.util.Comparator)(other: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in T>!)` Returns a lexicographic-order comparator with another comparator. If this `Comparator` considers two elements equal, i.e. `compare(a, b) == 0`, `other` is used to determine the order. The returned comparator is serializable if the specified comparator is also serializable. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparing(java.util.function.Function)(keyExtractor: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!)` Returns a lexicographic-order comparator with a function that extracts a `Comparable` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparing(java.util.function.Function,%20java.util.Comparator)(keyExtractor: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in T, out U>!, keyComparator: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in U>!)` Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given `Comparator`. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparingDouble(java.util.function.ToDoubleFunction)(keyExtractor: https://developer.android.com/reference/kotlin/java/util/function/ToDoubleFunction.html#<in T>!)` Returns a lexicographic-order comparator with a function that extracts a `double` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparingInt(java.util.function.ToIntFunction)(keyExtractor: https://developer.android.com/reference/kotlin/java/util/function/ToIntFunction.html#<in T>!)` Returns a lexicographic-order comparator with a function that extracts an `int` sort key. <br /> | | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#<T>!` | `https://developer.android.com/reference/kotlin/java/util/Comparator.html#thenComparingLong(java.util.function.ToLongFunction)(keyExtractor: https://developer.android.com/reference/kotlin/java/util/function/ToLongFunction.html#<in T>!)` Returns a lexicographic-order comparator with a function that extracts a `long` sort key. <br /> | ||

## Public constructors

### RuleBasedCollator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RuleBasedCollator(rules: String!)
```

Constructor that takes the argument rules for customization. The collator will be based on the CLDR root collation, with the attributes and re-ordering of the characters specified in the argument rules.

See the User Guide's section on [Collation Customization](https://unicode-org.github.io/icu/userguide/collation/customization) for details on the rule syntax.

| Parameters ||
|---|---|
| `rules` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the collation rules to build the collation table from. |

| Exceptions ||
|---|---|
| `java.text.ParseException` | and IOException thrown. ParseException thrown when argument rules have an invalid syntax. IOException thrown when an error occurred while reading internal data. |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clone(): Any
```

Clones the RuleBasedCollator

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a new instance of this RuleBasedCollator object |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### cloneAsThawed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cloneAsThawed(): RuleBasedCollator!
```

Provides for the clone operation. Any clone is initially unfrozen.

### compare

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compare(
    source: String!, 
    target: String!
): Int
```

Compares the source text String to the target text String according to the collation rules, strength and decomposition mode for this RuleBasedCollator. Returns an integer less than, equal to or greater than zero depending on whether the source String is less than, equal to or greater than the target String. See the Collator class description for an example of use.

General recommendation: 
If comparison are to be done to the same String multiple times, it would be more efficient to generate CollationKeys for the Strings and use CollationKey.compareTo(CollationKey) for the comparisons. If speed performance is critical and object instantiation is to be reduced, further optimization may be achieved by generating a simpler key of the form RawCollationKey and reusing this RawCollationKey object with the method RuleBasedCollator.getRawCollationKey. Internal byte representation can be directly accessed via RawCollationKey and stored for future use. Like CollationKey, RawCollationKey provides a method RawCollationKey.compareTo for key comparisons. If the each Strings are compared to only once, using the method RuleBasedCollator.compare(String, String) will have a better performance.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the source text String. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the target text String. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns an integer value. Value is less than zero if source is less than target, value is zero if source and target are equal, value is greater than zero if source is greater than target. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if either argument is null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getCollationKey(kotlin.String)`

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares the equality of two Collator objects. Collator objects are equal if they have the same collation (sorting \& searching) behavior.

The base class checks for null and for equal types. Subclasses should override.

| Parameters ||
|---|---|
| `obj` | the Collator to compare to. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this Collator has exactly the same collation behavior as obj, false otherwise. |

### freeze

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun freeze(): Collator!
```

Freezes the collator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Collator!` | the collator itself. |

### getCollationElementIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCollationElementIterator(source: UCharacterIterator!): CollationElementIterator!
```

Return a CollationElementIterator for the given UCharacterIterator. The source iterator's integrity will be preserved since a new copy will be created for use.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator`

### getCollationElementIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCollationElementIterator(source: String!): CollationElementIterator!
```

Return a CollationElementIterator for the given String.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator`

### getCollationElementIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCollationElementIterator(source: CharacterIterator!): CollationElementIterator!
```

Return a CollationElementIterator for the given CharacterIterator. The source iterator's integrity will be preserved since a new copy will be created for use.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator`

### getCollationKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCollationKey(source: String!): CollationKey!
```

Get a Collation key for the argument String source from this RuleBasedCollator.

General recommendation: 
If comparison are to be done to the same String multiple times, it would be more efficient to generate CollationKeys for the Strings and use CollationKey.compareTo(CollationKey) for the comparisons. If the each Strings are compared to only once, using the method RuleBasedCollator.compare(String, String) will have a better performance.

See the class documentation for an explanation about CollationKeys.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the text String to be transformed into a collation key. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey!` | the CollationKey for the given String based on this RuleBasedCollator's collation rules. If the source String is null, a null CollationKey is returned. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/CollationKey`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#compare(kotlin.String,%20kotlin.String)`

### getContractionsAndExpansions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getContractionsAndExpansions(
    contractions: UnicodeSet!, 
    expansions: UnicodeSet!, 
    addPrefixes: Boolean
): Unit
```

Gets unicode sets containing contractions and/or expansions of a collator

| Parameters ||
|---|---|
| `contractions` | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!: if not null, set to contain contractions |
| `expansions` | [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet)!: if not null, set to contain expansions |
| `addPrefixes` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): add the prefix contextual elements to contractions |

| Exceptions ||
|---|---|
| `java.lang.Exception` | Throws an exception if any errors occurs. |

### getDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDecomposition(): Int
```

Returns the decomposition mode of this Collator. The decomposition mode determines how Unicode composed characters are handled.

See the Collator class description for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the decomposition mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setDecomposition(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int`

### getMaxVariable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxVariable(): Int
```

**\[icu\]** Returns the maximum reordering group whose characters are affected by the alternate handling behavior.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum variable reordering group. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setMaxVariable(kotlin.Int)`

### getNumericCollation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumericCollation(): Boolean
```

Method to retrieve the numeric collation value. When numeric collation is turned on, this Collator generates a collation key for the numeric value of substrings of digits. This is a way to get '100' to sort AFTER '2'

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if numeric collation is turned on, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollation(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollationDefault()`

### getReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReorderCodes(): IntArray!
```

Retrieves the reordering codes for this collator. These reordering codes are a combination of UScript codes and ReorderCodes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | a copy of the reordering codes for this collator; if none are set then returns an empty array |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setReorderCodes(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getEquivalentReorderCodes(kotlin.Int)`

### getRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRules(): String!
```

Gets the collation tailoring rules for this RuleBasedCollator. Equivalent to String getRules(false).

On Android, the returned string will be empty unless this instance was constructed using `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#RuleBasedCollator(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the collation tailoring rules |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getRules(kotlin.Boolean)`

### getRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRules(fullrules: Boolean): String!
```

Returns current rules. The argument defines whether full rules (root collation + tailored) rules are returned or just the tailoring.

The root collation rules are an *approximation* of the root collator's sort order. They are almost never used or useful at runtime and can be removed from the data. See [User Guide: Collation Customization, Building on Existing Locales](https://unicode-org.github.io/icu/userguide/collation/customization#building-on-existing-locales)

`https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getRules()` should normally be used instead.

| Parameters ||
|---|---|
| `fullrules` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if the rules that defines the full set of collation order is required, otherwise false for returning only the tailored rules |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the current rules that defines this Collator. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getRules()`

### getStrength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStrength(): Int
```

Returns this Collator's strength attribute. The strength attribute determines the minimum level of difference considered significant.

**\[icu\] Note:** This can return QUATERNARY strength, which is not supported by the JDK version.

See the Collator class description for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | this Collator's current strength attribute. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setStrength(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int`

### getTailoredSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTailoredSet(): UnicodeSet!
```

Get a UnicodeSet that contains all the characters and sequences tailored in this collator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet!` | a pointer to a UnicodeSet object containing all the code points and sequences that may sort differently than in the root collator. |

### getUCAVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUCAVersion(): VersionInfo!
```

Get the UCA version of this collator object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#!` | the version object associated with this collator |

### getVariableTop

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVariableTop(): Int
```

**\[icu\]** Gets the variable top value of a Collator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the variable top primary weight |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getMaxVariable()`

### getVersion

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVersion(): VersionInfo!
```

Get the version of this collator object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/VersionInfo.html#!` | the version object associated with this collator |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Generates a unique hash code for this RuleBasedCollator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the unique hash code for this Collator |

### isAlternateHandlingShifted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAlternateHandlingShifted(): Boolean
```

Checks if the alternate handling behavior is the UCA defined SHIFTED or NON_IGNORABLE. If return value is true, then the alternate handling attribute for the Collator is SHIFTED. Otherwise if return value is false, then the alternate handling attribute for the Collator is NON_IGNORABLE See setAlternateHandlingShifted(boolean) for more details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true or false |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingShifted(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingDefault()`

### isCaseLevel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isCaseLevel(): Boolean
```

Checks if case level is set to true. See setCaseLevel(boolean) for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the case level mode |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevelDefault()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isCaseLevel()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevel(kotlin.Boolean)`

### isFrenchCollation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFrenchCollation(): Boolean
```

Checks if French Collation is set to true. See setFrenchCollation(boolean) for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if French Collation is set to true, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollation(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollationDefault()`

### isFrozen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFrozen(): Boolean
```

Determines whether the object has been frozen or not.

An unfrozen Collator is mutable and not thread-safe. A frozen Collator is immutable and thread-safe.

### isLowerCaseFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLowerCaseFirst(): Boolean
```

Return true if a lowercase character is sorted before the corresponding uppercase character. See setCaseFirst(boolean) for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true lower cased characters are sorted before upper cased characters, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setUpperCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setLowerCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isUpperCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseFirstDefault()`

### isUpperCaseFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUpperCaseFirst(): Boolean
```

Return true if an uppercase character is sorted before the corresponding lowercase character. See setCaseFirst(boolean) for details.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if upper cased characters are sorted before lower cased characters, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setUpperCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setLowerCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isLowerCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseFirstDefault()`

### setAlternateHandlingDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlternateHandlingDefault(): Unit
```

Sets the alternate handling mode to the initial mode set during construction of the RuleBasedCollator. See setAlternateHandling(boolean) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingShifted(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isAlternateHandlingShifted()`

### setAlternateHandlingShifted

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlternateHandlingShifted(shifted: Boolean): Unit
```

Sets the alternate handling for QUATERNARY strength to be either shifted or non-ignorable. See the UCA definition on [Variable Weighting](https://www.unicode.org/reports/tr10/#Variable_Weighting). This attribute will only be effective when QUATERNARY strength is set. If the mode is set to false, it corresponds to the NON_IGNORABLE mode in UCA. In the NON_IGNORABLE mode, the RuleBasedCollator treats all the code points with non-ignorable primary weights in the same way. If the mode is set to true, the behavior corresponds to SHIFTED defined in UCA, this causes code points with PRIMARY orders that are equal or below the variable top value to be ignored in PRIMARY order and moved to the QUATERNARY order. The default setting in a Collator object depends on the locale data loaded from the resources. For most locales, the default is false, but for others, such as "th", the default could be true.

| Parameters ||
|---|---|
| `shifted` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if SHIFTED behavior for alternate handling is desired, false for the NON_IGNORABLE behavior. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isAlternateHandlingShifted()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setAlternateHandlingDefault()`

### setCaseFirstDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCaseFirstDefault(): Unit
```

Sets the case first mode to the initial mode set during construction of the RuleBasedCollator. See setUpperCaseFirst(boolean) and setLowerCaseFirst(boolean) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isLowerCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isUpperCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setLowerCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setUpperCaseFirst(kotlin.Boolean)`

### setCaseLevel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCaseLevel(flag: Boolean): Unit
```

When case level is set to true, an additional weight is formed between the SECONDARY and TERTIARY weight, known as the case level. The case level is used to distinguish large and small Japanese Kana characters. Case level could also be used in other situations. For example to distinguish certain Pinyin characters. If the value is false, it means the case level is not generated. The contents of the case level are affected by the case first mode. A simple way to ignore accent differences in a string is to set the strength to PRIMARY and enable case level. The default setting in a Collator object depends on the locale data loaded from the resources.

See the section on [case level](https://unicode-org.github.io/icu/userguide/collation/architecture) for more information.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if case level sorting is required, false otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevelDefault()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isCaseLevel()`

### setCaseLevelDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCaseLevelDefault(): Unit
```

Sets the case level mode to the initial mode set during construction of the RuleBasedCollator. See setCaseLevel(boolean) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseLevel(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isCaseLevel()`

### setDecomposition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDecomposition(decomposition: Int): Unit
```

Sets the decomposition mode of this Collator. Setting this decomposition attribute with CANONICAL_DECOMPOSITION allows the Collator to handle un-normalized text properly, producing the same results as if the text were normalized. If NO_DECOMPOSITION is set, it is the user's responsibility to insure that all text is already in the appropriate form before a comparison or before getting a CollationKey. Adjusting decomposition mode allows the user to select between faster and more complete collation behavior.

Since a great many of the world's languages do not require text normalization, most locales set NO_DECOMPOSITION as the default decomposition mode. The default decompositon mode for the Collator is NO_DECOMPOSITON, unless specified otherwise by the locale used to create the Collator.

See getDecomposition for a description of decomposition mode.

| Parameters ||
|---|---|
| `decomposition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new decomposition mode |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given value is not a valid decomposition mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getDecomposition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#NO_DECOMPOSITION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#CANONICAL_DECOMPOSITION:kotlin.Int`

### setDecompositionDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDecompositionDefault(): Unit
```

Sets the decomposition mode to the initial mode set during construction of the RuleBasedCollator. See setDecomposition(int) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getDecomposition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setDecomposition(kotlin.Int)`

### setFrenchCollation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFrenchCollation(flag: Boolean): Unit
```

Sets the mode for the direction of SECONDARY weights to be used in French collation. If set to false, which treats SECONDARY weights in the order they appear. If set to true, the SECONDARY weights will be sorted backwards. See the section on [French collation](https://unicode-org.github.io/icu/userguide/collation/architecture) for more information. The default setting in a Collator object depends on the locale data loaded from the resources. For example, for "fr_CA" locale, the default is true.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to set the French collation on, false to set it off |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isFrenchCollation()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollationDefault()`

### setFrenchCollationDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFrenchCollationDefault(): Unit
```

Sets the French collation mode to the initial mode set during construction of the RuleBasedCollator. See setFrenchCollation(boolean) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isFrenchCollation()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setFrenchCollation(kotlin.Boolean)`

### setLowerCaseFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLowerCaseFirst(lowerfirst: Boolean): Unit
```

Sets the orders of lower cased characters to sort before upper cased characters, in strength TERTIARY. If true is set, the RuleBasedCollator will sort lower cased characters before the upper cased ones. Otherwise, if false is set, the RuleBasedCollator will ignore case preferences. The default default setting in a Collator object depends on the locale data loaded from the resources.

| Parameters ||
|---|---|
| `lowerfirst` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true for sorting lower cased characters before upper cased characters, false to ignore case preferences. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isLowerCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isUpperCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setUpperCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseFirstDefault()`

### setMaxVariable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMaxVariable(group: Int): RuleBasedCollator!
```

**\[icu\]** Sets the variable top to the top of the specified reordering group. The variable top determines the highest-sorting character which is affected by the alternate handling behavior. If that attribute is set to NON_IGNORABLE, then the variable top has no effect.

| Parameters ||
|---|---|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of Collator.ReorderCodes.SPACE, Collator.ReorderCodes.PUNCTUATION, Collator.ReorderCodes.SYMBOL, Collator.ReorderCodes.CURRENCY; or Collator.ReorderCodes.DEFAULT to restore the default max variable group |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#!` | this |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getMaxVariable()`

### setNumericCollation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setNumericCollation(flag: Boolean): Unit
```

**\[icu\]** When numeric collation is turned on, this Collator makes substrings of digits sort according to their numeric values.

This is a way to get '100' to sort AFTER '2'. Note that the longest digit substring that can be treated as a single unit is 254 digits (not counting leading zeros). If a digit substring is longer than that, the digits beyond the limit will be treated as a separate digit substring.

A "digit" in this sense is a code point with General_Category=Nd, which does not include circled numbers, roman numerals, etc. Only a contiguous digit substring is considered, that is, non-negative integers without separators. There is no support for plus/minus signs, decimals, exponents, etc.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to turn numeric collation on and false to turn it off |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getNumericCollation()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollationDefault()`

### setNumericCollationDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setNumericCollationDefault(): Unit
```

Method to set numeric collation to its default value.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getNumericCollation()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setNumericCollation(kotlin.Boolean)`

### setReorderCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setReorderCodes(vararg order: Int): Unit
```

Sets the reordering codes for this collator. Collation reordering allows scripts and some other groups of characters to be moved relative to each other. This reordering is done on top of the DUCET/CLDR standard collation order. Reordering can specify groups to be placed at the start and/or the end of the collation order. These groups are specified using UScript codes and `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes` entries.

By default, reordering codes specified for the start of the order are placed in the order given after several special non-script blocks. These special groups of characters are space, punctuation, symbol, currency, and digit. These special groups are represented with `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes` entries. Script groups can be intermingled with these special non-script groups if those special groups are explicitly specified in the reordering.

The special code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#OTHERS:kotlin.Int` stands for any script that is not explicitly mentioned in the list of reordering codes given. Anything that is after OTHERS will go at the very end of the reordering in the order given.

The special reorder code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#DEFAULT:kotlin.Int` will reset the reordering for this collator to the default for this collator. The default reordering may be the DUCET/CLDR order or may be a reordering that was specified when this collator was created from resource data or from rules. The DEFAULT code **must** be the sole code supplied when it is used. If not, then an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown.

The special reorder code `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes#NONE:kotlin.Int` will remove any reordering for this collator. The result of setting no reordering will be to have the DUCET/CLDR ordering used. The NONE code **must** be the sole code supplied when it is used.

| Parameters ||
|---|---|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the reordering codes to apply to this collator; if this is null or an empty array then this clears any existing reordering |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the reordering codes are malformed in any way (e.g. duplicates, multiple reset codes, overlapping equivalent scripts) |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getReorderCodes()`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#getEquivalentReorderCodes(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes`
- `https://developer.android.com/reference/kotlin/android/icu/lang/UScript.html#`

### setStrength

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStrength(newStrength: Int): Unit
```

Sets this Collator's strength attribute. The strength attribute determines the minimum level of difference considered significant during comparison.

See the Collator class description for an example of use.

| Parameters ||
|---|---|
| `newStrength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new strength value. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the new strength value is not one of PRIMARY, SECONDARY, TERTIARY, QUATERNARY or IDENTICAL. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getStrength()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setStrengthDefault()`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#PRIMARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#SECONDARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#TERTIARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#QUATERNARY:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/Collator#IDENTICAL:kotlin.Int`

### setStrengthDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStrengthDefault(): Unit
```

Sets the collation strength to the initial mode set during the construction of the RuleBasedCollator. See setStrength(int) for more details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setStrength(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#getStrength()`

### setUpperCaseFirst

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setUpperCaseFirst(upperfirst: Boolean): Unit
```

Sets whether uppercase characters sort before lowercase characters or vice versa, in strength TERTIARY. If false, lowercase characters sort before uppercase characters. If true, sort upper case characters first. The default setting in a Collator object depends on the locale data loaded from the resources. For most locales, the default is false, but for others, such as "da" or "mt", the default could be true.

| Parameters ||
|---|---|
| `upperfirst` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to sort uppercase characters before lowercase characters, false to sort lowercase characters before uppercase characters |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isLowerCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#isUpperCaseFirst()`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setLowerCaseFirst(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator#setCaseFirstDefault()`
