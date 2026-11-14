# NumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberFormat

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/NumberFormat "View this page in Java") 

```
abstract class NumberFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) |||
| | ↳ | [android.icu.text.UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat) ||
| | | ↳ | [android.icu.text.NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#) |

| Known Direct Subclasses [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat) |------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------| | [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat.html#). | |

| Known Indirect Subclasses [CompactDecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/CompactDecimalFormat) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [CompactDecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/CompactDecimalFormat) | Formats numbers in compact (abbreviated) notation, like "1. | |

**\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

**IMPORTANT:** New users are strongly encouraged to see if [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) fits their use case. Although not deprecated, this class, NumberFormat, is only provided for java.text.NumberFormat compatibility.
`NumberFormat`is the abstract base class for all number formats. This class provides the interface for formatting and parsing numbers.`NumberFormat`also provides methods for determining which locales have number formats, and what their names are.`NumberFormat`helps you to format and parse numbers for any locale. Your code can be completely independent of the locale conventions for decimal points, thousands-separators, or even the particular decimal digits used, or whether the number format is even decimal.

To format a number for the current Locale, use one of the factory class methods: 

```kotlin
myString = NumberFormat.getInstance().format(myNumber);
  
```
If you are formatting multiple numbers, it is more efficient to get the format and use it multiple times so that the system doesn't have to fetch the information about the local language and country conventions multiple times. 

```kotlin
NumberFormat nf = NumberFormat.getInstance();
  for (int i = 0; i < a.length; ++i) {
      output.println(nf.format(myNumber[i]) + "; ");
  }
  
```
To format a number for a different Locale, specify it in the call to`getInstance`. 

```kotlin
NumberFormat nf = NumberFormat.getInstance(Locale.FRENCH);
  
```
You can also use a`NumberFormat`to parse numbers: 

```kotlin
myNumber = nf.parse(myString);
  
