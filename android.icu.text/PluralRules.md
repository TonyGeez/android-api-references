# PluralRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PluralRules

Kotlin| [Java](PluralRules.md) 
| --- | --- |

```
open class PluralRules : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.PluralRules](PluralRules.md) |

Defines rules for mapping non-negative numeric values onto a small set of keywords.

Rules are constructed from a text description, consisting of a series of keywords and conditions. The #select method examines each condition in order and returns the keyword for the first condition that matches the number. If none match, [KEYWORD_OTHER](PluralRules.md) is returned.

A PluralRules object is immutable. It contains caches for sample values, but those are synchronized.

PluralRules is Serializable so that it can be used in formatters, which are serializable.

For more information, details, and tips for writing rules, see the [LDML spec, Part 3.5 Language Plural Rules](https://www.unicode.org/reports/tr35/tr35-numbers.html#Language_Plural_Rules)

Examples: 

```kotlin
"one: n is 1; few: n in 2..4"
  
```

This defines two rules, for 'one' and 'few'. The condition for 'one' is "n is 1" which means that the number must be equal to 1 for this condition to pass. The condition for 'few' is "n in 2..4" which means that the number must be between 2 and 4 inclusive - and be an integer - for this condition to pass. All other numbers are assigned the keyword "other" by the default rule. 

```kotlin
"zero: n is 0; one: n is 1; zero: n mod 100 in 1..19"
  
```

This illustrates that the same keyword can be defined multiple times. Each rule is examined in order, and the first keyword whose condition passes is the one returned. Also notes that a modulus is applied to n in the last rule. Thus its condition holds for 119, 219, 319... 

```kotlin
"one: n is 1; few: n mod 10 in 2..4 and n mod 100 not in 12..14"
  
```

This illustrates conjunction and negation. The condition for 'few' has two parts, both of which must be met: "n mod 10 in 2..4" and "n mod 100 not in 12..14". The first part applies a modulus to n before the test as in the previous example. The second part applies a different modulus and also uses negation, thus it matches all numbers*not*in 12, 13, 14, 112, 113, 114, 212, 213, 214...

Syntax: 

```kotlin
rules         = rule (';' rule)*
  rule          = keyword ':' condition
  keyword       = <identifier>
  condition     = and_condition ('or' and_condition)*
  and_condition = relation ('and' relation)*
  relation      = not? expr not? rel not? range_list
  expr          = ('n' | 'i' | 'f' | 'v' | 't') (mod value)?
  not           = 'not' | '!'
  rel           = 'in' | 'is' | '=' | '≠' | 'within'
  mod           = 'mod' | '%'
  range_list    = (range | value) (',' range_list)*
  value         = digit+
  digit         = 0|1|2|3|4|5|6|7|8|9
  range         = value'..'value
  
