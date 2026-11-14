# NumberingSystem

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberingSystem

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/NumberingSystem "View this page in Java") 
| --- | --- |

```
open class NumberingSystem
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#) |

`NumberingSystem`is the base class for all number systems. This class provides the interface for setting different numbering system types, whether it be a simple alternate digit system such as Thai digits or Devanagari digits, or an algorithmic numbering system such as Hebrew numbering or Chinese numbering.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#NumberingSystem())`()` Default constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableNames](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getAvailableNames())`()` Returns a string array containing a list of the names of numbering systems currently known to ICU. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDescription](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getDescription())`()` Returns the description string of the current numbering system. |
| openstatic [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getInstance())`()` Returns the default numbering system for the default`FORMAT`locale. |
| --- | --- |
| openstatic [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns the default numbering system for the specified ULocale. |
| openstatic [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getInstance(kotlin.Int,%20kotlin.Boolean,%20kotlin.String))`(`radix_in:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isAlgorithmic_in:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `desc_in:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Factory method for creating a numbering system. |
| openstatic [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns the default numbering system for the specified locale. |
| --- | --- |
| openstatic [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [getInstanceByName](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getInstanceByName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a numbering system from one of the predefined numbering systems known to ICU. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getName())`()` Returns the string representing the name of the numbering system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRadix](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#getRadix())`()` Returns the radix of the current numbering system. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAlgorithmic](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#isAlgorithmic())`()` Returns the numbering system's algorithmic status. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidDigitString](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#isValidDigitString(kotlin.String))`(`str:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convenience method to determine if a given digit string is valid for use as a descriptor of a numeric ( non-algorithmic ) numbering system. |

| Properties ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | [LATIN](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#LATIN:android.icu.text.NumberingSystem) For convenience, an instance representing the*latn*numbering system, which corresponds to digits in the ASCII range '0' through '9'. |

## Public constructors

### NumberingSystem

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NumberingSystem()
```

Default constructor. Returns a numbering system that uses the Latin-script decimal digits 0 through 9. This should be equivalent to NumberingSystem.LATIN.

## Public methods

### getAvailableNames

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableNames(): Array<String!>!
```

Returns a string array containing a list of the names of numbering systems currently known to ICU.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | An array of strings in alphabetical (invariant) order. |

### getDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescription(): String!
```

Returns the description string of the current numbering system. The description string describes the characteristics of the numbering system. For numeric systems, this string contains the digits used by the numbering system, in order, starting from zero. For algorithmic numbering systems, the string contains the name of the RBNF ruleset in the locale's NumberingSystemRules section that will be used to format numbers using this numbering system. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): NumberingSystem!
```

Returns the default numbering system for the default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): NumberingSystem!
```

Returns the default numbering system for the specified ULocale. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    radix_in: Int, 
    isAlgorithmic_in: Boolean, 
    desc_in: String!
): NumberingSystem!
```

Factory method for creating a numbering system.

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `radix_in` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The radix for this numbering system. ICU currently supports only numbering systems whose radix is 10. |
| `isAlgorithmic_in` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Specifies whether the numbering system is algorithmic (true) or numeric (false). |
| `desc_in` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:String used to describe the characteristics of the numbering system. For numeric systems, this string contains the digits used by the numbering system, in order, starting from zero. For algorithmic numbering systems, the string contains the name of the RBNF ruleset in the locale's NumberingSystemRules section that will be used to format numbers using this numbering system. |
| --- | --- |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: Locale!): NumberingSystem!
```

Returns the default numbering system for the specified locale. 

### getInstanceByName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstanceByName(name: String!): NumberingSystem!
```

Returns a numbering system from one of the predefined numbering systems known to ICU. Numbering system names are based on the numbering systems defined in CLDR. To get a list of available numbering systems, use the getAvailableNames method.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the desired numbering system. Numbering system names often correspond with the name of the script they are associated with. For example, "thai" for Thai digits, "hebr" for Hebrew numerals. |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem#)! | The NumberingSystem instance, or null if not available. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(): String!
```

Returns the string representing the name of the numbering system. 

### getRadix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRadix(): Int
```

Returns the radix of the current numbering system. 

### isAlgorithmic

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAlgorithmic(): Boolean
```

Returns the numbering system's algorithmic status. If true, the numbering system is algorithmic and uses an RBNF formatter to format numerals. If false, the numbering system is numeric and uses a fixed set of digits. 

### isValidDigitString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isValidDigitString(str: String!): Boolean
```

Convenience method to determine if a given digit string is valid for use as a descriptor of a numeric ( non-algorithmic ) numbering system. In order for a digit string to be valid, it must contain exactly ten Unicode code points.

## Properties

### LATIN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LATIN: NumberingSystem!
```

For convenience, an instance representing the*latn*numbering system, which corresponds to digits in the ASCII range '0' through '9'.
