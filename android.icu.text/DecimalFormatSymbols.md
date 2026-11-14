# DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalFormatSymbols

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/DecimalFormatSymbols "View this page in Java") 
| --- | --- |

```
open class DecimalFormatSymbols : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#) |

**\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols.html#). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]** '. This class represents the set of symbols (such as the decimal separator, the grouping separator, and so on) needed by`DecimalFormat`to format numbers.`DecimalFormat`creates for itself an instance of`DecimalFormatSymbols`from its locale data. If you need to change any of these symbols, you can get the`DecimalFormatSymbols`object from your`DecimalFormat`and modify it.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_CURRENCY_MATCH](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#CURRENCY_SPC_CURRENCY_MATCH:kotlin.Int) **\[icu\]** Indicates the currency match pattern used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_INSERT](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#CURRENCY_SPC_INSERT:kotlin.Int) **\[icu\]** Indicates the insertion value used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCY_SPC_SURROUNDING_MATCH](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#CURRENCY_SPC_SURROUNDING_MATCH:kotlin.Int) **\[icu\]** Indicates the surrounding match pattern used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#DecimalFormatSymbols())`()` Creates a DecimalFormatSymbols object for the default`FORMAT`locale. |
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#DecimalFormatSymbols(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **\[icu\]**Creates a DecimalFormatSymbols object for the given locale. |
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#DecimalFormatSymbols(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Creates a DecimalFormatSymbols object for the given locale. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#clone())`()` Creates and returns a copy of this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| openstatic [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | [forNumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#forNumberingSystem(android.icu.util.ULocale,%20android.icu.text.NumberingSystem))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `ns:` ` [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem)!`)` **\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem). |
| --- | --- |
| openstatic [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | [forNumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#forNumberingSystem(java.util.Locale,%20android.icu.text.NumberingSystem))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `ns:` ` [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem)!`)` **\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem). |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getAvailableLocales())`()` Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!\>! | [getAvailableULocales](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getAvailableULocales())`()` **\[icu\]** Returns an array of all locales for which the`getInstance`methods of this class can return localized instances. |
| --- | --- |
| open [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)! | [getCurrency](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getCurrency())`()` Returns the currency symbol, for [DecimalFormatSymbols.getCurrency()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getCurrency())API compatibility only. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getCurrencySymbol())`()` Returns the string denoting the local currency. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDecimalSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDecimalSeparator())`()` Returns the character used for decimal sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDecimalSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDecimalSeparatorString())`()` **\[icu\]**Returns the string used for decimal sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigit())`()` Returns the character used for a digit in a pattern. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getDigitStrings](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigitStrings())`()` **\[icu\]**Returns the array of strings used as digits, in order from 0 through 9 |
| --- | --- |
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [getDigits](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigits())`()` Returns the array of characters used as digits, in order from 0 through 9 |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExponentMultiplicationSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getExponentMultiplicationSign())`()` Returns the multiplication sign |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExponentSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getExponentSeparator())`()` **\[icu\]**Returns the string used to separate the mantissa from the exponent. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getGroupingSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getGroupingSeparator())`()` Returns the character used for grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getGroupingSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getGroupingSeparatorString())`()` **\[icu\]**Returns the string used for grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfinity](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getInfinity())`()` Returns the String used to represent infinity. |
| --- | --- |
| openstatic [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getInstance())`()` Returns a DecimalFormatSymbols instance for the default locale. |
| openstatic [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Returns a DecimalFormatSymbols instance for the given locale. |
| openstatic [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a DecimalFormatSymbols instance for the given locale. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInternationalCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getInternationalCurrencySymbol())`()` Returns the international string denoting the local currency. |
| open [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | [getLocale](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getLocale())`()` Returns the locale for which this object was constructed. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMinusSign())`()` Returns the character used to represent minus sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMinusSignString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMinusSignString())`()` **\[icu\]**Returns the string used to represent minus sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMonetaryDecimalSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryDecimalSeparator())`()` Returns the monetary decimal separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMonetaryDecimalSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryDecimalSeparatorString())`()` **\[icu\]**Returns the monetary decimal separator string. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMonetaryGroupingSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryGroupingSeparator())`()` **\[icu\]**Returns the monetary grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMonetaryGroupingSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryGroupingSeparatorString())`()` **\[icu\]**Returns the monetary grouping separator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNaN](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getNaN())`()` Returns the String used to represent NaN. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPadEscape](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPadEscape())`()` **\[icu\]**Returns the character used to pad numbers out to a specified width. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean))`(`itemType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `beforeCurrency:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**Returns the desired currency spacing value. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPatternSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternSeparator())`()` Returns the character used to separate positive and negative subpatterns in a pattern. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPerMill](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPerMill())`()` Returns the character used for mille percent sign. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPerMillString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPerMillString())`()` **\[icu\]**Returns the string used for permille sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPercent](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPercent())`()` Returns the character used for percent sign. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPercentString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPercentString())`()` **\[icu\]**Returns the string used for percent sign. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPlusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPlusSign())`()` **\[icu\]**Returns the localized plus sign. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPlusSignString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPlusSignString())`()` **\[icu\]**Returns the string used to represent plus sign. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getSignificantDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getSignificantDigit())`()` Returns the character used to represent a significant digit in a pattern. |
| open [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)! | [getULocale](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getULocale())`()` Returns the locale for which this object was constructed. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getZeroDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getZeroDigit())`()` Returns the character used for zero. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#hashCode())`()` Returns a hash code value for the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setCurrency(android.icu.util.Currency))`(`currency:` ` [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)!`)` Sets the currency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setCurrencySymbol(kotlin.String))`(`currency:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the string denoting the local currency. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDecimalSeparator(kotlin.Char))`(`decimalSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for decimal sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDecimalSeparatorString(kotlin.String))`(`decimalSeparatorString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for decimal sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDigit(kotlin.Char))`(`digit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for a digit in a pattern. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDigitStrings](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDigitStrings(kotlin.Array))`(`digitStrings:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` **\[icu\]**Sets the array of strings used as digits, in order from 0 through 9 |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExponentMultiplicationSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setExponentMultiplicationSign(kotlin.String))`(`exponentMultiplicationSign:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the multiplication sign |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExponentSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setExponentSeparator(kotlin.String))`(`exp:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used to separate the mantissa from the exponent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setGroupingSeparator(kotlin.Char))`(`groupingSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for grouping separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setGroupingSeparatorString(kotlin.String))`(`groupingSeparatorString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for grouping separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfinity](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setInfinity(kotlin.String))`(`infinity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the String used to represent infinity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInternationalCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setInternationalCurrencySymbol(kotlin.String))`(`currency:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the international string denoting the local currency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMinusSign(kotlin.Char))`(`minusSign:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to represent minus sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinusSignString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMinusSignString(kotlin.String))`(`minusSignString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used to represent minus sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryDecimalSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryDecimalSeparator(kotlin.Char))`(`sep:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the monetary decimal separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryDecimalSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryDecimalSeparatorString(kotlin.String))`(`sep:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the monetary decimal separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryGroupingSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryGroupingSeparator(kotlin.Char))`(`sep:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the monetary grouping separator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMonetaryGroupingSeparatorString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryGroupingSeparatorString(kotlin.String))`(`sep:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the monetary grouping separator string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNaN](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setNaN(kotlin.String))`(`NaN:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the String used to represent NaN. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPadEscape](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPadEscape(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the character used to pad numbers out to a specified width. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean,%20kotlin.String))`(`itemType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `beforeCurrency:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the indicated currency spacing pattern or value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPatternSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPatternSeparator(kotlin.Char))`(`patternSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to separate positive and negative subpatterns in a pattern. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerMill](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPerMill(kotlin.Char))`(`perMill:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for mille percent sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPerMillString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPerMillString(kotlin.String))`(`perMillString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for permille sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPercent](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPercent(kotlin.Char))`(`percent:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for percent sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPercentString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPercentString(kotlin.String))`(`percentString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the string used for percent sign. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPlusSign(kotlin.Char))`(`plus:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` **\[icu\]**Sets the localized plus sign. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlusSignString](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPlusSignString(kotlin.String))`(`plusSignString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Sets the localized plus sign string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSignificantDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setSignificantDigit(kotlin.Char))`(`sigDigit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used to represent a significant digit in a pattern. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setZeroDigit](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setZeroDigit(kotlin.Char))`(`zeroDigit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the character used for zero. |

## Constants

### CURRENCY_SPC_CURRENCY_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_CURRENCY_MATCH: Int
```

**\[icu\]** Indicates the currency match pattern used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). 

 Value: 0

### CURRENCY_SPC_INSERT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_INSERT: Int
```

**\[icu\]** Indicates the insertion value used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). 

 Value: 2

### CURRENCY_SPC_SURROUNDING_MATCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCY_SPC_SURROUNDING_MATCH: Int
```

**\[icu\]** Indicates the surrounding match pattern used in [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)). 

 Value: 1

## Public constructors

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols()
```

Creates a DecimalFormatSymbols object for the default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols(locale: ULocale!)
```

**\[icu\]**Creates a DecimalFormatSymbols object for the given locale.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale |

### DecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormatSymbols(locale: Locale!)
```

Creates a DecimalFormatSymbols object for the given locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale |

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

**\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem).

This method behaves equivalently to #getInstance called with a locale having a "numbers=xxxx" keyword specifying the numbering system by name.

In this method, the NumberingSystem argument will be used even if the locale has its own "numbers=xxxx" keyword.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale. |
| `ns` | [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem)!:the numbering system. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | A DecimalFormatSymbols instance. |

### forNumberingSystem

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun forNumberingSystem(
    locale: Locale!, 
    ns: NumberingSystem!
): DecimalFormatSymbols!
```

**\[icu\]** Returns a DecimalFormatSymbols instance for the given locale with digits and symbols corresponding to the given [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem).

This method behaves equivalently to #getInstance called with a locale having a "numbers=xxxx" keyword specifying the numbering system by name.

In this method, the NumberingSystem argument will be used even if the locale has its own "numbers=xxxx" keyword.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale. |
| `ns` | [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem)!:the numbering system. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | A DecimalFormatSymbols instance. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.

**Note:** Unlike`java.text.DecimalFormatSymbols#getAvailableLocales`, this method simply returns the array of`Locale`s available for this class. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | An array of`Locale`s for which localized`DecimalFormatSymbols`instances are available. |

### getAvailableULocales

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableULocales(): Array<ULocale!>!
```

**\[icu\]** Returns an array of all locales for which the`getInstance`methods of this class can return localized instances.

**Note:** Unlike`java.text.DecimalFormatSymbols#getAvailableLocales`, this method simply returns the array of`ULocale`s available in this class. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!>! | An array of`ULocale`s for which localized`DecimalFormatSymbols`instances are available. |

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the currency symbol, for [DecimalFormatSymbols.getCurrency()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getCurrency())API compatibility only. ICU clients should use the Currency API directly.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)! | the currency used, or null |

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