```

Each**not**term inverts the meaning; however, there should not be more than one of them.

The i, f, t, and v values are defined as follows:

- i to be the integer digits.
- f to be the visible decimal digits, as an integer.
- t to be the visible decimal digits---without trailing zeros---as an integer.
- v to be the number of visible fraction digits.
- j is defined to only match integers. That is j is 3 fails if v != 0 (eg for 3.1 or 3.0).

Examples are in the following table:

| n | i | f | v |
|------|---|----|---|
| 1.0 | 1 | 0 | 1 |
| 1.00 | 1 | 0 | 2 |
| 1.3 | 1 | 3 | 1 |
| --- | --- | --- | --- |
| 1.03 | 1 | 3 | 2 |
| 1.23 | 1 | 23 | 2 |

An "identifier" is a sequence of characters that do not have the Unicode Pattern_Syntax or Pattern_White_Space properties.

The difference between 'in' and 'within' is that 'in' only includes integers in the specified range, while 'within' includes all values. Using 'within' with a range_list consisting entirely of values is the same as using 'in' (it's not an error).

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------|
| | [PluralType](../android/icu/text/PluralRules.PluralType.md) Type of plurals and PluralRules. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_FEW](PluralRules.md) Common name for the 'paucal' or other special plural form. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_MANY](PluralRules.md) Common name for the arabic (11 to 99) plural form. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_ONE](PluralRules.md) Common name for the 'singular' plural form. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_OTHER](PluralRules.md) Common name for the default plural form. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_TWO](PluralRules.md) Common name for the 'dual' plural form. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [KEYWORD_ZERO](PluralRules.md) Common name for the 'zero' plural form. |
| --- | --- |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [NO_UNIQUE_VALUE](PluralRules.md) Value returned by [getUniqueKeywordValue](PluralRules.md))when there is no unique value to return. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [PluralRules](PluralRules.md)! | [createRules](PluralRules.md))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a PluralRules from a description if it is parsable, otherwise returns null. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PluralRules.md))`(`rhs:` ` [PluralRules](PluralRules.md)!`)` Returns true if rhs is equal to this. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PluralRules.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| openstatic [PluralRules](PluralRules.md)! | [forLocale](PluralRules.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`)` Provides access to the predefined cardinal-number`PluralRules`for a given locale. |
| openstatic [PluralRules](PluralRules.md)! | [forLocale](PluralRules.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)!`, `type:` ` [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!`)` Provides access to the predefined`PluralRules`for a given locale and the plural type. |
| openstatic [PluralRules](PluralRules.md)! | [forLocale](PluralRules.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`)` Provides access to the predefined cardinal-number`PluralRules`for a given [java.util.Locale](../java.util/Locale.md). |
| --- | --- |
| openstatic [PluralRules](PluralRules.md)! | [forLocale](PluralRules.md))`(`locale:` ` [Locale](../java.util/Locale.md)!`, `type:` ` [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!`)` Provides access to the predefined`PluralRules`for a given [java.util.Locale](../java.util/Locale.md) and the plural type. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | [getAllKeywordValues](PluralRules.md))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns all the values that trigger this keyword, or null if the number of such values is unlimited. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getKeywords](PluralRules.md))`()` Returns a set of all rule keywords used in this`PluralRules`object. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!\>! | [getSamples](PluralRules.md))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a list of integer values for which select() would return that keyword, or null if the keyword is not defined. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getUniqueKeywordValue](PluralRules.md))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the unique value that this keyword matches, or [NO_UNIQUE_VALUE](PluralRules.md) if the keyword matches multiple values or is not defined for this PluralRules. |
| openstatic [PluralRules](PluralRules.md)! | [parseDescription](PluralRules.md))`(`description:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses a plural rules description and returns a PluralRules. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [select](PluralRules.md))`(`number:` ` [FormattedNumber](../android.icu.number/FormattedNumber.md)!`)` Given a formatted number, returns the keyword of the first rule that applies to the number. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [select](PluralRules.md))`(`range:` ` [FormattedNumberRange](../android.icu.number/FormattedNumberRange.md)!`)` Given a formatted number range, returns the overall plural form of the range. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [select](PluralRules.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Given a floating-point number, returns the keyword of the first rule that applies to the number. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PluralRules.md))`()` Returns a string representation of the object. |

| Properties ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [PluralRules](PluralRules.md)! | [DEFAULT](PluralRules.md) The default rules that accept any number and return [KEYWORD_OTHER](PluralRules.md). |

## Constants

### KEYWORD_FEW

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_FEW: String
```

Common name for the 'paucal' or other special plural form. 

 Value: "few"

### KEYWORD_MANY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_MANY: String
```

Common name for the arabic (11 to 99) plural form. 

 Value: "many"

### KEYWORD_ONE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_ONE: String
```

Common name for the 'singular' plural form. 

 Value: "one"

### KEYWORD_OTHER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_OTHER: String
```

Common name for the default plural form. This name is returned for values to which no other form in the rule applies. It can additionally be assigned rules of its own. 

 Value: "other"

### KEYWORD_TWO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_TWO: String
```

Common name for the 'dual' plural form. 

 Value: "two"

### KEYWORD_ZERO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KEYWORD_ZERO: String
```

Common name for the 'zero' plural form. 

 Value: "zero"

### NO_UNIQUE_VALUE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_UNIQUE_VALUE: Double
```

Value returned by [getUniqueKeywordValue](PluralRules.md))when there is no unique value to return. 

 Value: -0.00123456777

## Public methods

### createRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createRules(description: String!): PluralRules!
```

Creates a PluralRules from a description if it is parsable, otherwise returns null.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the rule description. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------|
| [PluralRules](PluralRules.md)! | the PluralRules |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(rhs: PluralRules!): Boolean
```

Returns true if rhs is equal to this.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [PluralRules](PluralRules.md)!:the PluralRules to compare to. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this and rhs are equal. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### forLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forLocale(locale: ULocale!): PluralRules!
```

Provides access to the predefined cardinal-number`PluralRules`for a given locale. Same as forLocale(locale, PluralType.CARDINAL).

ICU defines plural rules for many locales based on CLDR*Language Plural Rules*. For these predefined rules, see CLDR page at https://unicode-org.github.io/cldr-staging/charts/latest/supplemental/language_plural_rules.html

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:The locale for which a`PluralRules`object is returned. |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PluralRules](PluralRules.md)! | The predefined`PluralRules`object for this locale. If there's no predefined rules for this locale, the rules for the closest parent in the locale hierarchy that has one will be returned. The final fallback always returns the default rules. |

### forLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forLocale(
    locale: ULocale!, 
    type: PluralRules.PluralType!
): PluralRules!
```

Provides access to the predefined`PluralRules`for a given locale and the plural type.

