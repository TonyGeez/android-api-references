# PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PluralFormat

Kotlin| [Java](../android/icu/text/PluralFormat.md) 
| --- | --- |

```
open class PluralFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](../java/text/Format.md) |||
| | ↳ | [android.icu.text.UFormat](../android/icu/text/UFormat.md) ||
| | | ↳ | [android.icu.text.PluralFormat](../android/icu/text/PluralFormat.md) |
| --- | --- | --- | --- |

`PluralFormat`supports the creation of internationalized messages with plural inflection. It is based on*plural selection* , i.e. the caller specifies messages for each plural case that can appear in the user's language and the`PluralFormat`selects the appropriate message based on the number.

### The Problem of Plural Forms in Internationalized Messages

<br />

Different languages have different ways to inflect plurals. Creating internationalized messages that include plural forms is only feasible when the framework is able to handle plural forms of*all* languages correctly.`ChoiceFormat`doesn't handle this well, because it attaches a number interval to each message and selects the message whose interval contains a given number. This can only handle a finite number of intervals. But in some languages, like Polish, one plural case applies to infinitely many intervals (e.g., the paucal case applies to numbers ending with 2, 3, or 4 except those ending with 12, 13, or 14). Thus`ChoiceFormat`is not adequate.

`PluralFormat`deals with this by breaking the problem into two parts:

- It uses`PluralRules`that can define more complex conditions for a plural case than just a single interval. These plural rules define both what plural cases exist in a language, and to which numbers these cases apply.
- It provides predefined plural rules for many languages. Thus, the programmer need not worry about the plural cases of a language and does not have to define the plural cases; they can simply use the predefined keywords. The whole plural formatting of messages can be done using localized patterns from resource bundles. For predefined plural rules, see the CLDR*Language Plural Rules*page at https://unicode-org.github.io/cldr-staging/charts/latest/supplemental/language_plural_rules.html

#### Usage of`PluralFormat`

Note: Typically, plural formatting is done via`MessageFormat`with a`plural`argument type, rather than using a stand-alone`PluralFormat`.

This discussion assumes that you use`PluralFormat`with a predefined set of plural rules. You can create one using one of the constructors that takes a`ULocale`object. To specify the message pattern, you can either pass it to the constructor or set it explicitly using the`applyPattern()`method. The`format()`method takes a number object and selects the message of the matching plural case. This message will be returned.

##### Patterns and Their Interpretation

The pattern text defines the message output for each plural case of the specified locale. Syntax: 

```kotlin
pluralStyle = [offsetValue] (selector '{' message '}')+
  offsetValue = "offset:" number
  selector = explicitValue | keyword
  explicitValue = '=' number  // adjacent, no white space in between
  keyword = [^[[:Pattern_Syntax:][:Pattern_White_Space:]]]+
  message: see <code><a docref="android.icu.text.MessageFormat">MessageFormat</a></code>
