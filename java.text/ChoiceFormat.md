# ChoiceFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ChoiceFormat

```
open class ChoiceFormat : NumberFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format) |||
| | ↳ | [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) ||
| | | ↳ | [java.text.ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#) |
| --- | --- | --- | --- |

A`ChoiceFormat`allows you to attach a format to a range of numbers. It is generally used in a`MessageFormat`for handling plurals. The choice is specified with an ascending list of doubles, where each item specifies a half-open interval up to the next item: 

```kotlin
X matches j if and only if limit[j] ≤ X < limit[j+1]
  
```
If there is no match, then either the first or last index is used, depending on whether the number (X) is too low or too high. If the limit array is not in ascending order, the results of formatting will be incorrect. ChoiceFormat also accepts`\u221E`as equivalent to infinity(INF).

<br />

**Note:** `ChoiceFormat`differs from the other`Format`classes in that you create a`ChoiceFormat`object with a constructor (not with a`getInstance`style factory method). The factory methods aren't necessary because`ChoiceFormat`doesn't require any complex setup for a given locale. In fact,`ChoiceFormat`doesn't implement any locale specific behavior.

When creating a`ChoiceFormat`, you must specify an array of formats and an array of limits. The length of these arrays must be the same. For example,

- *limits* = {1,2,3,4,5,6,7} 
 *formats*= {"Sun","Mon","Tue","Wed","Thur","Fri","Sat"}
- *limits* = {0, 1, ChoiceFormat.nextDouble(1)} 
 *formats* = {"no files", "one file", "many files"} 
 (`nextDouble`can be used to get the next higher double, to make the half-open interval.)

Here is a simple example that shows formatting and parsing: 

```kotlin
<code>double[] limits = {1,2,3,4,5,6,7};
  String[] dayOfWeekNames = {"Sun","Mon","Tue","Wed","Thur","Fri","Sat"};
  ChoiceFormat form = new ChoiceFormat(limits, dayOfWeekNames);
  ParsePosition status = new ParsePosition(0);
  for (double i = 0.0; i &lt;= 8.0; ++i) {
      status.setIndex(0);
      System.out.println(i + " -&gt; " + form.format(i) + " -&gt; "
                               + form.parse(form.format(i),status));
  }
  </code>
```
Here is a more complex example, with a pattern format: 

```kotlin
<code>double[] filelimits = {0,1,2};
  String[] filepart = {"are no files","is one file","are {2} files"};
  ChoiceFormat fileform = new ChoiceFormat(filelimits, filepart);
  Format[] testFormats = {fileform, null, NumberFormat.getInstance()};
  MessageFormat pattform = new MessageFormat("There {0} on {1}");
  pattform.setFormats(testFormats);
  Object[] testArgs = {null, "ADisk", null};
  for (int i = 0; i &lt; 4; ++i) {
      testArgs[0] = new Integer(i);
      testArgs[2] = testArgs[0];
      System.out.println(pattform.format(testArgs));
  }
  </code>
```

Specifying a pattern for ChoiceFormat objects is fairly straightforward. For example: 

```kotlin
<code>ChoiceFormat fmt = new ChoiceFormat(
       "-1#is negative| 0#is zero or fraction | 1#is one |1.0&lt;is 1+ |2#is two |2&lt;is more than 2.");
  System.out.println("Formatter Pattern : " + fmt.toPattern());
 
  System.out.println("Format with -INF : " + fmt.format(Double.NEGATIVE_INFINITY));
  System.out.println("Format with -1.0 : " + fmt.format(-1.0));
  System.out.println("Format with 0 : " + fmt.format(0));
  System.out.println("Format with 0.9 : " + fmt.format(0.9));
  System.out.println("Format with 1.0 : " + fmt.format(1));
  System.out.println("Format with 1.5 : " + fmt.format(1.5));
  System.out.println("Format with 2 : " + fmt.format(2));
  System.out.println("Format with 2.1 : " + fmt.format(2.1));
  System.out.println("Format with NaN : " + fmt.format(Double.NaN));
  System.out.println("Format with +INF : " + fmt.format(Double.POSITIVE_INFINITY));
  </code>
```
And the output result would be like the following: 

```kotlin
<code>Format with -INF : is negative
  Format with -1.0 : is negative
  Format with 0 : is zero or fraction
  Format with 0.9 : is zero or fraction
  Format with 1.0 : is one
  Format with 1.5 : is 1+
  Format with 2 : is two
  Format with 2.1 : is more than 2.
  Format with NaN : is negative
  Format with +INF : is more than 2.
  </code>
```

## Synchronization

Choice formats are not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

## Summary

| Inherited constants ||
|---|---|
| From class [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTION_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#FRACTION_FIELD:kotlin.Int) <br /> Field constant used to construct a FieldPosition object. Signifies that the position of the fraction part of a formatted number should be returned. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int) <br /> Field constant used to construct a FieldPosition object. Signifies that the position of the integer part of a formatted number should be returned. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#ChoiceFormat(kotlin.DoubleArray,%20kotlin.Array))`(`limits:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `formats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Constructs with the limits and the corresponding formats. |
| [ChoiceFormat](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#ChoiceFormat(kotlin.String))`(`newPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs with limits and corresponding formats based on the pattern. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#applyPattern(kotlin.String))`(`newPattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the pattern. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#clone())`()` Overrides Cloneable |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Equality comparison between two |
| --- | --- |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `status:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Returns pattern with formatted double. |
| open [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `status:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` Specialization of format. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getFormats](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#getFormats())`()` <br /> |
| --- | --- |
| open [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | [getLimits](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#getLimits())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#hashCode())`()` Generates a hash code for the message format object. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#nextDouble(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Finds the least double greater than`d`. |
| --- | --- |
| openstatic [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [nextDouble](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#nextDouble(kotlin.Double,%20kotlin.Boolean))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `positive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Finds the least double greater than`d`(if`positive`is`true`), or the greatest double less than`d`(if`positive`is`false`). |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#parse(kotlin.String,%20java.text.ParsePosition))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `status:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` Parses a Number from the input text. |
| static [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [previousDouble](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#previousDouble(kotlin.Double))`(`d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Finds the greatest double less than`d`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChoices](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#setChoices(kotlin.DoubleArray,%20kotlin.Array))`(`limits:` ` [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!`, `formats:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Set the choices to be used in formatting. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#toPattern())`()` Gets the pattern. |

| Inherited functions ||
|---|---|
| From class [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) |------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Double))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Specialization of format. <br /> | | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `toAppendTo:` ` [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#)`, `pos:` ` [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition)`)` <br /> Formats a number and appends the resulting text to the given string buffer. The number can be of any subclass of [java.lang.Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#). This implementation extracts the number's value using [java.lang.Number#longValue()](https://developer.android.com/reference/kotlin/java/lang/Number.html#longValue())for all integral type values that can be converted to`long`without loss of information, including`BigInteger`values with a [bit length](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#bitLength())of less than 64, and [java.lang.Number#doubleValue()](https://developer.android.com/reference/kotlin/java/lang/Number.html#doubleValue())for all other types. It then calls [format(long,java.lang.StringBuffer,java.text.FieldPosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition))or [format(double,java.lang.StringBuffer,java.text.FieldPosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition)). This may result in loss of magnitude information and precision for`BigInteger`and`BigDecimal`values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](https://developer.android.com/reference/kotlin/java/text/NumberFormat#format(kotlin.Long))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Specialization of format. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!> | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getAvailableLocales())`()` <br /> Returns a scientific format for the current default locale. /\*public\* static final NumberFormat getScientificInstance() { return getInstance(Locale.getDefault(Locale.Category.FORMAT), null, SCIENTIFICSTYLE); } /\*\* Returns a scientific format for the specified locale. <br /> | | [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)? | [getCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrency())`()` <br /> Gets the currency used by this number format when formatting currency values. The initial value is derived in a locale dependent way. The returned value may be null if no valid currency could be determined and no currency has been set using [setCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setCurrency(java.util.Currency)). The default implementation throws`UnsupportedOperationException`. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getCurrencyInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance())`()` <br /> Returns a currency format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getCurrencyInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance(java.util.Locale)). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getCurrencyInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getCurrencyInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Returns a currency format for the specified locale. If the specified locale contains the "`cf`" ([currency format style](https://www.unicode.org/reports/tr35/tr35.html#UnicodeCurrencyFormatIdentifier)) [Unicode extension](https://developer.android.com/reference/kotlin/java/util/Locale.html#def_locale_extension), the returned currency format uses the style if it is available. Otherwise, the style uses the default "`standard`" currency format. For example, if the style designates "`account`", negative currency amounts use a pair of parentheses in some locales. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getInstance())`()` <br /> Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is the same as calling [getNumberInstance()](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance()). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Returns a general-purpose number format for the specified locale. This is the same as calling [getNumberInstance(inLocale)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale)). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getIntegerInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance())`()` <br /> Returns an integer number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())). This is equivalent to calling [getIntegerInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance(java.util.Locale)). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getIntegerInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getIntegerInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumFractionDigits())`()` <br /> Returns the maximum number of digits allowed in the fraction portion of a number. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMaximumIntegerDigits())`()` <br /> Returns the maximum number of digits allowed in the integer portion of a number. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumFractionDigits())`()` <br /> Returns the minimum number of digits allowed in the fraction portion of a number. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getMinimumIntegerDigits())`()` <br /> Returns the minimum number of digits allowed in the integer portion of a number. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getNumberInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance())`()` <br /> Returns a general-purpose number format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getNumberInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale)). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getNumberInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getNumberInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Returns a general-purpose number format for the specified locale. <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getPercentInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance())`()` <br /> Returns a percentage format for the current default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. This is equivalent to calling [getPercentInstance(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance(java.util.Locale)). <br /> | | [NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat) | [getPercentInstance](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getPercentInstance(java.util.Locale))`(`inLocale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)`)` <br /> Returns a percentage format for the specified locale. <br /> | | [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) | [getRoundingMode](https://developer.android.com/reference/kotlin/java/text/NumberFormat#getRoundingMode())`()` <br /> Gets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. The default implementation of this method in NumberFormat always throws [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Subclasses which handle different rounding modes should override this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isGroupingUsed())`()` <br /> Returns true if grouping is used in this format. For example, in the English locale, with grouping on, the number 1234567 might be formatted as "1,234,567". The grouping separator as well as the size of each group is locale dependent and is determined by sub-classes of NumberFormat. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#isParseIntegerOnly())`()` <br /> Returns true if this format will parse numbers as integers only. For example in the English locale, with ParseIntegerOnly true, the string "1234." would be parsed as the integer value 1234 and parsing would stop at the "." character. Of course, the exact format accepted by the parse operation is locale dependent and determined by sub-classes of NumberFormat. <br /> | | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Parses text from the beginning of the given string to produce a number. The method may not use the entire text of the given string. See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on number parsing. **WARNING:** Don't use this method to deserialize a number. The underlying localized number format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using the parse methods in the boxed types, e.g. [Long.parseLong(String)](https://developer.android.com/reference/kotlin/java/lang/Long.html#parseLong(kotlin.String)), or [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#) for deserializing a locale-independent decimal number. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [parseObject](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parseObject(kotlin.String,%20java.text.ParsePosition))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition)`)` <br /> Parses text from a string to produce a`Number`. The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed number is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned. See the [parse(java.lang.String,java.text.ParsePosition)](https://developer.android.com/reference/kotlin/java/text/NumberFormat#parse(kotlin.String,%20java.text.ParsePosition))method for more information on number parsing. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setCurrency(java.util.Currency))`(`currency:` ` [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)`)` <br /> Sets the currency used by this number format when formatting currency values. This does not update the minimum or maximum number of fraction digits used by the number format. The default implementation throws`UnsupportedOperationException`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingUsed](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setGroupingUsed(kotlin.Boolean))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set whether or not grouping will be used in this format. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the maximum number of digits allowed in the fraction portion of a number. maximumFractionDigits must be ≥ minimumFractionDigits. If the new value for maximumFractionDigits is less than the current value of minimumFractionDigits, then minimumFractionDigits will also be set to the new value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMaximumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the maximum number of digits allowed in the integer portion of a number. maximumIntegerDigits must be ≥ minimumIntegerDigits. If the new value for maximumIntegerDigits is less than the current value of minimumIntegerDigits, then minimumIntegerDigits will also be set to the new value. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFractionDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumFractionDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the minimum number of digits allowed in the fraction portion of a number. minimumFractionDigits must be ≤ maximumFractionDigits. If the new value for minimumFractionDigits exceeds the current value of maximumFractionDigits, then maximumFractionDigits will also be set to the new value <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumIntegerDigits](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setMinimumIntegerDigits(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the minimum number of digits allowed in the integer portion of a number. minimumIntegerDigits must be ≤ maximumIntegerDigits. If the new value for minimumIntegerDigits exceeds the current value of maximumIntegerDigits, then maximumIntegerDigits will also be set to the new value <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseIntegerOnly](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setParseIntegerOnly(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether or not numbers should be parsed as integers only. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoundingMode](https://developer.android.com/reference/kotlin/java/text/NumberFormat#setRoundingMode(java.math.RoundingMode))`(`roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)?`)` <br /> Sets the [java.math.RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#) used in this NumberFormat. The default implementation of this method in NumberFormat always throws [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#). Subclasses which handle different rounding modes should override this method. <br /> | ||
| From class [Format](https://developer.android.com/reference/kotlin/java/text/Format) |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](https://developer.android.com/reference/kotlin/java/text/Format#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator)! | [formatToCharacterIterator](https://developer.android.com/reference/kotlin/java/text/Format#formatToCharacterIterator(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](https://developer.android.com/reference/kotlin/java/text/Format#parseObject(kotlin.String))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

## Public constructors

### ChoiceFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ChoiceFormat(
    limits: DoubleArray!, 
    formats: Array<String!>!)
```

