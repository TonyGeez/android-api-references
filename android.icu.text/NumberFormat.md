# NumberFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberFormat

Kotlin| [Java](../android/icu/text/NumberFormat.md) 
| --- | --- |

```
abstract class NumberFormat : UFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](../java/text/Format.md) |||
| | ↳ | [android.icu.text.UFormat](../android/icu/text/UFormat.md) ||
| | | ↳ | [android.icu.text.NumberFormat](../android/icu/text/NumberFormat.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DecimalFormat](../android/icu/text/DecimalFormat.md) |------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------| | [DecimalFormat](../android/icu/text/DecimalFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](../java/text/DecimalFormat.md). | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) |--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------| | [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. | |
| --- | --- | --- | --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](../java/text/NumberFormat.md). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

**IMPORTANT:** New users are strongly encouraged to see if [NumberFormatter](../android/icu/number/NumberFormatter.md) fits their use case. Although not deprecated, this class, NumberFormat, is only provided for java.text.NumberFormat compatibility.
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
| open | [Field](../android/icu/text/NumberFormat.Field.md) The instances of this inner class are used as attribute keys and values in AttributedCharacterIterator that NumberFormat. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCOUNTINGCURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify currency style of format which uses currency symbol to represent currency for accounting, for example: "($3.00), instead of "-$3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASHCURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify currency cash style of format which uses currency ISO code to represent currency, for example: "NT$3" instead of "NT$3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify general currency style of format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTION_FIELD](../android/icu/text/NumberFormat.md) Field constant used to construct a FieldPosition object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGERSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify a integer number style format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGER_FIELD](../android/icu/text/NumberFormat.md) Field constant used to construct a FieldPosition object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ISOCURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify currency style of format which uses currency ISO code to represent currency, for example: "USD3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NUMBERSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify normal number style of format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERCENTSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify a style of format to display percent. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLURALCURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify currency style of format which uses currency long name with plural format to represent currency, for example, "3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCIENTIFICSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify a style of format to display scientific number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STANDARDCURRENCYSTYLE](../android/icu/text/NumberFormat.md) **\[icu\]**Constant to specify currency style of format which uses currency symbol to represent currency, for example "$3. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [NumberFormat](../android/icu/text/NumberFormat.md))`()` Empty constructor. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../android/icu/text/NumberFormat.md))`()` Overrides clone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/text/NumberFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigDecimal](../android/icu/math/BigDecimal.md)!`)` **\[icu\]**Convenience method to format an ICU BigDecimal. |
| --- | --- |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigDecimal](../android/icu/math/BigDecimal.md)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` **\[icu\]**Formats an ICU BigDecimal. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`currAmt:` ` [CurrencyAmount](../android/icu/util/CurrencyAmount.md)!`)` **\[icu\]**Convenience method to format a CurrencyAmount. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`currAmt:` ` [CurrencyAmount](../android/icu/util/CurrencyAmount.md)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` **\[icu\]**Formats a CurrencyAmount. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Specialization of format. |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Specialization of format. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Formats a number and appends the resulting text to the given string buffer. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigDecimal](../java/math/BigDecimal.md)!`)` Convenience method to format a BigDecimal. |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigDecimal](../java/math/BigDecimal.md)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` **\[icu\]**Formats a BigDecimal. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigInteger](../java/math/BigInteger.md)!`)` **\[icu\]**Convenience method to format a BigInteger. |
| --- | --- |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [BigInteger](../java/math/BigInteger.md)!`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` **\[icu\]**Formats a BigInteger. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Specialization of format. |
| abstract [StringBuffer](../java/lang/StringBuffer.md)! | [format](../android/icu/text/NumberFormat.md))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `toAppendTo:` ` [StringBuffer](../java/lang/StringBuffer.md)!`, `pos:` ` [FieldPosition](../java/text/FieldPosition.md)!`)` Specialization of format. |
| --- | --- |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](../java/util/Locale.md)!\>! | [getAvailableLocales](../android/icu/text/NumberFormat.md))`()` Returns the list of Locales for which NumberFormats are available. |
| open [DisplayContext](../android/icu/text/DisplayContext.md)! | [getContext](../android/icu/text/NumberFormat.md))`(`type:` ` [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)!`)` **\[icu\]**Get the formatter's DisplayContext value for the specified DisplayContext. |
| open [Currency](../android/icu/util/Currency.md)! | [getCurrency](../android/icu/text/NumberFormat.md))`()` Returns the Currency object used to display currency amounts. |
| --- | --- |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getCurrencyInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getCurrencyInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getCurrencyInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`(`desiredLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `choice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`(`style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`, `style:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getIntegerInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getIntegerInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getIntegerInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumFractionDigits](../android/icu/text/NumberFormat.md))`()` Returns the maximum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumIntegerDigits](../android/icu/text/NumberFormat.md))`()` Returns the maximum number of digits allowed in the integer portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFractionDigits](../android/icu/text/NumberFormat.md))`()` Returns the minimum number of digits allowed in the fraction portion of a number. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumIntegerDigits](../android/icu/text/NumberFormat.md))`()` Returns the minimum number of digits allowed in the integer portion of a number. |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getNumberInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getNumberInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getNumberInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getPercentInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getPercentInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getPercentInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRoundingMode](../android/icu/text/NumberFormat.md))`()` Returns the rounding mode used in this NumberFormat. |
| static [NumberFormat](../android/icu/text/NumberFormat.md)! | [getScientificInstance](../android/icu/text/NumberFormat.md))`()` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| --- | --- |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getScientificInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| openstatic [NumberFormat](../android/icu/text/NumberFormat.md)! | [getScientificInstance](../android/icu/text/NumberFormat.md))`(`inLocale:` ` [Locale](../java/util/Locale.md)!`)` **NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/text/NumberFormat.md))`()` Returns a hash code value for the object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupingUsed](../android/icu/text/NumberFormat.md))`()` Returns true if grouping is used in this format. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseIntegerOnly](../android/icu/text/NumberFormat.md))`()` Returns true if this format will parse numbers as integers only. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseStrict](../android/icu/text/NumberFormat.md))`()` **\[icu\]**Returns whether strict parsing is in effect. |
| --- | --- |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [parse](../android/icu/text/NumberFormat.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parses text from the beginning of the given string to produce a number. |
| abstract [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [parse](../android/icu/text/NumberFormat.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsePosition:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals); otherwise, returns another type, such as a BigDecimal, BigInteger, or Double. |
| open [CurrencyAmount](../android/icu/util/CurrencyAmount.md)! | [parseCurrency](../android/icu/text/NumberFormat.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `pos:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Parses text from the given string as a CurrencyAmount. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](../android/icu/text/NumberFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `parsePosition:` ` [ParsePosition](../java/text/ParsePosition.md)!`)` Parses text from a string to produce a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](../android/icu/text/NumberFormat.md))`(`context:` ` [DisplayContext](../android/icu/text/DisplayContext.md)!`)` **\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](../android/icu/text/NumberFormat.md))`(`theCurrency:` ` [Currency](../android/icu/util/Currency.md)!`)` Sets the Currency object used to display currency amounts. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingUsed](../android/icu/text/NumberFormat.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not grouping will be used in this format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumFractionDigits](../android/icu/text/NumberFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumIntegerDigits](../android/icu/text/NumberFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the integer portion of a number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFractionDigits](../android/icu/text/NumberFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumIntegerDigits](../android/icu/text/NumberFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseIntegerOnly](../android/icu/text/NumberFormat.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to ignore the fraction part of a number when parsing (defaults to false). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseStrict](../android/icu/text/NumberFormat.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` **\[icu\]**Sets whether strict parsing is in effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoundingMode](../android/icu/text/NumberFormat.md))`(`roundingMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the rounding mode used in this NumberFormat. |

| Protected methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPattern](../android/icu/text/NumberFormat.md))`(`forLocale:` ` [ULocale](../android/icu/util/ULocale.md)!`, `choice:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the pattern for the provided locale and choice. |

## Constants

### ACCOUNTINGCURRENCYSTYLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCOUNTINGCURRENCYSTYLE: Int
```

**\[icu\]** Constant to specify currency style of format which uses currency symbol to represent currency for accounting, for example: "($3.00), instead of "-$3.00" ([CURRENCYSTYLE](../android/icu/text/NumberFormat.md)). Overrides any style specified using -cf- key in locale. 

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

- [java.text.FieldPosition](../java/text/FieldPosition.md) 

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

- [java.text.FieldPosition](../java/text/FieldPosition.md) 

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

Empty constructor. Public for API compatibility with historic versions of [java.text.NumberFormat](../java/text/NumberFormat.md) which had public constructor even though this is an abstract class.

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Double): String!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object)](../java/text/Format.md)) 

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

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
| `toAppendTo` | [StringBuffer](../java/lang/StringBuffer.md)!:where the text is to be appended |
| `pos` | [FieldPosition](../java/text/FieldPosition.md)!:A`FieldPosition`identifying a field in the formatted text |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [StringBuffer](../java/lang/StringBuffer.md)! | the string buffer passed in as`toAppendTo`, with formatted text appended |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if the Format cannot format the given object |

