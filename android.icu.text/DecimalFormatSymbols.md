# DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalFormatSymbols

Kotlin| [Java](../android/icu/text/DecimalFormatSymbols.md) 
| --- | --- |

```
open class DecimalFormatSymbols : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md) |

**\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormatSymbols](../java/text/DecimalFormatSymbols.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]** '. This class represents the set of symbols (such as the decimal separator, the grouping separator, and so on) needed by`DecimalFormat`to format numbers.`DecimalFormat`creates for itself an instance of`DecimalFormatSymbols`from its locale data. If you need to change any of these symbols, you can get the`DecimalFormatSymbols`object from your`DecimalFormat`and modify it.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_CURRENCY_MATCH](../android/icu/text/DecimalFormatSymbols.md) **\[icu\]** Indicates the currency match pattern used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_INSERT](../android/icu/text/DecimalFormatSymbols.md) **\[icu\]** Indicates the insertion value used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_SURROUNDING_MATCH](../android/icu/text/DecimalFormatSymbols.md) **\[icu\]** Indicates the surrounding match pattern used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md))`()` Creates a DecimalFormatSymbols object for the default`FORMAT`locale. |
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **\[icu\]**Creates a DecimalFormatSymbols object for the given locale. |
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Creates a DecimalFormatSymbols object for the given locale. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/DecimalFormatSymbols.md))`()` Creates and returns a copy of this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/DecimalFormatSymbols.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| openstatic [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | [forNumberingSystem](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `ns:` ` [NumberingSystem](../android/icu/text/NumberingSystem.md)!`)` **\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](../android/icu/text/NumberingSystem.md). |
| --- | --- |
| openstatic [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | [forNumberingSystem](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`, `ns:` ` [NumberingSystem](../android/icu/text/NumberingSystem.md)!`)` **\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](../android/icu/text/NumberingSystem.md). |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../android/icu/text/DecimalFormatSymbols.md))`()` Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](../android/icu/util/ULocale.md)!\>! | [getAvailableULocales](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]** Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| --- | --- |
| open [Currency](../android/icu/util/Currency.md)! | [getCurrency](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the currency symbol, for [DecimalFormatSymbols.getCurrency()](../android/icu/text/DecimalFormatSymbols.md))API compatibility only. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the string denoting the local currency. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDecimalSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for decimal sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDecimalSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used for decimal sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDigit](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for a digit in a pattern. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDigitStrings](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the array of strings used as digits, in order from 0 through 9 |
| --- | --- |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getDigits](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the array of characters used as digits, in order from 0 through 9 |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExponentMultiplicationSign](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the multiplication sign |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExponentSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used to separate the mantissa from the exponent. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getGroupingSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getGroupingSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used for grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfinity](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the String used to represent infinity. |
| --- | --- |
| openstatic [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | [getInstance](../android/icu/text/DecimalFormatSymbols.md))`()` Returns a DecimalFormatSymbols instance for the default locale. |
| openstatic [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | [getInstance](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Returns a DecimalFormatSymbols instance for the given locale. |
| openstatic [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | [getInstance](../android/icu/text/DecimalFormatSymbols.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Returns a DecimalFormatSymbols instance for the given locale. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInternationalCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the international string denoting the local currency. |
| open [Locale](../java/util/Locale.md)! | [getLocale](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the locale for which this object was constructed. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMinusSign](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used to represent minus sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMinusSignString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used to represent minus sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMonetaryDecimalSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the monetary decimal separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMonetaryDecimalSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the monetary decimal separator string. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMonetaryGroupingSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the monetary grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMonetaryGroupingSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the monetary grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNaN](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the String used to represent NaN. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPadEscape](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the character used to pad numbers out to a specified width. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md))`(`itemType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `beforeCurrency:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**Returns the desired currency spacing value. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPatternSeparator](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used to separate positive and negative subpatterns in a pattern. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPerMill](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for mille percent sign. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPerMillString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used for permille sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPercent](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for percent sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPercentString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used for percent sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPlusSign](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the localized plus sign. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPlusSignString](../android/icu/text/DecimalFormatSymbols.md))`()` **\[icu\]**Returns the string used to represent plus sign. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getSignificantDigit](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used to represent a significant digit in a pattern. |
| open [ULocale](../android/icu/util/ULocale.md)! | [getULocale](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the locale for which this object was constructed. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getZeroDigit](../android/icu/text/DecimalFormatSymbols.md))`()` Returns the character used for zero. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/text/DecimalFormatSymbols.md))`()` Returns a hash code value for the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](../android/icu/text/DecimalFormatSymbols.md))`(`currency:` ` [Currency](../android/icu/util/Currency.md)!`)` Sets the currency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md))`(`currency:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the string denoting the local currency. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`decimalSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for decimal sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`(`decimalSeparatorString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for decimal sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDigit](../android/icu/text/DecimalFormatSymbols.md))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for a digit in a pattern. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDigitStrings](../android/icu/text/DecimalFormatSymbols.md))`(`digitStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` **\[icu\]**Sets the array of strings used as digits, in order from 0 through 9 |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExponentMultiplicationSign](../android/icu/text/DecimalFormatSymbols.md))`(`exponentMultiplicationSign:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the multiplication sign |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExponentSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`exp:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used to separate the mantissa from the exponent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`groupingSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for grouping separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`(`groupingSeparatorString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for grouping separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfinity](../android/icu/text/DecimalFormatSymbols.md))`(`infinity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the String used to represent infinity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInternationalCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md))`(`currency:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the international string denoting the local currency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinusSign](../android/icu/text/DecimalFormatSymbols.md))`(`minusSign:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to represent minus sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinusSignString](../android/icu/text/DecimalFormatSymbols.md))`(`minusSignString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used to represent minus sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryDecimalSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`sep:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the monetary decimal separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryDecimalSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`(`sep:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the monetary decimal separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryGroupingSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`sep:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the monetary grouping separator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryGroupingSeparatorString](../android/icu/text/DecimalFormatSymbols.md))`(`sep:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the monetary grouping separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNaN](../android/icu/text/DecimalFormatSymbols.md))`(`NaN:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the String used to represent NaN. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadEscape](../android/icu/text/DecimalFormatSymbols.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the character used to pad numbers out to a specified width. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md))`(`itemType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `beforeCurrency:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the indicated currency spacing pattern or value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternSeparator](../android/icu/text/DecimalFormatSymbols.md))`(`patternSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to separate positive and negative subpatterns in a pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerMill](../android/icu/text/DecimalFormatSymbols.md))`(`perMill:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for mille percent sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerMillString](../android/icu/text/DecimalFormatSymbols.md))`(`perMillString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for permille sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPercent](../android/icu/text/DecimalFormatSymbols.md))`(`percent:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for percent sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPercentString](../android/icu/text/DecimalFormatSymbols.md))`(`percentString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for percent sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlusSign](../android/icu/text/DecimalFormatSymbols.md))`(`plus:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the localized plus sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlusSignString](../android/icu/text/DecimalFormatSymbols.md))`(`plusSignString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the localized plus sign string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSignificantDigit](../android/icu/text/DecimalFormatSymbols.md))`(`sigDigit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to represent a significant digit in a pattern. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZeroDigit](../android/icu/text/DecimalFormatSymbols.md))`(`zeroDigit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for zero. |

## Constants

### CURRENCY_SPC_CURRENCY_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_CURRENCY_MATCH: Int
```

**\[icu\]** Indicates the currency match pattern used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). 

 Value: 0

### CURRENCY_SPC_INSERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_INSERT: Int
```

**\[icu\]** Indicates the insertion value used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). 

 Value: 2

### CURRENCY_SPC_SURROUNDING_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_SURROUNDING_MATCH: Int
```

**\[icu\]** Indicates the surrounding match pattern used in [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md)). 

 Value: 1

## Public constructors

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols()
```

Creates a DecimalFormatSymbols object for the default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols(locale: ULocale!)
```

**\[icu\]**Creates a DecimalFormatSymbols object for the given locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale |

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols(locale: Locale!)
```

Creates a DecimalFormatSymbols object for the given locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object`x`, the expression: 

```kotlin
x.clone() != x
```
will be true, and that the expression: 

```kotlin
x.clone().getClass() == x.getClass()
```
will be`true`, but these are not absolute requirements. While it is typically the case that: 

```kotlin
x.clone().equals(x)
```
will be`true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling`super.clone`. If a class and all of its superclasses (except`Object`) obey this convention, it will be the case that`x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by`super.clone`before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by`super.clone`need to be modified.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

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

### forNumberingSystem

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forNumberingSystem(
    locale: ULocale!, 
    ns: NumberingSystem!
): DecimalFormatSymbols!
```

**\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](../android/icu/text/NumberingSystem.md).

This method behaves equivalently to #getInstance called with a locale having a "numbers=xxxx" keyword specifying the numbering system by name.

In this method, the NumberingSystem argument will be used even if the locale has its own "numbers=xxxx" keyword.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale. |
| `ns` | [NumberingSystem](../android/icu/text/NumberingSystem.md)!:the numbering system. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | A DecimalFormatSymbols instance. |

### forNumberingSystem

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forNumberingSystem(
    locale: Locale!, 
    ns: NumberingSystem!
): DecimalFormatSymbols!
```

**\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](../android/icu/text/NumberingSystem.md).

This method behaves equivalently to #getInstance called with a locale having a "numbers=xxxx" keyword specifying the numbering system by name.

In this method, the NumberingSystem argument will be used even if the locale has its own "numbers=xxxx" keyword.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale. |
| `ns` | [NumberingSystem](../android/icu/text/NumberingSystem.md)!:the numbering system. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | A DecimalFormatSymbols instance. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.

**Note:** Unlike`java.text.DecimalFormatSymbols#getAvailableLocales`, this method simply returns the array of`Locale`s available for this class. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | An array of`Locale`s for which localized`DecimalFormatSymbols`instances are available. |

### getAvailableULocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableULocales(): Array<ULocale!>!
```

**\[icu\]** Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.

**Note:** Unlike`java.text.DecimalFormatSymbols#getAvailableLocales`, this method simply returns the array of`ULocale`s available in this class. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](../android/icu/util/ULocale.md)!>! | An array of`ULocale`s for which localized`DecimalFormatSymbols`instances are available. |

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the currency symbol, for [DecimalFormatSymbols.getCurrency()](../android/icu/text/DecimalFormatSymbols.md))API compatibility only. ICU clients should use the Currency API directly.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [Currency](../android/icu/util/Currency.md)! | the currency used, or null |

### getCurrencySymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrencySymbol(): String!
```

Returns the string denoting the local currency.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the local currency String. |

### getDecimalSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecimalSeparator(): Char
```

Returns the character used for decimal sign. Different for French, etc.

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the decimal character |

### getDecimalSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecimalSeparatorString(): String!
```

**\[icu\]**Returns the string used for decimal sign.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the decimal sign string |

**See Also**

- [#setDecimalSeparatorString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigit(): Char
```

Returns the character used for a digit in a pattern.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the digit pattern character |

### getDigitStrings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigitStrings(): Array<String!>!
```

**\[icu\]**Returns the array of strings used as digits, in order from 0 through 9

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The array of ten digit strings |

**See Also**

- [#setDigitStrings(String[])](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDigitStrings(kotlin.Array)) 

### getDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDigits(): CharArray!
```

Returns the array of characters used as digits, in order from 0 through 9

| Return ||
|------------------------------------------------------------------------------------------|-----------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | The array |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigitStrings()> 

### getExponentMultiplicationSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExponentMultiplicationSign(): String!
```

Returns the multiplication sign 

### getExponentSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExponentSeparator(): String!
```

**\[icu\]**Returns the string used to separate the mantissa from the exponent. Examples: "x10\^" for 1.23x10\^4, "E" for 1.23E4.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized exponent symbol, used in localized patterns and formatted strings |

**See Also**