```
Use`getInstance`or`getNumberInstance`to get the normal number format. Use`getIntegerInstance`to get an integer number format. Use`getCurrencyInstance`to get the currency number format. And use`getPercentInstance`to get a format for displaying percentages. Some factory methods are found within subclasses of NumberFormat. With this format, a fraction like 0.53 is displayed as 53%.

Starting from ICU 4.2, you can use getInstance() by passing in a 'style' as parameter to get the correct instance. For example, use getInstance(...NUMBERSTYLE) to get the normal number format, getInstance(...PERCENTSTYLE) to get a format for displaying percentage, getInstance(...SCIENTIFICSTYLE) to get a format for displaying scientific number, getInstance(...INTEGERSTYLE) to get an integer number format, getInstance(...CURRENCYSTYLE) to get the currency number format, in which the currency is represented by its symbol, for example, "$3.00". getInstance(...ISOCURRENCYSTYLE) to get the currency number format, in which the currency is represented by its ISO code, for example "USD3.00". getInstance(...PLURALCURRENCYSTYLE) to get the currency number format, in which the currency is represented by its full name in plural format, for example, "3.00 US dollars" or "1.00 US dollar".

You can also control the display of numbers with such methods as`setMinimumFractionDigits`. If you want even more control over the format or parsing, or want to give your users more control, you can try casting the`NumberFormat`you get from the factory methods to a`DecimalFormat`. This will work for the vast majority of locales; just remember to put it in a`try`block in case you encounter an unusual one.

NumberFormat is designed such that some controls work for formatting and others work for parsing. The following is the detailed description for each these control methods,

setParseIntegerOnly : only affects parsing, e.g. if true, "3456.78" -\> 3456 (and leaves the parse position just after '6') if false, "3456.78" -\> 3456.78 (and leaves the parse position just after '8') This is independent of formatting. If you want to not show a decimal point where there might be no digits after the decimal point, use setDecimalSeparatorAlwaysShown on DecimalFormat.

You can also use forms of the`parse`and`format`methods with`ParsePosition`and`FieldPosition`to allow you to:

- progressively parse through pieces of a string
- align the decimal point and other areas

For example, you can align numbers in two ways:

1. If you are using a monospaced font with spacing for alignment, you can pass the`FieldPosition`in your format call, with`field`=`INTEGER_FIELD`. On output,`getEndIndex`will be set to the offset between the last character of the integer and the decimal. Add (desiredSpaceCount - getEndIndex) spaces at the front of the string.
2. If you are using proportional fonts, instead of padding with spaces, measure the width of the string in pixels from the start to`getEndIndex`. Then move the pen by (desiredPixelWidth - widthToAlignmentPoint) before drawing the text. It also works where there is no decimal, but possibly additional characters at the end, e.g., with parentheses in negative numbers: "(12)" for -12.

### Synchronization

Number formats are generally not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

#### DecimalFormat

DecimalFormat is the concrete implementation of NumberFormat, and the NumberFormat API is essentially an abstraction from DecimalFormat's API. Refer to DecimalFormat for more information about this API.
see DecimalFormat see java.text.ChoiceFormat

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat.Field) The instances of this inner class are used as attribute keys and values in AttributedCharacterIterator that NumberFormat. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCOUNTINGCURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#ACCOUNTINGCURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify currency style of format which uses currency symbol to represent currency for accounting, for example: "($3.00), instead of "-$3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASHCURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CASHCURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify currency cash style of format which uses currency ISO code to represent currency, for example: "NT$3" instead of "NT$3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify general currency style of format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTION_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#FRACTION_FIELD:kotlin.Int) Field constant used to construct a FieldPosition object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGERSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#INTEGERSTYLE:kotlin.Int) **\[icu\]**Constant to specify a integer number style format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGER_FIELD](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#INTEGER_FIELD:kotlin.Int) Field constant used to construct a FieldPosition object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ISOCURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#ISOCURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify currency style of format which uses currency ISO code to represent currency, for example: "USD3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NUMBERSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#NUMBERSTYLE:kotlin.Int) **\[icu\]**Constant to specify normal number style of format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERCENTSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#PERCENTSTYLE:kotlin.Int) **\[icu\]**Constant to specify a style of format to display percent. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLURALCURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#PLURALCURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify currency style of format which uses currency long name with plural format to represent currency, for example, "3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCIENTIFICSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#SCIENTIFICSTYLE:kotlin.Int) **\[icu\]**Constant to specify a style of format to display scientific number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARDCURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#STANDARDCURRENCYSTYLE:kotlin.Int) **\[icu\]**Constant to specify currency style of format which uses currency symbol to represent currency, for example "$3. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#NumberFormat())`()` Empty constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#clone())`()` Overrides clone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.math.BigDecimal))`(`number:` ` [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!`)` **\[icu\]**Convenience method to format an ICU BigDecimal. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.math.BigDecimal,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` **\[icu\]**Formats an ICU BigDecimal. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.util.CurrencyAmount))`(`currAmt:` ` [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#)!`)` **\[icu\]**Convenience method to format a CurrencyAmount. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.util.CurrencyAmount,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`currAmt:` ` [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` **\[icu\]**Formats a CurrencyAmount. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Double))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Specialization of format. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` Specialization of format. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` Formats a number and appends the resulting text to the given string buffer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigDecimal))`(`number:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Convenience method to format a BigDecimal. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigDecimal,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` **\[icu\]**Formats a BigDecimal. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigInteger))`(`number:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` **\[icu\]**Convenience method to format a BigInteger. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigInteger,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` **\[icu\]**Formats a BigInteger. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Long))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Specialization of format. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | [format](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!`)` Specialization of format. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getAvailableLocales())`()` Returns the list of Locales for which NumberFormats are available. |
| open [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | [getContext](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getContext(android.icu.text.DisplayContext.Type))`(`type:` ` [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!`)` **\[icu\]**Get the formatter's DisplayContext value for the specified DisplayContext. |
| open [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)! | [getCurrency](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrency())`()` Returns the Currency object used to display currency amounts. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getCurrencyInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getCurrencyInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getCurrencyInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(android.icu.util.ULocale,%20kotlin.Int))`(`desiredLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `choice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(kotlin.Int))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(java.util.Locale,%20kotlin.Int))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getIntegerInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getIntegerInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getIntegerInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMaximumFractionDigits())`()` Returns the maximum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMaximumIntegerDigits())`()` Returns the maximum number of digits allowed in the integer portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMinimumFractionDigits())`()` Returns the minimum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMinimumIntegerDigits())`()` Returns the minimum number of digits allowed in the integer portion of a number. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getNumberInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getNumberInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getNumberInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getPercentInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getPercentInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getPercentInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRoundingMode](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getRoundingMode())`()` Returns the rounding mode used in this NumberFormat. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getScientificInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance())`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getScientificInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance(android.icu.util.ULocale))`(`inLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | [getScientificInstance](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#hashCode())`()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupingUsed](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isGroupingUsed())`()` Returns true if grouping is used in this format. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly())`()` Returns true if this format will parse numbers as integers only. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseStrict](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseStrict())`()` **\[icu\]**Returns whether strict parsing is in effect. |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [parse](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parse(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce a number. |
| abstract [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [parse](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsePosition:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals); otherwise, returns another type, such as a BigDecimal, BigInteger, or Double. |
| open [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#)! | [parseCurrency](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parseCurrency(kotlin.CharSequence,%20java.text.ParsePosition))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` Parses text from the given string as a CurrencyAmount. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsePosition:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!`)` Parses text from a string to produce a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setContext(android.icu.text.DisplayContext))`(`context:` ` [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!`)` **\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setCurrency(android.icu.util.Currency))`(`theCurrency:` ` [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)!`)` Sets the Currency object used to display currency amounts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingUsed](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setGroupingUsed(kotlin.Boolean))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not grouping will be used in this format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMaximumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMaximumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMinimumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMinimumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setParseIntegerOnly(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to ignore the fraction part of a number when parsing (defaults to false). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseStrict](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setParseStrict(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**Sets whether strict parsing is in effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoundingMode](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setRoundingMode(kotlin.Int))`(`roundingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the rounding mode used in this NumberFormat. |

| Protected methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPattern](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPattern(android.icu.util.ULocale,%20kotlin.Int))`(`forLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`, `choice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the pattern for the provided locale and choice. |

## Constants

### ACCOUNTINGCURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNTINGCURRENCYSTYLE: Int
```

**\[icu\]** Constant to specify currency style of format which uses currency symbol to represent currency for accounting, for example: "($3.00), instead of "-$3.00" ([CURRENCYSTYLE](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CURRENCYSTYLE:kotlin.Int)). Overrides any style specified using -cf- key in locale. 

 Value: 7

### CASHCURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASHCURRENCYSTYLE: Int
```

**\[icu\]**Constant to specify currency cash style of format which uses currency ISO code to represent currency, for example: "NT$3" instead of "NT$3.23". 

 Value: 8

### CURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CURRENCYSTYLE: Int
```

**\[icu\]**Constant to specify general currency style of format. Defaults to STANDARDCURRENCYSTYLE, using currency symbol, for example "$3.00", with non-accounting style for negative values (e.g. minus sign). The specific style may be specified using the -cf- locale key. 

 Value: 1

### FRACTION_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRACTION_FIELD: Int
```

Field constant used to construct a FieldPosition object. Signifies that the position of the fraction part of a formatted number should be returned. 

 Value: 1

**See Also**

- [java.text.FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#) 

### INTEGERSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTEGERSTYLE: Int
```

**\[icu\]**Constant to specify a integer number style format. 

 Value: 4

### INTEGER_FIELD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTEGER_FIELD: Int
```

Field constant used to construct a FieldPosition object. Signifies that the position of the integer part of a formatted number should be returned. 

 Value: 0

**See Also**

- [java.text.FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#) 

### ISOCURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ISOCURRENCYSTYLE: Int
```

**\[icu\]**Constant to specify currency style of format which uses currency ISO code to represent currency, for example: "USD3.00". 

 Value: 5

### NUMBERSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMBERSTYLE: Int
```

**\[icu\]**Constant to specify normal number style of format. 

 Value: 0

### PERCENTSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERCENTSTYLE: Int
```

**\[icu\]**Constant to specify a style of format to display percent. 

 Value: 2

### PLURALCURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLURALCURRENCYSTYLE: Int
```

**\[icu\]**Constant to specify currency style of format which uses currency long name with plural format to represent currency, for example, "3.00 US Dollars". 

 Value: 6

### SCIENTIFICSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCIENTIFICSTYLE: Int
```

**\[icu\]**Constant to specify a style of format to display scientific number. 

 Value: 3

### STANDARDCURRENCYSTYLE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARDCURRENCYSTYLE: Int
```

**\[icu\]**Constant to specify currency style of format which uses currency symbol to represent currency, for example "$3.00", using non-accounting style for negative values (e.g. minus sign). Overrides any style specified using -cf- key in locale. 

 Value: 9

## Public constructors

### NumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NumberFormat()
```

Empty constructor. Public for API compatibility with historic versions of [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#) which had public constructor even though this is an abstract class.

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides clone.

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

Overrides equals. Two NumberFormats are equal they are of the same class and the user-specified values for settings (groupingUsed, parseIntegerOnly, maximumIntegerDigits, etc.) are equal.

| Parameters ||
|-------|-------------------------------|
| `obj` | the object to compare against |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the object is equal to this. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: BigDecimal!): String!
```

**\[icu\]**Convenience method to format an ICU BigDecimal. 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: BigDecimal!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

**\[icu\]**Formats an ICU BigDecimal. Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(currAmt: CurrencyAmount!): String!
```

**\[icu\]**Convenience method to format a CurrencyAmount. 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    currAmt: CurrencyAmount!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

**\[icu\]**Formats a CurrencyAmount. Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Double): String!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: Double, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Any!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Formats a number and appends the resulting text to the given string buffer.**\[icu\] Note:** recognizes`BigInteger`and`BigDecimal`objects.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)!:where the text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#)!:A`FieldPosition`identifying a field in the formatted text |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |

**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: BigDecimal!): String!
```

Convenience method to format a BigDecimal. 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: BigDecimal!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

**\[icu\]**Formats a BigDecimal. Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: BigInteger!): String!
```

**\[icu\]**Convenience method to format a BigInteger. 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: BigInteger!, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

**\[icu\]**Formats a BigInteger. Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Long): String!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: Long, 
    toAppendTo: StringBuffer!, 
    pos: FieldPosition!
): StringBuffer!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)) 

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns the list of Locales for which NumberFormats are available.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | the available locales |

### getContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(type: DisplayContext.Type!): DisplayContext!
```

**\[icu\]**Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [DisplayContext.Type](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type)!:the DisplayContext.Type whose value to return |

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)! | the current DisplayContext setting for the specified type |

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the Currency object used to display currency amounts. This may be null. 

### getCurrencyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCurrencyInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a currency format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for currency |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getCurrencyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a currency format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for currency |

### getCurrencyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a currency format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for currency |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns the default number format for the current default`FORMAT`locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getIntegerInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    desiredLocale: ULocale!, 
    choice: Int
): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a specific style number format for a specific locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------|
| `desiredLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the specific locale. |
| `choice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if choice is not one of NUMBERSTYLE, CURRENCYSTYLE, PERCENTSTYLE, SCIENTIFICSTYLE, INTEGERSTYLE, ISOCURRENCYSTYLE, PLURALCURRENCYSTYLE, ACCOUNTINGCURRENCYSTYLE. CASHCURRENCYSTYLE, STANDARDCURRENCYSTYLE. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(style: Int): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]** Returns a specific style number format for default`FORMAT`locale.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    inLocale: Locale!, 
    style: Int
): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a specific style number format for a specific locale.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the specific locale. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntegerInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns an integer number format for the current default`FORMAT`locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly())).

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for integer values |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIntegerInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]** Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly())).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `inLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale for which a number format is needed |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for integer values |

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIntegerInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly())).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale for which a number format is needed |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for integer values |

### getMaximumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumFractionDigits(): Int
```

