Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalFormatSymbols

```
open class DecimalFormatSymbols : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.text.DecimalFormatSymbols](DecimalFormatSymbols.md) |

This class represents the set of symbols (such as the decimal separator, the grouping separator, and so on) needed by `DecimalFormat` to format numbers. `DecimalFormat` creates for itself an instance of `DecimalFormatSymbols` from its locale data. If you need to change any of these symbols, you can get the `DecimalFormatSymbols` object from your `DecimalFormat` and modify it.

## Summary

| Public constructors ||
|---|---|
| DecimalFormatSymbols Create a DecimalFormatSymbols object for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#` locale. |
| DecimalFormatSymbols Create a DecimalFormatSymbols object for the given locale. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | clone Standard override. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Override equals. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java.util/Locale.md)!\>! | getAvailableLocales Returns an array of all locales for which the `getInstance` methods of this class can return localized instances. |
| --- | --- |
| open [Currency](../java.util/Currency.md)! | getCurrency Gets the currency of these DecimalFormatSymbols. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCurrencySymbol Returns the currency symbol for the currency of these DecimalFormatSymbols in their locale. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getDecimalSeparator Gets the character used for decimal sign. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getDigit Gets the character used for a digit in a pattern. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getExponentSeparator Returns the string used to separate the mantissa from the exponent. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getGroupingSeparator Gets the character used for grouping separator. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getInfinity Gets the string used to represent infinity. |
| static [DecimalFormatSymbols](DecimalFormatSymbols.md)! | getInstance Gets the `DecimalFormatSymbols` instance for the default locale. |
| static [DecimalFormatSymbols](DecimalFormatSymbols.md)! | getInstance Gets the `DecimalFormatSymbols` instance for the specified locale. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getInternationalCurrencySymbol Returns the ISO 4217 currency code of the currency of these DecimalFormatSymbols. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getMinusSign Gets the character used to represent minus sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getMonetaryDecimalSeparator Returns the monetary decimal separator. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getMonetaryGroupingSeparator Gets the character used for grouping separator for currencies. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getNaN Gets the string used to represent "not a number". |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getPatternSeparator Gets the character used to separate positive and negative subpatterns in a pattern. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getPerMill Gets the character used for per mille sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getPercent Gets the character used for percent sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | getZeroDigit Gets the character used for zero. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Override hashCode. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCurrency Sets the currency of these DecimalFormatSymbols. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCurrencySymbol Sets the currency symbol for the currency of these DecimalFormatSymbols in their locale. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDecimalSeparator Sets the character used for decimal sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDigit Sets the character used for a digit in a pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExponentSeparator Sets the string used to separate the mantissa from the exponent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setGroupingSeparator Sets the character used for grouping separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInfinity Sets the string used to represent infinity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setInternationalCurrencySymbol Sets the ISO 4217 currency code of the currency of these DecimalFormatSymbols. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMinusSign Sets the character used to represent minus sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMonetaryDecimalSeparator Sets the monetary decimal separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMonetaryGroupingSeparator Sets the character used for grouping separator for currencies. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setNaN Sets the string used to represent "not a number". |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPatternSeparator Sets the character used to separate positive and negative subpatterns in a pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPerMill Sets the character used for per mille sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPercent Sets the character used for percent sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setZeroDigit Sets the character used for zero. |

## Public constructors

### DecimalFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormatSymbols()
```

Create a DecimalFormatSymbols object for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#` locale. It is recommended that the getInstance method is used instead.

This is equivalent to calling DecimalFormatSymbols.
**See Also**

- getDefault
- `https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#`

### DecimalFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormatSymbols(locale: Locale!)
```

Create a DecimalFormatSymbols object for the given locale. It is recommended that the getInstance method is used instead. If the specified locale contains the `https://developer.android.com/reference/kotlin/java/util/Locale.html#UNICODE_LOCALE_EXTENSION:kotlin.Char` for the numbering system, the instance is initialized with the specified numbering system if the JRE implementation supports it. For example,

```kotlin
NumberFormat.getNumberInstance(Locale.forLanguageTag("th-TH-u-nu-thai"))
  
```
This may return a `NumberFormat` instance with the Thai numbering system, instead of the Latin numbering system.

<br />

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the desired locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `locale` is null |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Standard override.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Override equals.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAvailableLocales

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the `getInstance` methods of this class can return localized instances. It must contain at least a `Locale` instance equal to `https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | an array of locales for which localized `DecimalFormatSymbols` instances are available. |

### getCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrency(): Currency!
```

Gets the currency of these DecimalFormatSymbols. May be null if the currency symbol attribute was previously set to a value that's not a valid ISO 4217 currency code.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Currency.html#!` | the currency used, or null |

### getCurrencySymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrencySymbol(): String!
```

Returns the currency symbol for the currency of these DecimalFormatSymbols in their locale.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the currency symbol |

### getDecimalSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDecimalSeparator(): Char
```

Gets the character used for decimal sign. Different for French, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character used for decimal sign |

### getDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDigit(): Char
```

Gets the character used for a digit in a pattern.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character used for a digit in a pattern |

### getExponentSeparator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExponentSeparator(): String!
```

Returns the string used to separate the mantissa from the exponent. Examples: "x10\^" for 1.23x10\^4, "E" for 1.23E4.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the exponent separator string |

**See Also**

- setExponentSeparator

### getGroupingSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupingSeparator(): Char
```

Gets the character used for grouping separator. Different for French, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the grouping separator |

### getInfinity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInfinity(): String!
```

Gets the string used to represent infinity. Almost always left unchanged.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the string representing infinity |

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(): DecimalFormatSymbols!
```

Gets the `DecimalFormatSymbols` instance for the default locale.

This is equivalent to calling getInstance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols#!` | a `DecimalFormatSymbols` instance. |

**See Also**

- getDefault
- `https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#`

### getInstance

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(locale: Locale!): DecimalFormatSymbols!
```

Gets the `DecimalFormatSymbols` instance for the specified locale. If the specified locale contains the `https://developer.android.com/reference/kotlin/java/util/Locale.html#UNICODE_LOCALE_EXTENSION:kotlin.Char` for the numbering system, the instance is initialized with the specified numbering system if the JRE implementation supports it. For example,

```kotlin
NumberFormat.getNumberInstance(Locale.forLanguageTag("th-TH-u-nu-thai"))
  
```
This may return a `NumberFormat` instance with the Thai numbering system, instead of the Latin numbering system.

<br />

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the desired locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols#!` | a `DecimalFormatSymbols` instance. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `locale` is null |

### getInternationalCurrencySymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInternationalCurrencySymbol(): String!
```

Returns the ISO 4217 currency code of the currency of these DecimalFormatSymbols.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the currency code |

### getMinusSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinusSign(): Char
```

Gets the character used to represent minus sign. If no explicit negative format is specified, one is formed by prefixing minusSign to the positive format.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character representing minus sign |

### getMonetaryDecimalSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMonetaryDecimalSeparator(): Char
```

Returns the monetary decimal separator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the monetary decimal separator |

### getMonetaryGroupingSeparator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMonetaryGroupingSeparator(): Char
```

Gets the character used for grouping separator for currencies. May be different from `grouping separator` in some locales, e.g, German in Austria.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the monetary grouping separator |

### getNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNaN(): String!
```

Gets the string used to represent "not a number". Almost always left unchanged.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the string representing "not a number" |

### getPatternSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPatternSeparator(): Char
```

Gets the character used to separate positive and negative subpatterns in a pattern.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the pattern separator |

### getPerMill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPerMill(): Char
```

Gets the character used for per mille sign. Different for Arabic, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character used for per mille sign |

### getPercent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPercent(): Char
```

Gets the character used for percent sign. Different for Arabic, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character used for percent sign |

### getZeroDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getZeroDigit(): Char
```

Gets the character used for zero. Different for Arabic, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the character used for zero |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Override hashCode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### setCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrency(currency: Currency!): Unit
```

Sets the currency of these DecimalFormatSymbols. This also sets the currency symbol attribute to the currency's symbol in the DecimalFormatSymbols' locale, and the international currency symbol attribute to the currency's ISO 4217 currency code.