- [#setExponentSeparator](../android/icu/text/DecimalFormatSymbols.md)) 

### getGroupingSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupingSeparator(): Char
```

Returns the character used for grouping separator. Different for French, etc.

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the thousands character |

### getGroupingSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupingSeparatorString(): String!
```

**\[icu\]**Returns the string used for grouping separator. Different for French, etc.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the grouping separator string |

**See Also**

- [#setGroupingSeparatorString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getInfinity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInfinity(): String!
```

Returns the String used to represent infinity. Almost always left unchanged.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the Infinity string |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): DecimalFormatSymbols!
```

Returns a DecimalFormatSymbols instance for the default locale.

**Note:** Unlike`java.text.DecimalFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DecimalFormatSymbols()`. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | A DecimalFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): DecimalFormatSymbols!
```

Returns a DecimalFormatSymbols instance for the given locale.

**Note:** Unlike`java.text.DecimalFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DecimalFormatSymbols(locale)`. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | A DecimalFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): DecimalFormatSymbols!
```

Returns a DecimalFormatSymbols instance for the given locale.

**Note:** Unlike`java.text.DecimalFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DecimalFormatSymbols(locale)`. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | A DecimalFormatSymbols instance. |

### getInternationalCurrencySymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInternationalCurrencySymbol(): String!
```

Returns the international string denoting the local currency.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the international string denoting the local currency |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): Locale!
```

Returns the locale for which this object was constructed.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------|
| [Locale](../java/util/Locale.md)! | the locale for which this object was constructed |

### getMinusSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinusSign(): Char
```

Returns the character used to represent minus sign. If no explicit negative format is specified, one is formed by prefixing minusSign to the positive format.

| Return ||
|------------------------------------------------------------------------------|--------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the minus sign character |

### getMinusSignString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinusSignString(): String!
```

**\[icu\]**Returns the string used to represent minus sign.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the minus sign string |

**See Also**

- [#setMinusSignString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getMonetaryDecimalSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonetaryDecimalSeparator(): Char
```

Returns the monetary decimal separator.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the monetary decimal separator character |

### getMonetaryDecimalSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonetaryDecimalSeparatorString(): String!
```

**\[icu\]**Returns the monetary decimal separator string.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the monetary decimal separator string |

**See Also**

- [#setMonetaryDecimalSeparatorString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getMonetaryGroupingSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonetaryGroupingSeparator(): Char
```

**\[icu\]**Returns the monetary grouping separator.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the monetary grouping separator character |

### getMonetaryGroupingSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMonetaryGroupingSeparatorString(): String!
```

**\[icu\]**Returns the monetary grouping separator.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the monetary grouping separator string |

**See Also**

- [#setMonetaryGroupingSeparatorString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getNaN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNaN(): String!
```

Returns the String used to represent NaN. Almost always left unchanged.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the NaN String |

### getPadEscape

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadEscape(): Char
```

**\[icu\]** Returns the character used to pad numbers out to a specified width. This is not the pad character itself; rather, it is the special pattern character*preceding*the pad character. In the pattern "\*_#,##0", '\*' is the pad escape, and '_' is the pad character.

| Return ||
|------------------------------------------------------------------------------|---------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character |

**See Also**

- [#setPadEscape](../android/icu/text/DecimalFormatSymbols.md))
- [android.icu.text.DecimalFormat#getFormatWidth](../android/icu/text/DecimalFormat.md))
- [android.icu.text.DecimalFormat#getPadPosition](../android/icu/text/DecimalFormat.md))
- [android.icu.text.DecimalFormat#getPadCharacter](../android/icu/text/DecimalFormat.md)) 

### getPatternForCurrencySpacing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPatternForCurrencySpacing(
    itemType: Int, 
    beforeCurrency: Boolean
): String!
```

**\[icu\]**Returns the desired currency spacing value. Original values come from ICU's CLDR data based on the locale provided during construction, and can be null. These values govern what and when text is inserted between a currency code/name/symbol and the currency amount when formatting money.

For more information, see [UTS#35 section 5.10.2](http://www.unicode.org/reports/tr35/#Currencies).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `itemType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of CURRENCY_SPC_CURRENCY_MATCH, CURRENCY_SPC_SURROUNDING_MATCH or CURRENCY_SPC_INSERT |
| `beforeCurrency` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to get the`beforeCurrency`values, false to get the`afterCurrency`values. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value, or null. |

**See Also**

- [#setPatternForCurrencySpacing(int, boolean, String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getPatternSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPatternSeparator(): Char
```

Returns the character used to separate positive and negative subpatterns in a pattern.

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the pattern separator character |

### getPerMill

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPerMill(): Char
```

Returns the character used for mille percent sign. Different for Arabic, etc.

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the mille percent character |

### getPerMillString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPerMillString(): String!
```

**\[icu\]**Returns the string used for permille sign.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the permille string |

**See Also**

- [#setPerMillString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getPercent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPercent(): Char
```

Returns the character used for percent sign. Different for Arabic, etc.

| Return ||
|------------------------------------------------------------------------------|-----------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the percent character |

### getPercentString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPercentString(): String!
```

**\[icu\]**Returns the string used for percent sign.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the percent string |

**See Also**

- [#setPercentString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### getPlusSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPlusSign(): Char
```

**\[icu\]**Returns the localized plus sign.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the plus sign, used in localized patterns and formatted strings |

**See Also**

- [#setPlusSign](../android/icu/text/DecimalFormatSymbols.md))
- [#setMinusSign](../android/icu/text/DecimalFormatSymbols.md))
- [#getMinusSign](../android/icu/text/DecimalFormatSymbols.md)) 

### getPlusSignString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPlusSignString(): String!
```

**\[icu\]**Returns the string used to represent plus sign.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the plus sign string |

### getSignificantDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSignificantDigit(): Char
```

Returns the character used to represent a significant digit in a pattern.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the significant digit pattern character |

### getULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getULocale(): ULocale!
```

Returns the locale for which this object was constructed.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ULocale](../android/icu/util/ULocale.md)! | the locale for which this object was constructed |

### getZeroDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getZeroDigit(): Char
```

Returns the character used for zero. Different for Arabic, etc.

| Return ||
|------------------------------------------------------------------------------|---------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character |

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

### setCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrency(currency: Currency!): Unit
```

Sets the currency.

**Note:**ICU does not use the DecimalFormatSymbols for the currency any more. This API is present for API compatibility only.

This also sets the currency symbol attribute to the currency's symbol in the DecimalFormatSymbols' locale, and the international currency symbol attribute to the currency's ISO 4217 currency code.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------|
| `currency` | [Currency](../android/icu/util/Currency.md)!:the new currency to be used |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`currency`is null |

**See Also**

- [#setCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md))
- [#setInternationalCurrencySymbol](../android/icu/text/DecimalFormatSymbols.md)) 

### setCurrencySymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrencySymbol(currency: String!): Unit
```

Sets the string denoting the local currency.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `currency` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the local currency String. |

### setDecimalSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecimalSeparator(decimalSeparator: Char): Unit
```

Sets the character used for decimal sign. Different for French, etc.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------|
| `decimalSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the decimal character |

### setDecimalSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecimalSeparatorString(decimalSeparatorString: String!): Unit
```

**\[icu\]**Sets the string used for decimal sign.

**Note:** When the input decimal separator String is represented by multiple Java chars, then [getDecimalSeparator()](../android/icu/text/DecimalFormatSymbols.md))will return the default decimal separator character ('.').

| Parameters ||
|--------------------------|-----------------------------------------------------------------------------------------------------------|
| `decimalSeparatorString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the decimal sign string |

| Exceptions ||
|----------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if`decimalSeparatorString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDecimalSeparatorString()> 

### setDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDigit(digit: Char): Unit
```

Sets the character used for a digit in a pattern.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `digit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the digit pattern character |

### setDigitStrings

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDigitStrings(digitStrings: Array<String!>!): Unit
```

**\[icu\]**Sets the array of strings used as digits, in order from 0 through 9

**Note:**

When the input array of digit strings contains any strings represented by multiple Java chars, then [getDigits()](../android/icu/text/DecimalFormatSymbols.md))will return the default digits ('0' - '9') and [getZeroDigit()](../android/icu/text/DecimalFormatSymbols.md))will return the default zero digit ('0').

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `digitStrings` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The array of digit strings. The length of the array must be exactly 10. |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the`digitStrings`is null. |
| `java.lang.IllegalArgumentException` | if the length of the array is not 10. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigitStrings()> 

### setExponentMultiplicationSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExponentMultiplicationSign(exponentMultiplicationSign: String!): Unit
```

Sets the multiplication sign 

### setExponentSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setExponentSeparator(exp: String!): Unit
```

**\[icu\]**Sets the string used to separate the mantissa from the exponent. Examples: "x10\^" for 1.23x10\^4, "E" for 1.23E4.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exp` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the localized exponent symbol, used in localized patterns and formatted strings |

**See Also**

- [#getExponentSeparator](../android/icu/text/DecimalFormatSymbols.md)) 

### setGroupingSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingSeparator(groupingSeparator: Char): Unit
```

Sets the character used for grouping separator. Different for French, etc.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------|
| `groupingSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the thousands character |

**See Also**

- [#setGroupingSeparatorString(String)](../android/icu/text/DecimalFormatSymbols.md)) 

### setGroupingSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingSeparatorString(groupingSeparatorString: String!): Unit
```

**\[icu\]**Sets the string used for grouping separator.

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getGroupingSeparator()](../android/icu/text/DecimalFormatSymbols.md))will return the default grouping separator character (',').

| Parameters ||
|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| `groupingSeparatorString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the grouping separator string |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if`groupingSeparatorString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getGroupingSeparatorString()> 

### setInfinity

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInfinity(infinity: String!): Unit
```

Sets the String used to represent infinity. Almost always left unchanged.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------|
| `infinity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Infinity String |

### setInternationalCurrencySymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInternationalCurrencySymbol(currency: String!): Unit
```

Sets the international string denoting the local currency.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `currency` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the international string denoting the local currency. |

### setMinusSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinusSign(minusSign: Char): Unit
```

Sets the character used to represent minus sign. If no explicit negative format is specified, one is formed by prefixing minusSign to the positive format.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------|
| `minusSign` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the minus sign character |

### setMinusSignString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinusSignString(minusSignString: String!): Unit
```

**\[icu\]**Sets the string used to represent minus sign.

**Note:** When the input minus sign String is represented by multiple Java chars, then [getMinusSign()](../android/icu/text/DecimalFormatSymbols.md))will return the default minus sign character ('-').

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------|
| `minusSignString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the minus sign string |

| Exceptions ||
|----------------------------------|-----------------------------|
| `java.lang.NullPointerException` | if`minusSignString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getGroupingSeparatorString()> 

### setMonetaryDecimalSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonetaryDecimalSeparator(sep: Char): Unit
```

Sets the monetary decimal separator.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `sep` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the monetary decimal separator character |

### setMonetaryDecimalSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonetaryDecimalSeparatorString(sep: String!): Unit
```

**\[icu\]**Sets the monetary decimal separator string.

**Note:** When the input monetary decimal separator String is represented by multiple Java chars, then [getMonetaryDecimalSeparatorString()](../android/icu/text/DecimalFormatSymbols.md))will return the default monetary decimal separator character ('.').

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------|
| `sep` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the monetary decimal separator string |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`sep`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryDecimalSeparatorString()> 

### setMonetaryGroupingSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonetaryGroupingSeparator(sep: Char): Unit
```

**\[icu\]**Sets the monetary grouping separator.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `sep` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the monetary grouping separator character |

### setMonetaryGroupingSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMonetaryGroupingSeparatorString(sep: String!): Unit
```

**\[icu\]**Sets the monetary grouping separator string.

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getMonetaryGroupingSeparator()](../android/icu/text/DecimalFormatSymbols.md))will return the default monetary grouping separator character (',').

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `sep` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the monetary grouping separator string |

| Exceptions ||
|----------------------------------|-----------------|
| `java.lang.NullPointerException` | if`sep`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryGroupingSeparatorString()> 

### setNaN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNaN(NaN: String!): Unit
```

Sets the String used to represent NaN. Almost always left unchanged.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `NaN` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the NaN String |

### setPadEscape

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPadEscape(c: Char): Unit
```

**\[icu\]** Sets the character used to pad numbers out to a specified width. This is not the pad character itself; rather, it is the special pattern character*preceding*the pad character. In the pattern "\*_#,##0", '\*' is the pad escape, and '_' is the pad character. 
**See Also**

- [#getPadEscape](../android/icu/text/DecimalFormatSymbols.md))
- [android.icu.text.DecimalFormat#setFormatWidth](../android/icu/text/DecimalFormat.md))
- [android.icu.text.DecimalFormat#setPadPosition](../android/icu/text/DecimalFormat.md))
- [android.icu.text.DecimalFormat#setPadCharacter](../android/icu/text/DecimalFormat.md)) 

### setPatternForCurrencySpacing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPatternForCurrencySpacing(
    itemType: Int, 
    beforeCurrency: Boolean, 
    pattern: String!
): Unit
```

**\[icu\]** Sets the indicated currency spacing pattern or value. See [getPatternForCurrencySpacing](../android/icu/text/DecimalFormatSymbols.md))for more information.

Values for currency match and surrounding match must be patterns. Values for insert can be any string.

**Note:**ICU4J does not currently use this information.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `itemType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of CURRENCY_SPC_CURRENCY_MATCH, CURRENCY_SPC_SURROUNDING_MATCH or CURRENCY_SPC_INSERT |
| `beforeCurrency` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the pattern is for before the currency symbol. false if the pattern is for after it. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to override current setting; can be null. |
| --- | --- |

**See Also**

- [#getPatternForCurrencySpacing(int, boolean)](../android/icu/text/DecimalFormatSymbols.md)) 

### setPatternSeparator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPatternSeparator(patternSeparator: Char): Unit
```

Sets the character used to separate positive and negative subpatterns in a pattern.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------|
| `patternSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the pattern separator character |

### setPerMill

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPerMill(perMill: Char): Unit
```

Sets the character used for mille percent sign. Different for Arabic, etc.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `perMill` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the mille percent character |

### setPerMillString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPerMillString(perMillString: String!): Unit
```

**\[icu\]**Sets the string used for permille sign.

**Note:** When the input permille String is represented by multiple Java chars, then [getPerMill()](../android/icu/text/DecimalFormatSymbols.md))will return the default permille character ('‰').

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `perMillString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the permille string |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`perMillString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPerMillString()> 

### setPercent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPercent(percent: Char): Unit
```

Sets the character used for percent sign. Different for Arabic, etc.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------|
| `percent` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the percent character |

### setPercentString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPercentString(percentString: String!): Unit
```

**\[icu\]**Sets the string used for percent sign.

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getPercent()](../android/icu/text/DecimalFormatSymbols.md))will return the default percent sign character ('%').

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------|
| `percentString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the percent string |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`percentString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPercentString()> 

### setPlusSign

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlusSign(plus: Char): Unit
```

**\[icu\]**Sets the localized plus sign.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `plus` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the plus sign, used in localized patterns and formatted strings |

**See Also**

- [#getPlusSign](../android/icu/text/DecimalFormatSymbols.md))
- [#setMinusSign](../android/icu/text/DecimalFormatSymbols.md))
- [#getMinusSign](../android/icu/text/DecimalFormatSymbols.md)) 

### setPlusSignString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlusSignString(plusSignString: String!): Unit
```

**\[icu\]**Sets the localized plus sign string.

**Note:** When the input plus sign String is represented by multiple Java chars, then [getPlusSign()](../android/icu/text/DecimalFormatSymbols.md))will return the default plus sign character ('+').

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `plusSignString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the plus sign string, used in localized patterns and formatted strings |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if`plusSignString`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPlusSignString()> 

### setSignificantDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSignificantDigit(sigDigit: Char): Unit
```

Sets the character used to represent a significant digit in a pattern.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `sigDigit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the significant digit pattern character |

### setZeroDigit

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setZeroDigit(zeroDigit: Char): Unit
```

Sets the character used for zero.

**Note:**This method propagates digit 1 to digit 9 by incrementing code point one by one.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------|
| `zeroDigit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the zero character. |