```
Pattern_White_Space between syntax elements is ignored, except between the {curly braces} and their sub-message, and between the '=' and the number of an explicitValue.

There are 6 predefined case keywords in CLDR/ICU - 'zero', 'one', 'two', 'few', 'many' and 'other'. You always have to define a message text for the default plural case "`other`" which is contained in every rule set. If you do not specify a message text for a particular plural case, the message text of the plural case "`other`" gets assigned to this plural case.

When formatting, the input number is first matched against the explicitValue clauses. If there is no exact-number match, then a keyword is selected by calling the`PluralRules`with the input number*minus the offset*. (The offset defaults to 0 if it is omitted from the pattern string.) If there is no clause with that keyword, then the "other" clauses is returned.

An unquoted pound sign () in the selected sub-message itself (i.e., outside of arguments nested in the sub-message) is replaced by the input number minus the offset. The number-minus-offset value is formatted using a`NumberFormat`for the`PluralFormat`'s locale. If you need special number formatting, you have to use a`MessageFormat`and explicitly specify a`NumberFormat`argument.**Note:**That argument is formatting without subtracting the offset! If you need a custom format and have a non-zero offset, then you need to pass the number-minus-offset value as a separate parameter.

For a usage example, see the [MessageFormat](../android/icu/text/MessageFormat.md) class documentation.

#### Defining Custom Plural Rules

If you need to use`PluralFormat`with custom rules, you can create a`PluralRules`object and pass it to`PluralFormat`'s constructor. If you also specify a locale in this constructor, this locale will be used to format the number in the message texts.

For more information about`PluralRules`, see [PluralRules](../android/icu/text/PluralRules.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PluralFormat](../android/icu/text/PluralFormat.md))`()` Creates a new cardinal-number`PluralFormat`for the default`FORMAT`locale. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`rules:` ` [PluralRules](../android/icu/text/PluralRules.md)!`)` Creates a new cardinal-number`PluralFormat`for a given set of rules. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`rules:` ` [PluralRules](../android/icu/text/PluralRules.md)!`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new cardinal-number`PluralFormat`for a given set of rules and a pattern. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Creates a new cardinal-number`PluralFormat`for a given locale. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `rules:` ` [PluralRules](../android/icu/text/PluralRules.md)!`)` Creates a new cardinal-number`PluralFormat`for a given set of rules. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `rules:` ` [PluralRules](../android/icu/text/PluralRules.md)!`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new cardinal-number`PluralFormat`for a given set of rules, a pattern and a locale. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `type:` ` [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!`)` Creates a new`PluralFormat`for the plural type. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `type:` ` [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`PluralFormat`for a plural type, a pattern and a locale. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`ulocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new cardinal-number`PluralFormat`for a given pattern string and locale. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new cardinal-number`PluralFormat`for a given pattern string. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Creates a new cardinal-number`PluralFormat`for a given [java.util.Locale](../java/util/Locale.md). |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `rules:` ` [PluralRules](../android/icu/text/PluralRules.md)!`)` Creates a new cardinal-number`PluralFormat`for a given set of rules. |
| [PluralFormat](../android/icu/text/PluralFormat.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `type:` ` [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!`)` Creates a new`PluralFormat`for the plural type. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](../android/icu/text/PluralFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the pattern used by this plural format. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/PluralFormat.md))`(`rhs:` ` [PluralFormat](../android/icu/text/PluralFormat.md)!`)` Returns true if this equals the provided PluralFormat. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/PluralFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/PluralFormat.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Formats a plural message for a given number. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/PluralFormat.md))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats a plural message for a given number and appends the formatted message to the given`StringBuffer`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/text/PluralFormat.md))`()` Returns a hash code value for the object. |
| --- | --- |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [parse](../android/icu/text/PluralFormat.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsePosition:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` This method is not yet supported by`PluralFormat`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../android/icu/text/PluralFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` This method is not yet supported by`PluralFormat`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNumberFormat](../android/icu/text/PluralFormat.md))`(`format:` ` [NumberFormat](../android/icu/text/NumberFormat.md)!`)` Sets the number format used by this formatter. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](../android/icu/text/PluralFormat.md))`()` Returns the pattern for this PluralFormat. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/text/PluralFormat.md))`()` Returns a string representation of the object. |

## Public constructors

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat()
```

Creates a new cardinal-number`PluralFormat`for the default`FORMAT`locale. This locale will be used to get the set of plural rules and for standard number formatting. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(rules: PluralRules!)
```

Creates a new cardinal-number`PluralFormat`for a given set of rules. The standard number formatting will be done using the default`FORMAT`locale.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `rules` | [PluralRules](../android/icu/text/PluralRules.md)!:defines the behavior of the`PluralFormat`object. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    rules: PluralRules!, 
    pattern: String!)
```

Creates a new cardinal-number`PluralFormat`for a given set of rules and a pattern. The standard number formatting will be done using the default`FORMAT`locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `rules` | [PluralRules](../android/icu/text/PluralRules.md)!:defines the behavior of the`PluralFormat`object. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this`PluralFormat`. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(ulocale: ULocale!)
```

Creates a new cardinal-number`PluralFormat`for a given locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the`PluralFormat`will be configured with rules for this locale. This locale will also be used for standard number formatting. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    ulocale: ULocale!, 
    rules: PluralRules!)
```

Creates a new cardinal-number`PluralFormat`for a given set of rules. The standard number formatting will be done using the given locale.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the default number formatting will be done using this locale. |
| `rules` | [PluralRules](../android/icu/text/PluralRules.md)!:defines the behavior of the`PluralFormat`object. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    ulocale: ULocale!, 
    rules: PluralRules!, 
    pattern: String!)
```

Creates a new cardinal-number`PluralFormat`for a given set of rules, a pattern and a locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the`PluralFormat`will be configured with rules for this locale. This locale will also be used for standard number formatting. |
| `rules` | [PluralRules](../android/icu/text/PluralRules.md)!:defines the behavior of the`PluralFormat`object. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this`PluralFormat`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    ulocale: ULocale!, 
    type: PluralRules.PluralType!)
```

Creates a new`PluralFormat`for the plural type. The standard number formatting will be done using the given locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the default number formatting will be done using this locale. |
| `type` | [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!:The plural type (e.g., cardinal or ordinal). |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    ulocale: ULocale!, 
    type: PluralRules.PluralType!, 
    pattern: String!)
```