**See Also**

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Long): String!
```

Specialization of format. 
**See Also**

- [java.text.Format#format(Object)](../java/text/Format.md)) 

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

- [java.text.Format#format(Object, StringBuffer, FieldPosition)](../java/text/Format.md)) 

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Returns the list of Locales for which NumberFormats are available.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java/util/Locale.md)!>! | the available locales |

### getContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(type: DisplayContext.Type!): DisplayContext!
```

**\[icu\]**Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [DisplayContext.Type](../android/icu/text/DisplayContext.Type.md)!:the DisplayContext.Type whose value to return |

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [DisplayContext](../android/icu/text/DisplayContext.md)! | the current DisplayContext setting for the specified type |

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

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a currency format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for currency |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getCurrencyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a currency format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for currency |

### getCurrencyInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a currency format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for currency |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns the default number format for the current default`FORMAT`locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getIntegerInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    desiredLocale: ULocale!, 
    choice: Int
): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a specific style number format for a specific locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------|
| `desiredLocale` | [ULocale](../android/icu/util/ULocale.md)!:the specific locale. |
| `choice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if choice is not one of NUMBERSTYLE, CURRENCYSTYLE, PERCENTSTYLE, SCIENTIFICSTYLE, INTEGERSTYLE, ISOCURRENCYSTYLE, PLURALCURRENCYSTYLE, ACCOUNTINGCURRENCYSTYLE. CASHCURRENCYSTYLE, STANDARDCURRENCYSTYLE. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(style: Int): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]** Returns a specific style number format for default`FORMAT`locale.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    inLocale: Locale!, 
    style: Int
): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a specific style number format for a specific locale.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](../java/util/Locale.md)!:the specific locale. |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number format style |

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntegerInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns an integer number format for the current default`FORMAT`locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](../android/icu/math/BigDecimal.md)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](../android/icu/text/NumberFormat.md))).

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for integer values |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIntegerInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]** Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](../android/icu/math/BigDecimal.md)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](../android/icu/text/NumberFormat.md))).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `inLocale` | [ULocale](../android/icu/util/ULocale.md)!:the locale for which a number format is needed |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for integer values |

### getIntegerInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIntegerInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see [ROUND_HALF_EVEN](../android/icu/math/BigDecimal.md)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](../android/icu/text/NumberFormat.md))).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](../java/util/Locale.md)!:the locale for which a number format is needed |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for integer values |

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

- [#setMaximumFractionDigits](../android/icu/text/NumberFormat.md)) 

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

- [#setMaximumIntegerDigits](../android/icu/text/NumberFormat.md)) 

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

- [#setMinimumFractionDigits](../android/icu/text/NumberFormat.md)) 

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

- [#setMinimumIntegerDigits](../android/icu/text/NumberFormat.md)) 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNumberInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a general-purpose number format for the current default`FORMAT`locale. 
**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a general-purpose number format for the specified locale. 

### getNumberInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a general-purpose number format for the specified locale. 

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPercentInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a percentage format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for percents |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPercentInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a percentage format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for percents |

### getPercentInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPercentInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat. Returns a percentage format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a number format for percents |

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

- [#setRoundingMode(int)](../android/icu/text/NumberFormat.md)) 

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getScientificInstance(): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]** Returns a scientific format for the current default`FORMAT`locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a scientific number format |

**See Also**

- [android.icu.util.ULocale.Category#FORMAT](../android/icu/util/ULocale.Category.md) 

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getScientificInstance(inLocale: ULocale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a scientific format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a scientific number format |

### getScientificInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getScientificInstance(inLocale: Locale!): NumberFormat!
```

**NOTE:** New users are strongly encouraged to use [NumberFormatter](../android/icu/number/NumberFormatter.md) instead of NumberFormat.**\[icu\]**Returns a scientific format for the specified locale.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------|
| [NumberFormat](../android/icu/text/NumberFormat.md)! | a scientific number format |

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

- [#setGroupingUsed](../android/icu/text/NumberFormat.md)) 

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

- [#setParseStrict](../android/icu/text/NumberFormat.md)) 

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

For more detail on parsing, see the "Parsing" header in the class documentation of [DecimalFormat](../android/icu/text/DecimalFormat.md). 
**See Also**

- [#isParseIntegerOnly](../android/icu/text/NumberFormat.md))
- [android.icu.text.DecimalFormat#setParseBigDecimal](../android/icu/text/DecimalFormat.md))
- [java.text.Format#parseObject(String, ParsePosition)](../java/text/Format.md)) 

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
| `pos` | [ParsePosition](../java/text/ParsePosition.md)!:input-output position; on input, the position within text to match; must have 0 \<= pos.getIndex() \< text.length(); on output, the position after the last matched character. If the parse fails, the position in unchanged upon output. |

| Return ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------|
| [CurrencyAmount](../android/icu/util/CurrencyAmount.md)! | a CurrencyAmount, or null upon failure |

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
| `parsePosition` | [ParsePosition](../java/text/ParsePosition.md)!:the position at which to start the parse |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the parsed number, or null |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |

**See Also**

- [java.text.NumberFormat#parseObject(String, ParsePosition)](../java/text/NumberFormat.md)) 

### setContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: DisplayContext!): Unit
```

**\[icu\]**Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [DisplayContext](../android/icu/text/DisplayContext.md)!:The DisplayContext value to set. |

### setCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrency(theCurrency: Currency!): Unit
```

Sets the Currency object used to display currency amounts. This takes effect immediately, if this format is a currency format. If this format is not a currency format, then the currency object is used if and when this object becomes a currency format.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theCurrency` | [Currency](../android/icu/util/Currency.md)!:new currency object to use. May be null for some subclasses. |

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

- [#isGroupingUsed](../android/icu/text/NumberFormat.md)) 

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

- [#getMaximumFractionDigits](../android/icu/text/NumberFormat.md)) 

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

- [#getMaximumIntegerDigits](../android/icu/text/NumberFormat.md)) 

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

- [#getMinimumFractionDigits](../android/icu/text/NumberFormat.md)) 

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

- [#getMinimumIntegerDigits](../android/icu/text/NumberFormat.md)) 

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

- [#isParseIntegerOnly](../android/icu/text/NumberFormat.md)) 

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

- [#isParseStrict](../android/icu/text/NumberFormat.md)) 

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
| `forLocale` | [ULocale](../android/icu/util/ULocale.md)!:the locale of the data. |
| `choice` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the pattern format. |

| Return ||
|-----------------------------------------------------------------------------------|-------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern |
