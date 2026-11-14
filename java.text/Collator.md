# Collator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Collator

```
abstract class Collator : Cloneable, Comparator<Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.Collator](../java/text/Collator.md) |

| Known Direct Subclasses [RuleBasedCollator](../java/text/RuleBasedCollator.md) |-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [RuleBasedCollator](../java/text/RuleBasedCollator.md) | The class is a concrete subclass of`Collator`that provides a simple, data-driven, table collator. | |
| --- | --- | --- | --- | --- | --- | --- |

The`Collator`class performs locale-sensitive`String`comparison. You use this class to build searching and sorting routines for natural language text.

`Collator`is an abstract base class. Subclasses implement specific collation strategies. One subclass,`RuleBasedCollator`, is currently provided with the Java Platform and is applicable to a wide set of languages. Other subclasses may be created to handle more specialized needs.

Like other locale-sensitive classes, you can use the static factory method,`getInstance`, to obtain the appropriate`Collator`object for a given locale. You will only need to look at the subclasses of`Collator`if you need to understand the details of a particular collation strategy or if you need to modify that strategy.

The following example shows how to compare two strings using the`Collator`for the default locale. 

```kotlin
<code>// Compare two strings in the default locale
  Collator myCollator = Collator.getInstance();
  if( myCollator.compare("abc", "ABC") &lt; 0 )
      System.out.println("abc is less than ABC");
  else
      System.out.println("abc is greater than or equal to ABC");
  </code>
```

You can set a`Collator`'s*strength* property to determine the level of difference considered significant in comparisons. Four strengths are provided:`PRIMARY`,`SECONDARY`,`TERTIARY`, and`IDENTICAL`. The exact assignment of strengths to language features is locale dependent. For example, in Czech, "e" and "f" are considered primary differences, while "e" and "ě" are secondary differences, "e" and "E" are tertiary differences and "e" and "e" are identical. The following shows how both case and accents could be ignored for US English. 

```kotlin
//Get the Collator for US English and set its strength to PRIMARY
  Collator usCollator = Collator.getInstance(Locale.US);
  usCollator.setStrength(Collator.PRIMARY);
  if( usCollator.compare("abc", "ABC") == 0 ) {
      System.out.println("Strings are equivalent");
  }
  
```

For comparing`String`s exactly once, the`compare`method provides the best performance. When sorting a list of`String`s however, it is generally necessary to compare each`String`multiple times. In this case,`CollationKey`s provide better performance. The`CollationKey`class converts a`String`to a series of bits that can be compared bitwise against other`CollationKey`s. A`CollationKey`is created by a`Collator`object for a given`String`. 
**Note:** `CollationKey`s from different`Collator`s can not be compared. See the class description for [CollationKey](../java/text/CollationKey.md) for an example using`CollationKey`s.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CANONICAL_DECOMPOSITION](../java/text/Collator.md) Decomposition mode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL_DECOMPOSITION](../java/text/Collator.md) Decomposition mode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDENTICAL](../java/text/Collator.md) Collator strength value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NO_DECOMPOSITION](../java/text/Collator.md) Decomposition mode value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PRIMARY](../java/text/Collator.md) Collator strength value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SECONDARY](../java/text/Collator.md) Collator strength value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TERTIARY](../java/text/Collator.md) Collator strength value. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [Collator](../java/text/Collator.md))`()` Default constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/text/Collator.md))`()` Returns a new collator with the same decomposition mode and strength value as this collator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](../java/text/Collator.md))`(`o1:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `o2:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Compares its two arguments for order. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compare](../java/text/Collator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Compares the source string to the target string according to the collation rules for this Collator. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/Collator.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the equality of two Collators. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/text/Collator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `target:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convenience method for comparing the equality of two strings based on this Collator's collation rules. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../java/text/Collator.md))`()` Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| --- | --- |
| abstract [CollationKey](../java/text/CollationKey.md)! | [getCollationKey](../java/text/Collator.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Transforms the String into a series of bits that can be compared bitwise to other CollationKeys. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDecomposition](../java/text/Collator.md))`()` Get the decomposition mode of this Collator. |
| openstatic [Collator](../java/text/Collator.md)! | [getInstance](../java/text/Collator.md))`()` Gets the Collator for the current default locale. |
| --- | --- |
| openstatic [Collator](../java/text/Collator.md)! | [getInstance](../java/text/Collator.md))`(`desiredLocale:` ` [Locale](../java/util/Locale.md)!`)` Gets the Collator for the desired locale. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrength](../java/text/Collator.md))`()` Returns this Collator's strength property. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/text/Collator.md))`()` Generates the hash code for this Collator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecomposition](../java/text/Collator.md))`(`decompositionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the decomposition mode of this Collator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrength](../java/text/Collator.md))`(`newStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this Collator's strength property. |

| Inherited functions ||
|---|---|
| From class [Comparator](../java/util/Comparator.md) |---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Comparator](../java/util/Comparator.md)<T>! | [reversed](../java/util/Comparator.md))`()` <br /> Returns a comparator that imposes the reverse ordering of this comparator. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`other:` ` [Comparator](../java/util/Comparator.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with another comparator. If this`Comparator`considers two elements equal, i.e.`compare(a, b) == 0`,`other`is used to determine the order. The returned comparator is serializable if the specified comparator is also serializable. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`keyExtractor:` ` [Function](../java/util/function/Function.md)<in` `T,` `out` `U>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`Comparable`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparing](../java/util/Comparator.md))`(`keyExtractor:` ` [Function](../java/util/function/Function.md)<in` `T,` `out` `U>!`, `keyComparator:` ` [Comparator](../java/util/Comparator.md)<in` `U>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a key to be compared with the given`Comparator`. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingDouble](../java/util/Comparator.md))`(`keyExtractor:` ` [ToDoubleFunction](../java/util/function/ToDoubleFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`double`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingInt](../java/util/Comparator.md))`(`keyExtractor:` ` [ToIntFunction](../java/util/function/ToIntFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts an`int`sort key. <br /> | | [Comparator](../java/util/Comparator.md)<T>! | [thenComparingLong](../java/util/Comparator.md))`(`keyExtractor:` ` [ToLongFunction](../java/util/function/ToLongFunction.md)<in` `T>!`)` <br /> Returns a lexicographic-order comparator with a function that extracts a`long`sort key. <br /> | ||

## Constants

### CANONICAL_DECOMPOSITION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANONICAL_DECOMPOSITION: Int
```

Decomposition mode value. With CANONICAL_DECOMPOSITION set, characters that are canonical variants according to Unicode standard will be decomposed for collation. This should be used to get correct collation of accented characters.

CANONICAL_DECOMPOSITION corresponds to Normalization Form D as described in [Unicode Standard Annex #15: Unicode Normalization Forms](http://www.unicode.org/reports/tr15/). 

 Value: 1

**See Also**

- [java.text.Collator#getDecomposition](../java/text/Collator.md))
- [java.text.Collator#setDecomposition](../java/text/Collator.md)) 

### FULL_DECOMPOSITION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FULL_DECOMPOSITION: Int
```

Decomposition mode value. With FULL_DECOMPOSITION set, both Unicode canonical variants and Unicode compatibility variants will be decomposed for collation. This causes not only accented characters to be collated, but also characters that have special formats to be collated with their norminal form. For example, the half-width and full-width ASCII and Katakana characters are then collated together. FULL_DECOMPOSITION is the most complete and therefore the slowest decomposition mode.

FULL_DECOMPOSITION corresponds to Normalization Form KD as described in [Unicode Standard Annex #15: Unicode Normalization Forms](http://www.unicode.org/reports/tr15/). 

 Value: 2

**See Also**

- [java.text.Collator#getDecomposition](../java/text/Collator.md))
- [java.text.Collator#setDecomposition](../java/text/Collator.md)) 

### IDENTICAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDENTICAL: Int
```

Collator strength value. When set, all differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for control characters ("\\u0001" vs "\\u0002") to be considered equal at the PRIMARY, SECONDARY, and TERTIARY levels but different at the IDENTICAL level. Additionally, differences between pre-composed accents such as "\\u00C0" (A-grave) and combining accents such as "A\\u0300" (A, combining-grave) will be considered significant at the IDENTICAL level if decomposition is set to NO_DECOMPOSITION. 

 Value: 3

### NO_DECOMPOSITION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_DECOMPOSITION: Int
```

Decomposition mode value. With NO_DECOMPOSITION set, accented characters will not be decomposed for collation. This is the default setting and provides the fastest collation but will only produce correct results for languages that do not use accents. 

 Value: 0

**See Also**

- [java.text.Collator#getDecomposition](../java/text/Collator.md))
- [java.text.Collator#setDecomposition](../java/text/Collator.md)) 

### PRIMARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIMARY: Int
```

Collator strength value. When set, only PRIMARY differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for different base letters ("a" vs "b") to be considered a PRIMARY difference. 

 Value: 0

**See Also**

- [java.text.Collator#setStrength](../java/text/Collator.md))
- [java.text.Collator#getStrength](../java/text/Collator.md)) 

### SECONDARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SECONDARY: Int
```

Collator strength value. When set, only SECONDARY and above differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for different accented forms of the same base letter ("a" vs "\\u00E4") to be considered a SECONDARY difference. 

 Value: 1

**See Also**

- [java.text.Collator#setStrength](../java/text/Collator.md))
- [java.text.Collator#getStrength](../java/text/Collator.md)) 

### TERTIARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TERTIARY: Int
```

Collator strength value. When set, only TERTIARY and above differences are considered significant during comparison. The assignment of strengths to language features is locale dependent. A common example is for case differences ("a" vs "A") to be considered a TERTIARY difference. 

 Value: 2

**See Also**

- [java.text.Collator#setStrength](../java/text/Collator.md))
- [java.text.Collator#getStrength](../java/text/Collator.md))

## Protected constructors

### Collator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Collator()
```

Default constructor. This constructor is protected so subclasses can get access to it. Users typically create a Collator sub-class by calling the factory method getInstance. 
**See Also**

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a new collator with the same decomposition mode and strength value as this collator.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this collator. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

**See Also**

- [java.lang.Cloneable](../java/lang/Cloneable.md) 

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compare(
    o1: Any!, 
    o2: Any!
): Int
```

Compares its two arguments for order. Returns a negative integer, zero, or a positive integer as the first argument is less than, equal to, or greater than the second.

This implementation merely returns`compare((String)o1, (String)o2) `.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------|
| `o1` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the first object to be compared. |
| `o2` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the second object to be compared. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as the first argument is less than, equal to, or greater than the second. |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if an argument is null and this comparator does not permit null arguments |
| `java.lang.ClassCastException` | the arguments cannot be cast to Strings. |

**See Also**

- [java.util.Comparator](../java/util/Comparator.md) 

### compare

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compare(
    source: String!, 
    target: String!
): Int
```

Compares the source string to the target string according to the collation rules for this Collator. Returns an integer less than, equal to or greater than zero depending on whether the source String is less than, equal to or greater than the target string. See the Collator class description for an example of use.

For a one time comparison, this method has the best performance. If a given String will be involved in multiple comparisons, CollationKey.compareTo has the best performance. See the Collator class description for an example using CollationKeys.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source string. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the target string. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Returns an integer value. Value is less than zero if source is less than target, value is zero if source and target are equal, value is greater than zero if source is greater than target. |

**See Also**

- [java.text.CollationKey](../java/text/CollationKey.md)
- [java.text.Collator#getCollationKey](../java/text/Collator.md)) 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the equality of two Collators.

| Parameters ||
|--------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `that` | the Collator to be compared with this. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Collator is the same as that Collator; false otherwise. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(
    source: String!, 
    target: String!
): Boolean
```

Convenience method for comparing the equality of two strings based on this Collator's collation rules.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the source string to be compared with. |
| `target` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the target string to be compared with. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the strings are equal according to the collation rules. false, otherwise. |

**See Also**

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | An array of locales for which localized`Collator`instances are available. |

### getCollationKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCollationKey(source: String!): CollationKey!
```

Transforms the String into a series of bits that can be compared bitwise to other CollationKeys. CollationKeys provide better performance than Collator.compare when Strings are involved in multiple comparisons. See the Collator class description for an example using CollationKeys.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be transformed into a collation key. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [CollationKey](../java/text/CollationKey.md)! | the CollationKey for the given String based on this Collator's collation rules. If the source String is null, a null CollationKey is returned. |

**See Also**

- [java.text.CollationKey](../java/text/CollationKey.md) 

### getDecomposition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecomposition(): Int
```

Get the decomposition mode of this Collator. Decomposition mode determines how Unicode composed characters are handled. Adjusting decomposition mode allows the user to select between faster and more complete collation behavior.

The three values for decomposition mode are:

- NO_DECOMPOSITION,
- CANONICAL_DECOMPOSITION
- FULL_DECOMPOSITION.

See the documentation for these three constants for a description of their meaning.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the decomposition mode |

**See Also**

- [java.text.Collator#setDecomposition](../java/text/Collator.md))
- [java.text.Collator#NO_DECOMPOSITION](../java/text/Collator.md)
- [java.text.Collator#CANONICAL_DECOMPOSITION](../java/text/Collator.md)
- [java.text.Collator#FULL_DECOMPOSITION](../java/text/Collator.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): Collator!
```

Gets the Collator for the current default locale. The default locale is determined by java.util.Locale.getDefault.

| Return ||
|---------------------------------------------------------------------------------|----------------------------------------------------------|
| [Collator](../java/text/Collator.md)! | the Collator for the default locale.(for example, en_US) |

**See Also**

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(desiredLocale: Locale!): Collator!
```

Gets the Collator for the desired locale.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `desiredLocale` | [Locale](../java/util/Locale.md)!:the desired locale. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------|
| [Collator](../java/text/Collator.md)! | the Collator for the desired locale. |

**See Also**

- [java.util.Locale](../java/util/Locale.md)
- [java.util.ResourceBundle](../java/util/ResourceBundle.md) 

### getStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStrength(): Int
```

Returns this Collator's strength property. The strength property determines the minimum level of difference considered significant during comparison. See the Collator class description for an example of use.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | this Collator's current strength property. |

**See Also**

- [java.text.Collator#setStrength](../java/text/Collator.md))
- [java.text.Collator#PRIMARY](../java/text/Collator.md)
- [java.text.Collator#SECONDARY](../java/text/Collator.md)
- [java.text.Collator#TERTIARY](../java/text/Collator.md)
- [java.text.Collator#IDENTICAL](../java/text/Collator.md) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hashCode(): Int
```

Generates the hash code for this Collator.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setDecomposition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecomposition(decompositionMode: Int): Unit
```

Set the decomposition mode of this Collator. See getDecomposition for a description of decomposition mode.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------|
| `decompositionMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new decomposition mode. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the given value is not a valid decomposition mode. |

**See Also**

- [java.text.Collator#getDecomposition](../java/text/Collator.md))
- [java.text.Collator#NO_DECOMPOSITION](../java/text/Collator.md)
- [java.text.Collator#CANONICAL_DECOMPOSITION](../java/text/Collator.md)
- [java.text.Collator#FULL_DECOMPOSITION](../java/text/Collator.md) 

### setStrength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrength(newStrength: Int): Unit
```

Sets this Collator's strength property. The strength property determines the minimum level of difference considered significant during comparison. See the Collator class description for an example of use.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------|
| `newStrength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new strength value. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the new strength value is not one of PRIMARY, SECONDARY, TERTIARY or IDENTICAL. |

**See Also**

- [java.text.Collator#getStrength](../java/text/Collator.md))
- [java.text.Collator#PRIMARY](../java/text/Collator.md)
- [java.text.Collator#SECONDARY](../java/text/Collator.md)
- [java.text.Collator#TERTIARY](../java/text/Collator.md)
- [java.text.Collator#IDENTICAL](../java/text/Collator.md)