Creates a new`PluralFormat`for a plural type, a pattern and a locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the`PluralFormat`will be configured with rules for this locale. This locale will also be used for standard number formatting. |
| `type` | [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!:The plural type (e.g., cardinal or ordinal). |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this`PluralFormat`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    ulocale: ULocale!, 
    pattern: String!)
```

Creates a new cardinal-number`PluralFormat`for a given pattern string and locale. The locale will be used to get the set of plural rules and for standard number formatting.

Example code:

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ulocale` | [ULocale](../android/icu/util/ULocale.md)!:the`PluralFormat`will be configured with rules for this locale. This locale will also be used for standard number formatting. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this`PluralFormat`. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(pattern: String!)
```

Creates a new cardinal-number`PluralFormat`for a given pattern string. The default`FORMAT`locale will be used to get the set of plural rules and for standard number formatting.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this`PluralFormat`. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(locale: Locale!)
```

Creates a new cardinal-number`PluralFormat`for a given [java.util.Locale](../java/util/Locale.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the`PluralFormat`will be configured with rules for this locale. This locale will also be used for standard number formatting. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    locale: Locale!, 
    rules: PluralRules!)
```

Creates a new cardinal-number`PluralFormat`for a given set of rules. The standard number formatting will be done using the given locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the default number formatting will be done using this locale. |
| `rules` | [PluralRules](../android/icu/text/PluralRules.md)!:defines the behavior of the`PluralFormat`object. |

### PluralFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PluralFormat(
    locale: Locale!, 
    type: PluralRules.PluralType!)
```

Creates a new`PluralFormat`for the plural type. The standard number formatting will be done using the given [java.util.Locale](../java/util/Locale.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the default number formatting will be done using this locale. |
| `type` | [PluralRules.PluralType](../android/icu/text/PluralRules.PluralType.md)!:The plural type (e.g., cardinal or ordinal). |

## Public methods

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pattern: String!): Unit
```

Sets the pattern used by this plural format. The method parses the pattern and creates a map of format strings for the plural rules. Patterns and their interpretation are specified in the class description.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the pattern for this plural format. |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if the pattern is invalid. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(rhs: PluralFormat!): Boolean
```

Returns true if this equals the provided PluralFormat.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| `rhs` | [PluralFormat](../android/icu/text/PluralFormat.md)!:the PluralFormat to compare against |

| Return ||
|------------------------------------------------------------------------------------|-------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this equals rhs |

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

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Double): String!
```

Formats a plural message for a given number.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a number for which the plural message should be formatted. If no pattern has been applied to this`PluralFormat`object yet, the formatted number will be returned. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string containing the formatted plural message. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Any!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats a plural message for a given number and appends the formatted message to the given`StringBuffer`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | [StringBuffer](../java/lang/StringBuffer.md)!:the formatted message will be appended to this`StringBuffer`. |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:will be ignored by this method. |
| --- | --- |
| `number` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:a number object (instance of`Number`for which the plural message should be formatted. If no pattern has been applied to this`PluralFormat`object yet, the formatted number will be returned. Note: If this object is not an instance of`Number`, the`toAppendTo`will not be modified. |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](../java/lang/StringBuffer.md)! | the string buffer passed in as toAppendTo, with formatted text appended. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if number is not an instance of Number |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](../java/util/HashMap.md).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](../java/lang/Object.md))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    text: String!, 
    parsePosition: ParsePosition!
): Number!
```

This method is not yet supported by`PluralFormat`.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be parsed. |
| `parsePosition` | [ParsePosition](../java/text/ParsePosition.md)!:defines the position where parsing is to begin, and upon return, the position where parsing left off. If the position has not changed upon return, then parsing failed. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | nothing because this method is not yet implemented. |

| Exceptions ||
|-------------------------------------------|---------------------------------------|
| `java.lang.UnsupportedOperationException` | will always be thrown by this method. |

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseObject(
    source: String!, 
    pos: ParsePosition!
): Any!
```

This method is not yet supported by`PluralFormat`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string to be parsed. |
| `pos` | [ParsePosition](../java/text/ParsePosition.md)!:defines the position where parsing is to begin, and upon return, the position where parsing left off. If the position has not changed upon return, then parsing failed. |

| Return ||
|-----------------------------------------------------------------------------|-----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | nothing because this method is not yet implemented. |

| Exceptions ||
|-------------------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |
| `java.lang.UnsupportedOperationException` | will always be thrown by this method. |

### setNumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumberFormat(format: NumberFormat!): Unit
```

Sets the number format used by this formatter. You only need to call this if you want a different number format than the default formatter for the locale.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `format` | [NumberFormat](../android/icu/text/NumberFormat.md)!:the number format to use. |

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Returns the pattern for this PluralFormat.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern string |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