Returns the maximum number of digits allowed in the fraction portion of a number. The default value is 3, which subclasses can override. When formatting, the exact behavior when this value is exceeded is subclass-specific. When parsing, this has no effect.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of fraction digits |

**See Also**

- [#setMaximumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMaximumFractionDigits(kotlin.Int)) 

### getMaximumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumIntegerDigits(): Int
```

Returns the maximum number of digits allowed in the integer portion of a number. The default value is 40, which subclasses can override. When formatting, if the number of digits exceeds this value, the highest- significance digits are truncated until the limit is reached, in accordance with UTS#35. This setting has no effect on parsing.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of integer digits |

**See Also**

- [#setMaximumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMaximumIntegerDigits(kotlin.Int)) 

### getMinimumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumFractionDigits(): Int
```

Returns the minimum number of digits allowed in the fraction portion of a number. The default value is 0, which subclasses can override. When formatting, if this value is not reached, numbers are padded on the right with the locale-specific '0' character to ensure at least this number of fraction digits. When parsing, this has no effect.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of fraction digits |

**See Also**

- [#setMinimumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMinimumFractionDigits(kotlin.Int)) 

### getMinimumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumIntegerDigits(): Int
```

Returns the minimum number of digits allowed in the integer portion of a number. The default value is 1, which subclasses can override. When formatting, if this value is not reached, numbers are padded on the left with the locale-specific '0' character to ensure at least this number of integer digits. When parsing, this has no effect.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of integer digits |

**See Also**

- [#setMinimumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setMinimumIntegerDigits(kotlin.Int)) 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNumberInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a general-purpose number format for the current default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a general-purpose number format for the specified locale. 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a general-purpose number format for the specified locale. 

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPercentInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a percentage format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for percents |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPercentInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a percentage format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for percents |

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPercentInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat. Returns a percentage format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a number format for percents |

### getRoundingMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundingMode(): Int
```

Returns the rounding mode used in this NumberFormat. The default implementation of tis method in NumberFormat always throws`UnsupportedOperationException`.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A rounding mode, between`BigDecimal.ROUND_UP`and`BigDecimal.ROUND_UNNECESSARY`. |

**See Also**

- [#setRoundingMode(int)](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setRoundingMode(kotlin.Int)) 

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getScientificInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]** Returns a scientific format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a scientific number format |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#) 

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getScientificInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a scientific format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a scientific number format |

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getScientificInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#) instead of NumberFormat.**\[icu\]**Returns a scientific format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#)! | a scientific number format |

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

### isGroupingUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isGroupingUsed(): Boolean
```

Returns true if grouping is used in this format. For example, in the en_US locale, with grouping on, the number 1234567 will be formatted as "1,234,567". The grouping separator as well as the size of each group is locale-dependent and is determined by subclasses of NumberFormat. Grouping affects both parsing and formatting.

| Return ||
|------------------------------------------------------------------------------------|--------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if grouping is used |

**See Also**

- [#setGroupingUsed](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setGroupingUsed(kotlin.Boolean)) 

### isParseIntegerOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isParseIntegerOnly(): Boolean
```

Returns true if this format will parse numbers as integers only. For example in the English locale, with ParseIntegerOnly true, the string "1234." would be parsed as the integer value 1234 and parsing would stop at the "." character. The decimal separator accepted by the parse operation is locale-dependent and determined by the subclass.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this will parse integers only |

### isParseStrict

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isParseStrict(): Boolean
```

**\[icu\]**Returns whether strict parsing is in effect.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if strict parsing is in effect |

**See Also**

- [#setParseStrict](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setParseStrict(kotlin.Boolean)) 

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(text: String!): Number!
```

Parses text from the beginning of the given string to produce a number. The method might not use the entire text of the given string.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A String whose beginning should be parsed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | A Number parsed from the string. |

| Exceptions ||
|----------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |

**See Also**

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(
    text: String!, 
    parsePosition: ParsePosition!
): Number!
```

Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals); otherwise, returns another type, such as a BigDecimal, BigInteger, or Double. The return type is not guaranteed other than for the Long case.

If IntegerOnly is set, will stop at a decimal point (or equivalent; e.g., for rational numbers "1 2/3", will stop after the 1).

Does not throw an exception; if no object can be parsed, index is unchanged!

For more detail on parsing, see the "Parsing" header in the class documentation of [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat). 
**See Also**

- [#isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly())
- [android.icu.text.DecimalFormat#setParseBigDecimal](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseBigDecimal(kotlin.Boolean))
- [java.text.Format#parseObject(String, ParsePosition)](https://developer.android.com/reference/kotlin/java/text/Format.html#parseObject(kotlin.String,%20java.text.ParsePosition)) 

### parseCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parseCurrency(
    text: CharSequence!, 
    pos: ParsePosition!
): CurrencyAmount!
```

Parses text from the given string as a CurrencyAmount. Unlike the parse() method, this method will attempt to parse a generic currency name, searching for a match of this object's locale's currency display names, or for a 3-letter ISO currency code. This method will fail if this format is not a currency format, that is, if it does not contain the currency pattern symbol (U+00A4) in its prefix or suffix.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text to parse |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!:input-output position; on input, the position within text to match; must have 0 \<= pos.getIndex() \< text.length(); on output, the position after the last matched character. If the parse fails, the position in unchanged upon output. |

| Return ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------|
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#)! | a CurrencyAmount, or null upon failure |

### parseObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseObject(
    source: String!, 
    parsePosition: ParsePosition!
): Any!
```

Parses text from a string to produce a number.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the String to parse |
| `pos` | A`ParsePosition`object with index and error index information as described above. |
| `parsePosition` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#)!:the position at which to start the parse |

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the parsed number, or null |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |

**See Also**

- [java.text.NumberFormat#parseObject(String, ParsePosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#parseObject(kotlin.String,%20java.text.ParsePosition)) 

### setContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: DisplayContext!): Unit
```

**\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext)!:The DisplayContext value to set. |

### setCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrency(theCurrency: Currency!): Unit
```

Sets the Currency object used to display currency amounts. This takes effect immediately, if this format is a currency format. If this format is not a currency format, then the currency object is used if and when this object becomes a currency format.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theCurrency` | [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#)!:new currency object to use. May be null for some subclasses. |

### setGroupingUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingUsed(newValue: Boolean): Unit
```

Sets whether or not grouping will be used in this format. Grouping affects both parsing and formatting.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to use grouping. |

**See Also**

- [#isGroupingUsed](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isGroupingUsed()) 

### setMaximumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumFractionDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the fraction portion of a number. This must be \>= minimumFractionDigits. If the new value for maximumFractionDigits is less than the current value of minimumFractionDigits, then minimumFractionDigits will also be set to the new value.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMaximumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMaximumFractionDigits()) 

### setMaximumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumIntegerDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the integer portion of a number. This must be \>= minimumIntegerDigits. If the new value for maximumIntegerDigits is less than the current value of minimumIntegerDigits, then minimumIntegerDigits will also be set to the new value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of integer digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMaximumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMaximumIntegerDigits()) 

### setMinimumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumFractionDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the fraction portion of a number. This must be \<= maximumFractionDigits. If the new value for minimumFractionDigits exceeds the current value of maximumFractionDigits, then maximumFractionDigits will also be set to the new value.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of fraction digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMinimumFractionDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMinimumFractionDigits()) 

### setMinimumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumIntegerDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the integer portion of a number. This must be \<= maximumIntegerDigits. If the new value for minimumIntegerDigits is more than the current value of maximumIntegerDigits, then maximumIntegerDigits will also be set to the new value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of integer digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMinimumIntegerDigits](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getMinimumIntegerDigits()) 

### setParseIntegerOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParseIntegerOnly(value: Boolean): Unit
```

Sets whether to ignore the fraction part of a number when parsing (defaults to false). If a string contains a decimal point, parsing will stop before the decimal point. Note that determining whether a character is a decimal point depends on the locale.

For example, in*en-US*, parsing the string "123.45" will return the number 123 and parse position 3.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this should parse integers only |

**See Also**

- [#isParseIntegerOnly](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly()) 

### setParseStrict

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParseStrict(value: Boolean): Unit
```

**\[icu\]**Sets whether strict parsing is in effect. When this is true, the string is required to be a stronger match to the pattern than when lenient parsing is in effect. More specifically, the following conditions cause a parse failure relative to lenient mode (examples use the pattern "#,##0.#"):

- The presence and position of special symbols, including currency, must match the pattern. 
 '+123' fails (there is no plus sign in the pattern)
- Leading or doubled grouping separators 
 ',123' and '1,,234" fail
- Groups of incorrect length when grouping is used 
 '1,23' and '1234,567' fail, but '1234' passes
- Grouping separators used in numbers followed by exponents 
 '1,234E5' fails, but '1234E5' and '1,234E' pass ('E' is not an exponent when not followed by a number)

When strict parsing is off, all grouping separators are ignored. This is the default behavior.

<br />

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to enable strict parsing. Default is false. |

**See Also**

- [#isParseStrict](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseStrict()) 

### setRoundingMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRoundingMode(roundingMode: Int): Unit
```

Set the rounding mode used in this NumberFormat. The default implementation of tis method in NumberFormat always throws`UnsupportedOperationException`.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `roundingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A rounding mode, between`BigDecimal.ROUND_UP`and`BigDecimal.ROUND_UNNECESSARY`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getRoundingMode()>

## Protected methods

### getPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open static fun getPattern(
    forLocale: ULocale!, 
    choice: Int
): String!
```

Returns the pattern for the provided locale and choice.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `forLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:the locale of the data. |
| `choice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the pattern format. |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern |
