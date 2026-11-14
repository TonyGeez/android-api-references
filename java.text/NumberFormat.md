# NumberFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberFormat

```
abstract class NumberFormat : Format
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format) ||
| | ↳ | [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) |

| Known Direct Subclasses [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat), [DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat) | A`ChoiceFormat`allows you to attach a format to a range of numbers. | | [DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat) | is a concrete subclass of`NumberFormat`that formats decimal numbers. | |

`NumberFormat`is the abstract base class for all number formats. This class provides the interface for formatting and parsing numbers.`NumberFormat`also provides methods for determining which locales have number formats, and what their names are.

`NumberFormat`helps you to format and parse numbers for any locale. Your code can be completely independent of the locale conventions for decimal points, thousands-separators, or even the particular decimal digits used, or whether the number format is even decimal.

To format a number for the current Locale, use one of the factory class methods: 

```kotlin
<code>myString = NumberFormat.getInstance().format(myNumber);
  </code>
```
If you are formatting multiple numbers, it is more efficient to get the format and use it multiple times so that the system doesn't have to fetch the information about the local language and country conventions multiple times. 

```kotlin
<code>NumberFormat nf = NumberFormat.getInstance();
  for (int i = 0; i &lt; myNumber.length; ++i) {
      output.println(nf.format(myNumber[i]) + "; ");
  }
  </code>
```
To format a number for a different Locale, specify it in the call to`getInstance`. 

```kotlin
<code>NumberFormat nf = NumberFormat.getInstance(Locale.FRENCH);
  </code>
```

If the locale contains "nu" (numbers) [Unicode extensions](https://developer.android.com/reference/kotlin/java/util/Locale.html#def_locale_extension), the decimal digits, and/or the country used for formatting are overridden.

You can also use a`NumberFormat`to parse numbers: 

```kotlin
<code>myNumber = nf.parse(myString);
  </code>
```
Use`getInstance`or`getNumberInstance`to get the normal number format. Use`getIntegerInstance`to get an integer number format. Use`getCurrencyInstance`to get the currency number format. Use`getCompactNumberInstance`to get the compact number format to format a number in shorter form. For example,`2000`can be formatted as`"2K"`in [US locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#US:java.util.Locale). Use`getPercentInstance`to get a format for displaying percentages. With this format, a fraction like 0.53 is displayed as 53%.

You can also control the display of numbers with such methods as`setMinimumFractionDigits`. If you want even more control over the format or parsing, or want to give your users more control, you can try casting the`NumberFormat`you get from the factory methods to a`DecimalFormat`or`CompactNumberFormat`depending on the factory method used. This will work for the vast majority of locales; just remember to put it in a`try`block in case you encounter an unusual one.

NumberFormat and DecimalFormat are designed such that some controls work for formatting and others work for parsing. The following is the detailed description for each these control methods,

setParseIntegerOnly : only affects parsing, e.g. if true, "3456.78" → 3456 (and leaves the parse position just after index 6) if false, "3456.78" → 3456.78 (and leaves the parse position just after index 8) This is independent of formatting. If you want to not show a decimal point where there might be no digits after the decimal point, use setDecimalSeparatorAlwaysShown.

setDecimalSeparatorAlwaysShown : only affects formatting, and only where there might be no digits after the decimal point, such as with a pattern like "#,##0.##", e.g., if true, 3456.00 → "3,456." if false, 3456.00 → "3456" This is independent of parsing. If you want parsing to stop at the decimal point, use setParseIntegerOnly.

You can also use forms of the`parse`and`format`methods with`ParsePosition`and`FieldPosition`to allow you to:

- progressively parse through pieces of a string
- align the decimal point and other areas

For example, you can align numbers in two ways:

1. If you are using a monospaced font with spacing for alignment, you can pass the`FieldPosition`in your format call, with`field`=`INTEGER_FIELD`. On output,`getEndIndex`will be set to the offset between the last character of the integer and the decimal. Add (desiredSpaceCount - getEndIndex) spaces at the front of the string.
2. If you are using proportional fonts, instead of padding with spaces, measure the width of the string in pixels from the start to`getEndIndex`. Then move the pen by (desiredPixelWidth - widthToAlignmentPoint) before drawing the text. It also works where there is no decimal, but possibly additional characters at the end, e.g., with parentheses in negative numbers: "(12)" for -12.

## Synchronization

Number formats are generally not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Field](https://developer.android.com/reference/kotlin/java/text/NumberFormat.Field) Defines constants that are used as attribute keys in the`AttributedCharacterIterator`returned from`NumberFormat.formatToCharacterIterator`and as field identifiers in`FieldPosition`. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTION_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#FRACTION_FIELD:kotlin.Int) Field constant used to construct a FieldPosition object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int) Field constant used to construct a FieldPosition object. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#NumberFormat())`()` Sole constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/NumberFormat#clone())`()` Overrides Cloneable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/NumberFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Double))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Specialization of format. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Specialization of format. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Formats a number and appends the resulting text to the given string buffer. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Long))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Specialization of format. |
| abstract [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Specialization of format. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\> | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getAvailableLocales())`()` Returns a scientific format for the current default locale. |
| open [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)? | [getCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrency())`()` Gets the currency used by this number format when formatting currency values. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getCurrencyInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance())`()` Returns a currency format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getCurrencyInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Returns a currency format for the specified locale. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getInstance())`()` Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Returns a general-purpose number format for the specified locale. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getIntegerInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance())`()` Returns an integer number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getIntegerInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Returns an integer number format for the specified locale. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumFractionDigits())`()` Returns the maximum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumIntegerDigits())`()` Returns the maximum number of digits allowed in the integer portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumFractionDigits())`()` Returns the minimum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumIntegerDigits())`()` Returns the minimum number of digits allowed in the integer portion of a number. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getNumberInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance())`()` Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getNumberInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Returns a general-purpose number format for the specified locale. |
| static [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getPercentInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance())`()` Returns a percentage format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| openstatic [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | [getPercentInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` Returns a percentage format for the specified locale. |
| open [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) | [getRoundingMode](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getRoundingMode())`()` Gets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/NumberFormat#hashCode())`()` Overrides hashCode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isGroupingUsed())`()` Returns true if grouping is used in this format. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())`()` Returns true if this format will parse numbers as integers only. |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Parses text from the beginning of the given string to produce a number. |
| abstract [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `parsePosition:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals), otherwise a Double. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [parseObject](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` Parses text from a string to produce a`Number`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setCurrency(java.util.Currency))`(`currency:` ` [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)`)` Sets the currency used by this number format when formatting currency values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setGroupingUsed(kotlin.Boolean))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether or not grouping will be used in this format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setParseIntegerOnly(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not numbers should be parsed as integers only. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoundingMode](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setRoundingMode(java.math.RoundingMode))`(`roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)?`)` Sets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. |

| Inherited functions ||
|---|---|
| From class [Format](https://developer.android.com/reference/kotlin/java/text/Format) |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/Format#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

## Constants

### FRACTION_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRACTION_FIELD: Int
```

Field constant used to construct a FieldPosition object. Signifies that the position of the fraction part of a formatted number should be returned. 

 Value: 1

**See Also**

- [java.text.FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition) 

### INTEGER_FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTEGER_FIELD: Int
```

Field constant used to construct a FieldPosition object. Signifies that the position of the integer part of a formatted number should be returned. 

 Value: 0

**See Also**

- [java.text.FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)

## Protected constructors

### NumberFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected NumberFormat()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides Cloneable.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Overrides equals.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Double): String
```

Specialization of format.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the double number to format |

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the formatted String |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

**See Also**

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: Double, 
    toAppendTo: StringBuffer, 
    pos: FieldPosition
): StringBuffer
```

Specialization of format.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the double number to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):the StringBuffer to which the formatted text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition):keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the formatted StringBuffer |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

**See Also**

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Any, 
    toAppendTo: StringBuffer, 
    pos: FieldPosition
): StringBuffer
```

Formats a number and appends the resulting text to the given string buffer. The number can be of any subclass of [java.lang.Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#).

This implementation extracts the number's value using [java.lang.Number#longValue()](https://developer.android.com/reference/kotlin/java/lang/Number.html#longValue())for all integral type values that can be converted to`long`without loss of information, including`BigInteger`values with a [bit length](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#bitLength())of less than 64, and [java.lang.Number#doubleValue()](https://developer.android.com/reference/kotlin/java/lang/Number.html#doubleValue())for all other types. It then calls [format(long,java.lang.StringBuffer,java.text.FieldPosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition))or [format(double,java.lang.StringBuffer,java.text.FieldPosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition)). This may result in loss of magnitude information and precision for`BigInteger`and`BigDecimal`values.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):the`StringBuffer`to which the formatted text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition):keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |
| `number` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the number to format |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the value passed in as`toAppendTo` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if`number`is null or not an instance of`Number`. |
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

**See Also**

- [java.text.FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition) 

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(number: Long): String
```

Specialization of format.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------|
| `number` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the long number to format |

| Return ||
|----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the formatted String |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

**See Also**

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun format(
    number: Long, 
    toAppendTo: StringBuffer, 
    pos: FieldPosition
): StringBuffer
```

Specialization of format.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the long number to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):the StringBuffer to which the formatted text is to be appended |
| `pos` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition):keeps track on the position of the field within the returned string. For example, for formatting a number`123456789`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 11, respectively for the output string`123,456,789`. |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the formatted StringBuffer |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

**See Also**

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>
```

Returns a scientific format for the current default locale. /\*public\* static final NumberFormat getScientificInstance() { return getInstance(Locale.getDefault(Locale.Category.FORMAT), null, SCIENTIFICSTYLE); } /\*\* Returns a scientific format for the specified locale.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `inLocale` | the desired locale /\*public\* static NumberFormat getScientificInstance(Locale inLocale) { return getInstance(inLocale, null, SCIENTIFICSTYLE); } |

### getCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency?
```

Gets the currency used by this number format when formatting currency values. The initial value is derived in a locale dependent way. The returned value may be null if no valid currency could be determined and no currency has been set using [setCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setCurrency(java.util.Currency)).

The default implementation throws`UnsupportedOperationException`.

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)? | the currency used by this number format, or`null` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the number format class doesn't implement currency formatting |

### getCurrencyInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCurrencyInstance(): NumberFormat
```

Returns a currency format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.

This is equivalent to calling [getCurrencyInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance(java.util.Locale)).

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for currency formatting |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))
- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### getCurrencyInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCurrencyInstance(inLocale: Locale): NumberFormat
```

Returns a currency format for the specified locale.

If the specified locale contains the "`cf`" ([currency format style](https://www.unicode.org/reports/tr35/tr35.html#UnicodeCurrencyFormatIdentifier)) [Unicode extension](https://developer.android.com/reference/kotlin/java/util/Locale.html#def_locale_extension), the returned currency format uses the style if it is available. Otherwise, the style uses the default "`standard`" currency format. For example, if the style designates "`account`", negative currency amounts use a pair of parentheses in some locales.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):the desired locale |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for currency formatting |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(): NumberFormat
```

Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is the same as calling [getNumberInstance()](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance()).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for general-purpose number formatting |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(inLocale: Locale): NumberFormat
```

Returns a general-purpose number format for the specified locale. This is the same as calling [getNumberInstance(inLocale)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):the desired locale |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for general-purpose number formatting |

### getIntegerInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getIntegerInstance(): NumberFormat
```

Returns an integer number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())).

This is equivalent to calling [getIntegerInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance(java.util.Locale)).

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | a number format for integer values |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/NumberFormat#getRoundingMode()>
- [java.util.Locale#getDefault(java.util.Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))
- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### getIntegerInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getIntegerInstance(inLocale: Locale): NumberFormat
```

Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):the desired locale |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | a number format for integer values |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/NumberFormat#getRoundingMode()> 

### getMaximumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumFractionDigits(): Int
```

Returns the maximum number of digits allowed in the fraction portion of a number.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of digits. |

**See Also**

- [#setMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumFractionDigits(kotlin.Int)) 

### getMaximumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumIntegerDigits(): Int
```

Returns the maximum number of digits allowed in the integer portion of a number.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of digits |

**See Also**

- [#setMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumIntegerDigits(kotlin.Int)) 

### getMinimumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumFractionDigits(): Int
```

Returns the minimum number of digits allowed in the fraction portion of a number.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of digits |

**See Also**

- [#setMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumFractionDigits(kotlin.Int)) 

### getMinimumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumIntegerDigits(): Int
```

Returns the minimum number of digits allowed in the integer portion of a number.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of digits |

**See Also**

- [#setMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumIntegerDigits(kotlin.Int)) 

### getNumberInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getNumberInstance(): NumberFormat
```

Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.

This is equivalent to calling [getNumberInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale)).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for general-purpose number formatting |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))
- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### getNumberInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getNumberInstance(inLocale: Locale): NumberFormat
```

Returns a general-purpose number format for the specified locale.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):the desired locale |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for general-purpose number formatting |

### getPercentInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getPercentInstance(): NumberFormat
```

Returns a percentage format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.

This is equivalent to calling [getPercentInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance(java.util.Locale)).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for percentage formatting |

**See Also**