ICU defines plural rules for many locales based on CLDR*Language Plural Rules*. For these predefined rules, see CLDR page at https://unicode-org.github.io/cldr-staging/charts/latest/supplemental/language_plural_rules.html

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!:The locale for which a`PluralRules`object is returned. |
| `type` | [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!:The plural type (e.g., cardinal or ordinal). |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PluralRules](PluralRules.md)! | The predefined`PluralRules`object for this locale. If there's no predefined rules for this locale, the rules for the closest parent in the locale hierarchy that has one will be returned. The final fallback always returns the default rules. |

### forLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forLocale(locale: Locale!): PluralRules!
```

Provides access to the predefined cardinal-number`PluralRules`for a given [java.util.Locale](../java.util/Locale.md). Same as forLocale(locale, PluralType.CARDINAL).

ICU defines plural rules for many locales based on CLDR*Language Plural Rules*. For these predefined rules, see CLDR page at https://unicode-org.github.io/cldr-staging/charts/latest/supplemental/language_plural_rules.html

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:The locale for which a`PluralRules`object is returned. |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PluralRules](PluralRules.md)! | The predefined`PluralRules`object for this locale. If there's no predefined rules for this locale, the rules for the closest parent in the locale hierarchy that has one will be returned. The final fallback always returns the default rules. |

### forLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forLocale(
    locale: Locale!, 
    type: PluralRules.PluralType!
): PluralRules!
```

Provides access to the predefined`PluralRules`for a given [java.util.Locale](../java.util/Locale.md) and the plural type.

ICU defines plural rules for many locales based on CLDR*Language Plural Rules*. For these predefined rules, see CLDR page at https://unicode-org.github.io/cldr-staging/charts/latest/supplemental/language_plural_rules.html

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java.util/Locale.md)!:The locale for which a`PluralRules`object is returned. |
| `type` | [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!:The plural type (e.g., cardinal or ordinal). |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PluralRules](PluralRules.md)! | The predefined`PluralRules`object for this locale. If there's no predefined rules for this locale, the rules for the closest parent in the locale hierarchy that has one will be returned. The final fallback always returns the default rules. |

### getAllKeywordValues

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAllKeywordValues(keyword: String!): MutableCollection<Double!>!
```

Returns all the values that trigger this keyword, or null if the number of such values is unlimited.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!>! | the values that trigger this keyword, or null. The returned collection is immutable. It will be empty if the keyword is not defined. |

### getKeywords

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeywords(): MutableSet<String!>!
```

Returns a set of all rule keywords used in this`PluralRules`object. The rule "other" is always present by default.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The set of keywords. |

### getSamples

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSamples(keyword: String!): MutableCollection<Double!>!
```

Returns a list of integer values for which select() would return that keyword, or null if the keyword is not defined. The returned collection is unmodifiable. The returned list is not complete, and there might be additional values that would return the keyword.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to test |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)!>! | a list of values matching the keyword. |

### getUniqueKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUniqueKeywordValue(keyword: String!): Double
```

Returns the unique value that this keyword matches, or [NO_UNIQUE_VALUE](PluralRules.md) if the keyword matches multiple values or is not defined for this PluralRules.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to check for a unique value |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | The unique value for the keyword, or NO_UNIQUE_VALUE. |

### parseDescription

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parseDescription(description: String!): PluralRules!
```

Parses a plural rules description and returns a PluralRules.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `description` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the rule description. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------------------------------|
| `java.text.ParseException` | if the description cannot be parsed. The exception index is typically not set, it will be -1. |

### select

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun select(number: FormattedNumber!): String!
```

Given a formatted number, returns the keyword of the first rule that applies to the number. A FormattedNumber allows you to specify an exponent or trailing zeros, which can affect the plural category. To get a FormattedNumber, see [NumberFormatter](../android.icu.number/NumberFormatter.md).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [FormattedNumber](../android.icu.number/FormattedNumber.md)!:The number for which the rule has to be determined. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The keyword of the selected rule. |

### select

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun select(range: FormattedNumberRange!): String!
```

Given a formatted number range, returns the overall plural form of the range. For example, "3-5" returns "other" in English. To get a FormattedNumberRange, see [android.icu.number.NumberRangeFormatter](../android.icu.number/NumberRangeFormatter.md). This method only works if PluralRules was created with a locale. If it was created from PluralRules.createRules(), or if it was deserialized, this method throws UnsupportedOperationException.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `range` | [FormattedNumberRange](../android.icu.number/FormattedNumberRange.md)!:The number range onto which the rules will be applied. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The keyword of the selected rule. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If called on an instance without plural ranges data. |

### select

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun select(number: Double): String!
```

Given a floating-point number, returns the keyword of the first rule that applies to the number.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The number for which the rule has to be determined. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The keyword of the selected rule. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### DEFAULT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT: PluralRules!
```

The default rules that accept any number and return [KEYWORD_OTHER](PluralRules.md).