Constructs with the limits and the corresponding formats.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `limits` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!:limits in ascending order |
| `formats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:corresponding format strings |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if`limits`or`formats`is`null` |

**See Also**

- [#setChoices](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#setChoices(kotlin.DoubleArray,%20kotlin.Array)) 

### ChoiceFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ChoiceFormat(newPattern: String!)
```

Constructs with limits and corresponding formats based on the pattern.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------|
| `newPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new pattern string |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`newPattern`is`null` |

**See Also**

- [#applyPattern](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#applyPattern(kotlin.String))

## Public methods

### applyPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(newPattern: String!): Unit
```

Sets the pattern.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `newPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:See the class description. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`newPattern`is`null` |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Overrides Cloneable

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

Equality comparison between two

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Double, 
    toAppendTo: StringBuffer, 
    status: FieldPosition
): StringBuffer
```

Returns pattern with formatted double.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):number to be formatted and substituted. |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):where text is appended. |
| `pos` | keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |
| --- | --- |
| `status` | [FieldPosition](https://developer.android.com/reference/kotlin/java/text/FieldPosition):ignore no useful status is returned. |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the formatted StringBuffer |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |
| `java.lang.NullPointerException` | if`toAppendTo`is`null` |

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Long, 
    toAppendTo: StringBuffer, 
    status: FieldPosition
): StringBuffer
```

Specialization of format. This method really calls`format(double, StringBuffer, FieldPosition)`thus the range of longs that are supported is only equal to the range that can be stored by double. This will never be a practical limitation.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the long number to format |
| `toAppendTo` | [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#):the StringBuffer to which the formatted text is to be appended |
| `pos` | keeps track on the position of the field within the returned string. For example, for formatting a number`123456789`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](https://developer.android.com/reference/kotlin/java/text/NumberFormat#INTEGER_FIELD:kotlin.Int), the begin index and end index of`fieldPosition`will be set to 0 and 11, respectively for the output string`123,456,789`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------------------|----------------------------|
| [StringBuffer](https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#) | the formatted StringBuffer |

| Exceptions ||
|---------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |

### getFormats

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFormats(): Array<Any!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a copy of the`String[]`array supplied to the constructor or the most recent call to[setChoices(double[],java.lang.String[])](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#setChoices(kotlin.DoubleArray,%20kotlin.Array)). |

### getLimits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLimits(): DoubleArray!
```

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)! | a copy of the`double[]`array supplied to the constructor or the most recent call to[setChoices(double[],java.lang.String[])](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#setChoices(kotlin.DoubleArray,%20kotlin.Array)). |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Generates a hash code for the message format object.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### nextDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun nextDouble(d: Double): Double
```

Finds the least double greater than`d`. If`NaN`, returns same value.

Used to make half-open intervals.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the reference value |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the least double value greather than`d` |

**See Also**

- [#previousDouble](https://developer.android.com/reference/kotlin/java/text/ChoiceFormat#previousDouble(kotlin.Double)) 

### nextDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun nextDouble(
    d: Double, 
    positive: Boolean
): Double
```

Finds the least double greater than`d`(if`positive`is`true`), or the greatest double less than`d`(if`positive`is`false`). If`NaN`, returns same value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the reference value |
| `positive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the least double is desired;`false`otherwise |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the least or greater double value |

### parse

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun parse(
    text: String, 
    status: ParsePosition
): Number?
```

Parses a Number from the input text.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | the String to parse |
| `parsePosition` | the parse position |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the source text. |
| --- | --- |
| `status` | [ParsePosition](https://developer.android.com/reference/kotlin/java/text/ParsePosition):an input-output parameter. On input, the status.index field indicates the first character of the source text that should be parsed. On exit, if no error occurred, status.index is set to the first unparsed character in the source text. On exit, if an error did occur, status.index is unchanged and status.errorIndex is set to the first index of the character that caused the parse to fail. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | A Number representing the value of the number parsed. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`status`is`null`or if`text`is`null`and the list of choice strings is not empty. |

### previousDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun previousDouble(d: Double): Double
```

Finds the greatest double less than`d`. If`NaN`, returns same value.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the reference value |

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the greatest double value less than`d` |

**See Also**

### setChoices

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setChoices(
    limits: DoubleArray!, 
    formats: Array<String!>!
): Unit
```

Set the choices to be used in formatting.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `limits` | [DoubleArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double-array/index.html)!:contains the top value that you want parsed with that format, and should be in ascending sorted order. When formatting X, the choice will be the i, where limit\[i\] ≤ X \< limit\[i+1\]. If the limit array is not in ascending order, the results of formatting will be incorrect. |
| `formats` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:are the formats you want to use for each limit. They can be either Format objects or Strings. When formatting with object Y, if the object is a NumberFormat, then ((NumberFormat) Y).format(X) is called. Otherwise Y.toString() is called. |

| Exceptions ||
|----------------------------------|-------------------------------|
| `java.lang.NullPointerException` | if`limits`or`formats`is`null` |

### toPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Gets the pattern.

| Return ||
|-----------------------------------------------------------------------------------|--------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the pattern string |