- [java.util.Locale#getDefault(java.util.Locale.Category)](https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category))
- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### getPercentInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPercentInstance(inLocale: Locale): NumberFormat
```

Returns a percentage format for the specified locale.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#):the desired locale |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------|
| [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat#) | the`NumberFormat`instance for percentage formatting |

### getRoundingMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundingMode(): RoundingMode
```

Gets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. The default implementation of this method in NumberFormat always throws [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Subclasses which handle different rounding modes should override this method.

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) | The`RoundingMode`used for this NumberFormat. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | The default implementation always throws this exception |

**See Also**

- [#setRoundingMode(RoundingMode)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setRoundingMode(java.math.RoundingMode)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Overrides hashCode.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isGroupingUsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isGroupingUsed(): Boolean
```

Returns true if grouping is used in this format. For example, in the English locale, with grouping on, the number 1234567 might be formatted as "1,234,567". The grouping separator as well as the size of each group is locale dependent and is determined by sub-classes of NumberFormat.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if grouping is used;`false`otherwise |

**See Also**

- [#setGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setGroupingUsed(kotlin.Boolean)) 

### isParseIntegerOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isParseIntegerOnly(): Boolean
```

Returns true if this format will parse numbers as integers only. For example in the English locale, with ParseIntegerOnly true, the string "1234." would be parsed as the integer value 1234 and parsing would stop at the "." character. Of course, the exact format accepted by the parse operation is locale dependent and determined by sub-classes of NumberFormat.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if numbers should be parsed as integers only;`false`otherwise |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(source: String): Number?
```

Parses text from the beginning of the given string to produce a number. The method may not use the entire text of the given string.

See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on number parsing.

**WARNING:** Don't use this method to deserialize a number. The underlying localized number format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using the parse methods in the boxed types, e.g. [Long.parseLong(String)](https://developer.android.com/reference/kotlin/java/lang/Long.html#parseLong(kotlin.String)), or [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#) for deserializing a locale-independent decimal number.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A`String`whose beginning should be parsed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | A`Number`parsed from the string. |

| Exceptions ||
|----------------------------|------------------------------------------------------------|
| `java.text.ParseException` | if the beginning of the specified string cannot be parsed. |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun parse(
    source: String, 
    parsePosition: ParsePosition
): Number?
```

Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals), otherwise a Double. If IntegerOnly is set, will stop at a decimal point (or equivalent; e.g., for rational numbers "1 2/3", will stop after the 1). Does not throw an exception; if no object can be parsed, index is unchanged!

**WARNING:** Don't use this method to deserialize a number. The underlying localized number format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using the parse methods in the boxed types, e.g. [Long.parseLong(String)](https://developer.android.com/reference/kotlin/java/lang/Long.html#parseLong(kotlin.String)), or [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#) for deserializing a locale-independent decimal number.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the String to parse |
| `parsePosition` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition):the parse position |

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | the parsed value |

**See Also**

- [java.text.NumberFormat#isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly()) 

### parseObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parseObject(
    source: String, 
    pos: ParsePosition
): Any?
```

Parses text from a string to produce a`Number`.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed number is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on number parsing.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):A`String`, part of which should be parsed. |
| `pos` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition):A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | A`Number`parsed from the string. In case of error, returns null. |

| Exceptions ||
|----------------------------------|---------------------------|
| `java.lang.NullPointerException` | if`source`or`pos`is null. |

### setCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrency(currency: Currency): Unit
```

Sets the currency used by this number format when formatting currency values. This does not update the minimum or maximum number of fraction digits used by the number format.

The default implementation throws`UnsupportedOperationException`.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `currency` | [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#):the new currency to be used by this number format |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the number format class doesn't implement currency formatting |
| `java.lang.NullPointerException` | if`currency`is null |

### setGroupingUsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingUsed(newValue: Boolean): Unit
```

Set whether or not grouping will be used in this format.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if grouping is used;`false`otherwise |

**See Also**

- [#isGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isGroupingUsed()) 

### setMaximumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumFractionDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the fraction portion of a number. maximumFractionDigits must be ≥ minimumFractionDigits. If the new value for maximumFractionDigits is less than the current value of minimumFractionDigits, then minimumFractionDigits will also be set to the new value.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumFractionDigits()) 

### setMaximumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumIntegerDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the integer portion of a number. maximumIntegerDigits must be ≥ minimumIntegerDigits. If the new value for maximumIntegerDigits is less than the current value of minimumIntegerDigits, then minimumIntegerDigits will also be set to the new value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of integer digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumIntegerDigits()) 

### setMinimumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumFractionDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the fraction portion of a number. minimumFractionDigits must be ≤ maximumFractionDigits. If the new value for minimumFractionDigits exceeds the current value of maximumFractionDigits, then maximumFractionDigits will also be set to the new value

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumFractionDigits()) 

### setMinimumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumIntegerDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the integer portion of a number. minimumIntegerDigits must be ≤ maximumIntegerDigits. If the new value for minimumIntegerDigits exceeds the current value of maximumIntegerDigits, then maximumIntegerDigits will also be set to the new value

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of integer digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [#getMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumIntegerDigits()) 

### setParseIntegerOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParseIntegerOnly(value: Boolean): Unit
```

Sets whether or not numbers should be parsed as integers only.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if numbers should be parsed as integers only;`false`otherwise |

**See Also**

- [#isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly()) 

### setRoundingMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRoundingMode(roundingMode: RoundingMode?): Unit
```

Sets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. The default implementation of this method in NumberFormat always throws [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Subclasses which handle different rounding modes should override this method.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `roundingMode` | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)?:The`RoundingMode`to be used |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | The default implementation always throws this exception |
| `java.lang.NullPointerException` | if`roundingMode`is null |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/NumberFormat#getRoundingMode()>