- [#setDecimalSeparatorString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setDecimalSeparatorString(kotlin.String)) 

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

- [#setExponentSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setExponentSeparator(kotlin.String)) 

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

- [#setGroupingSeparatorString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setGroupingSeparatorString(kotlin.String)) 

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
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | A DecimalFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): DecimalFormatSymbols!
```

Returns a DecimalFormatSymbols instance for the given locale.

**Note:** Unlike`java.text.DecimalFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DecimalFormatSymbols(locale)`. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | A DecimalFormatSymbols instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): DecimalFormatSymbols!
```

Returns a DecimalFormatSymbols instance for the given locale.

**Note:** Unlike`java.text.DecimalFormatSymbols#getInstance`, this method simply returns`new android.icu.text.DecimalFormatSymbols(locale)`. ICU currently does not support`DecimalFormatSymbolsProvider`, which was introduced in Java 6.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------|
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#)! | A DecimalFormatSymbols instance. |

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
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | the locale for which this object was constructed |

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

- [#setMinusSignString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMinusSignString(kotlin.String)) 

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

- [#setMonetaryDecimalSeparatorString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryDecimalSeparatorString(kotlin.String)) 

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

- [#setMonetaryGroupingSeparatorString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMonetaryGroupingSeparatorString(kotlin.String)) 

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

- [#setPadEscape](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPadEscape(kotlin.Char))
- [android.icu.text.DecimalFormat#getFormatWidth](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getFormatWidth())
- [android.icu.text.DecimalFormat#getPadPosition](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition())
- [android.icu.text.DecimalFormat#getPadCharacter](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadCharacter()) 

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

- [#setPatternForCurrencySpacing(int, boolean, String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean,%20kotlin.String)) 

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

- [#setPerMillString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPerMillString(kotlin.String)) 

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

- [#setPercentString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPercentString(kotlin.String)) 

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

- [#setPlusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setPlusSign(kotlin.Char))
- [#setMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMinusSign(kotlin.Char))
- [#getMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMinusSign()) 

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
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)! | the locale for which this object was constructed |

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

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#).

The general contract of`hashCode`is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result.
- It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

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
| `currency` | [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)!:the new currency to be used |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if`currency`is null |

**See Also**

- [#setCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setCurrencySymbol(kotlin.String))
- [#setInternationalCurrencySymbol](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setInternationalCurrencySymbol(kotlin.String)) 

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

**Note:** When the input decimal separator String is represented by multiple Java chars, then [getDecimalSeparator()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDecimalSeparator())will return the default decimal separator character ('.').

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

When the input array of digit strings contains any strings represented by multiple Java chars, then [getDigits()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getDigits())will return the default digits ('0' - '9') and [getZeroDigit()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getZeroDigit())will return the default zero digit ('0').

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

- [#getExponentSeparator](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getExponentSeparator()) 

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

- [#setGroupingSeparatorString(String)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setGroupingSeparatorString(kotlin.String)) 

### setGroupingSeparatorString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingSeparatorString(groupingSeparatorString: String!): Unit
```

**\[icu\]**Sets the string used for grouping separator.

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getGroupingSeparator()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getGroupingSeparator())will return the default grouping separator character (',').

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

**Note:** When the input minus sign String is represented by multiple Java chars, then [getMinusSign()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMinusSign())will return the default minus sign character ('-').

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

**Note:** When the input monetary decimal separator String is represented by multiple Java chars, then [getMonetaryDecimalSeparatorString()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryDecimalSeparatorString())will return the default monetary decimal separator character ('.').

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

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getMonetaryGroupingSeparator()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMonetaryGroupingSeparator())will return the default monetary grouping separator character (',').

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

- [#getPadEscape](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPadEscape())
- [android.icu.text.DecimalFormat#setFormatWidth](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int))
- [android.icu.text.DecimalFormat#setPadPosition](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int))
- [android.icu.text.DecimalFormat#setPadCharacter](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadCharacter(kotlin.Char)) 

### setPatternForCurrencySpacing

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPatternForCurrencySpacing(
    itemType: Int, 
    beforeCurrency: Boolean, 
    pattern: String!
): Unit
```

**\[icu\]** Sets the indicated currency spacing pattern or value. See [getPatternForCurrencySpacing](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean))for more information.

Values for currency match and surrounding match must be patterns. Values for insert can be any string.

**Note:**ICU4J does not currently use this information.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `itemType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of CURRENCY_SPC_CURRENCY_MATCH, CURRENCY_SPC_SURROUNDING_MATCH or CURRENCY_SPC_INSERT |
| `beforeCurrency` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the pattern is for before the currency symbol. false if the pattern is for after it. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string to override current setting; can be null. |
| --- | --- |

**See Also**

- [#getPatternForCurrencySpacing(int, boolean)](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPatternForCurrencySpacing(kotlin.Int,%20kotlin.Boolean)) 

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

**Note:** When the input permille String is represented by multiple Java chars, then [getPerMill()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPerMill())will return the default permille character ('‰').

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

**Note:** When the input grouping separator String is represented by multiple Java chars, then [getPercent()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPercent())will return the default percent sign character ('%').

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

- [#getPlusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPlusSign())
- [#setMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#setMinusSign(kotlin.Char))
- [#getMinusSign](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getMinusSign()) 

### setPlusSignString

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlusSignString(plusSignString: String!): Unit
```

**\[icu\]**Sets the localized plus sign string.

**Note:** When the input plus sign String is represented by multiple Java chars, then [getPlusSign()](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getPlusSign())will return the default plus sign character ('+').

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