| Parameters ||
|---|---|
| `currency` | [Currency](../java.util/Currency.md)!: the new currency to be used |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `currency` is null |

**See Also**

- setCurrencySymbol
- setInternationalCurrencySymbol

### setCurrencySymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrencySymbol(currency: String!): Unit
```

Sets the currency symbol for the currency of these DecimalFormatSymbols in their locale.

| Parameters ||
|---|---|
| `currency` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the currency symbol |

### setDecimalSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecimalSeparator(decimalSeparator: Char): Unit
```

Sets the character used for decimal sign. Different for French, etc.

| Parameters ||
|---|---|
| `decimalSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character used for decimal sign |

### setDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDigit(digit: Char): Unit
```

Sets the character used for a digit in a pattern.

| Parameters ||
|---|---|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character used for a digit in a pattern |

### setExponentSeparator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExponentSeparator(exp: String!): Unit
```

Sets the string used to separate the mantissa from the exponent. Examples: "x10\^" for 1.23x10\^4, "E" for 1.23E4.

| Parameters ||
|---|---|
| `exp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the exponent separator string |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `exp` is null |

**See Also**

- getExponentSeparator

### setGroupingSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGroupingSeparator(groupingSeparator: Char): Unit
```

Sets the character used for grouping separator. Different for French, etc.

| Parameters ||
|---|---|
| `groupingSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the grouping separator |

### setInfinity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInfinity(infinity: String!): Unit
```

Sets the string used to represent infinity. Almost always left unchanged.

| Parameters ||
|---|---|
| `infinity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string representing infinity |

### setInternationalCurrencySymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInternationalCurrencySymbol(currencyCode: String!): Unit
```

Sets the ISO 4217 currency code of the currency of these DecimalFormatSymbols. If the currency code is valid (as defined by getInstance), this also sets the currency attribute to the corresponding Currency instance and the currency symbol attribute to the currency's symbol in the DecimalFormatSymbols' locale. If the currency code is not valid, then the currency attribute is set to null and the currency symbol attribute is not modified.

| Parameters ||
|---|---|
| `currencyCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the currency code |

**See Also**

- setCurrency
- setCurrencySymbol

### setMinusSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinusSign(minusSign: Char): Unit
```

Sets the character used to represent minus sign. If no explicit negative format is specified, one is formed by prefixing minusSign to the positive format.

| Parameters ||
|---|---|
| `minusSign` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character representing minus sign |

### setMonetaryDecimalSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMonetaryDecimalSeparator(sep: Char): Unit
```

Sets the monetary decimal separator.

| Parameters ||
|---|---|
| `sep` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the monetary decimal separator |

### setMonetaryGroupingSeparator

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMonetaryGroupingSeparator(monetaryGroupingSeparator: Char): Unit
```

Sets the character used for grouping separator for currencies. Invocation of this method will not affect the normal `grouping separator`.

| Parameters ||
|---|---|
| `monetaryGroupingSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the monetary grouping separator |

**See Also**

- setGroupingSeparator

### setNaN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNaN(NaN: String!): Unit
```

Sets the string used to represent "not a number". Almost always left unchanged.

| Parameters ||
|---|---|
| `NaN` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string representing "not a number" |

### setPatternSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPatternSeparator(patternSeparator: Char): Unit
```

Sets the character used to separate positive and negative subpatterns in a pattern.

| Parameters ||
|---|---|
| `patternSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the pattern separator |

### setPerMill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPerMill(perMill: Char): Unit
```

Sets the character used for per mille sign. Different for Arabic, etc.

| Parameters ||
|---|---|
| `perMill` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character used for per mille sign |

### setPercent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPercent(percent: Char): Unit
```

Sets the character used for percent sign. Different for Arabic, etc.

| Parameters ||
|---|---|
| `percent` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character used for percent sign |

### setZeroDigit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZeroDigit(zeroDigit: Char): Unit
```

Sets the character used for zero. Different for Arabic, etc.

| Parameters ||
|---|---|
| `zeroDigit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the character used for zero |
