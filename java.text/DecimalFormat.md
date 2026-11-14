# DecimalFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalFormat

```
open class DecimalFormat : NumberFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.text.Format](Format.md) |||
| | ↳ | [java.text.NumberFormat](NumberFormat.md) ||
| | | ↳ | [java.text.DecimalFormat](DecimalFormat.md) |
| --- | --- | --- | --- |

is a concrete subclass of`NumberFormat`that formats decimal numbers. It has a variety of features designed to make it possible to parse and format numbers in any locale, including support for Western, Arabic, and Indic digits. It also supports different kinds of numbers, including integers (123), fixed-point numbers (123.4), scientific notation (1.23E4), percentages (12%), and currency amounts ($123). All of these can be localized.

To obtain a`NumberFormat`for a specific locale, including the default locale, call one of`NumberFormat`'s factory methods, such as`getInstance()`. In general, do not call the`DecimalFormat`constructors directly, since the`NumberFormat`factory methods may return subclasses other than`DecimalFormat`. If you need to customize the format object, do something like this: 

```kotlin
NumberFormat f = NumberFormat.getInstance(loc);
  if (f instanceof DecimalFormat) {
      ((DecimalFormat) f).setDecimalSeparatorAlwaysShown(true);
  }
  
```

A`DecimalFormat`comprises a*pattern* and a set of*symbols* . The pattern may be set directly using`applyPattern()`, or indirectly using the API methods. The symbols are stored in a`DecimalFormatSymbols`object. When using the`NumberFormat`factory methods, the pattern and symbols are read from localized`ResourceBundle`s.

## Patterns

`DecimalFormat`patterns have the following syntax: 

```kotlin
<i>Pattern:</i><i>PositivePattern</i><i>PositivePattern</i>; <i>NegativePattern</i><i>PositivePattern:</i><i>Prefix<sub>opt</sub></i><i>Number</i><i>Suffix<sub>opt</sub></i><i>NegativePattern:</i><i>Prefix<sub>opt</sub></i><i>Number</i><i>Suffix<sub>opt</sub></i><i>Prefix:</i>any Unicode characters except \uFFFE, \uFFFF, and special characters
  <i>Suffix:</i>any Unicode characters except \uFFFE, \uFFFF, and special characters
  <i>Number:</i><i>Integer</i><i>Exponent<sub>opt</sub></i><i>Integer</i>. <i>Fraction</i><i>Exponent<sub>opt</sub></i><i>Integer:</i><i>MinimumInteger</i>
          # <i>Integer</i> , <i>Integer</i><i>MinimumInteger:</i>0
          0 <i>MinimumInteger</i>0 , <i>MinimumInteger</i><i>Fraction:</i><i>MinimumFraction<sub>opt</sub></i><i>OptionalFraction<sub>opt</sub></i><i>MinimumFraction:</i>0 <i>MinimumFraction<sub>opt</sub></i><i>OptionalFraction:</i> <i>OptionalFraction<sub>opt</sub></i><i>Exponent:</i>E <i>MinimumExponent</i><i>MinimumExponent:</i>0 <i>MinimumExponent<sub>opt</sub></i>
```

A`DecimalFormat`pattern contains a positive and negative subpattern, for example,`"#,##0.00;(#,##0.00)"`. Each subpattern has a prefix, numeric part, and suffix. The negative subpattern is optional; if absent, then the positive subpattern prefixed with the minus sign (`'-' U+002D HYPHEN-MINUS`) is used as the negative subpattern. That is,`"0.00"`alone is equivalent to`"0.00;-0.00"`. If there is an explicit negative subpattern, it serves only to specify the negative prefix and suffix; the number of digits, minimal digits, and other characteristics are all the same as the positive pattern. That means that`"#,##0.0#;(#)"`produces precisely the same behavior as`"#,##0.0#;(#,##0.0#)"`.

The prefixes, suffixes, and various symbols used for infinity, digits, grouping separators, decimal separators, etc. may be set to arbitrary values, and they will appear properly during formatting. However, care must be taken that the symbols and strings do not conflict, or parsing will be unreliable. For example, either the positive and negative prefixes or the suffixes must be distinct for`DecimalFormat.parse()`to be able to distinguish positive from negative values. (If they are identical, then`DecimalFormat`will behave as if no negative subpattern was specified.) Another example is that the decimal separator and grouping separator should be distinct characters, or parsing will be impossible.

The grouping separator is commonly used for thousands, but in some countries it separates ten-thousands. The grouping size is a constant number of digits between the grouping characters, such as 3 for 100,000,000 or 4 for 1,0000,0000. If you supply a pattern with multiple grouping characters, the interval between the last one and the end of the integer is the one that is used. So`"#,##,###,####"`==`"######,####"`==`"##,####,####"`.

### Special Pattern Characters

Many characters in a pattern are taken literally; they are matched during parsing and output unchanged during formatting. Special characters, on the other hand, stand for other characters, strings, or classes of characters. They must be quoted, unless noted otherwise, if they are to appear in the prefix or suffix as literals.

The characters listed here are used in non-localized patterns. Localized patterns use the corresponding characters taken from this formatter's`DecimalFormatSymbols`object instead, and these characters lose their special status. Two exceptions are the currency sign and quote, which are not localized.

| Symbol | Location | Localized? | Meaning |
| --- | --- | --- | --- |
| `0` | Number | Yes | Digit |
| | Number | Yes | Digit, zero shows as absent |
| `.` | Number | Yes | Decimal separator or monetary decimal separator |
| --- | --- | --- | --- |
| `-` | Number | Yes | Minus sign |
| `,` | Number | Yes | Grouping separator or monetary grouping separator |
| `E` | Number | Yes | Separates mantissa and exponent in scientific notation.*Need not be quoted in prefix or suffix.* |
| --- | --- | --- | --- |
| `;` | Subpattern boundary | Yes | Separates positive and negative subpatterns |
| `%` | Prefix or suffix | Yes | Multiply by 100 and show as percentage |
| `&#92;u2030` | Prefix or suffix | Yes | Multiply by 1000 and show as per mille value |
| --- | --- | --- | --- |
| `&#164;`(`&#92;u00A4`) | Prefix or suffix | No | Currency sign, replaced by currency symbol. If doubled, replaced by international currency symbol. If present in a pattern, the monetary decimal/grouping separators are used instead of the decimal/grouping separators. |
| `'` | Prefix or suffix | No | Used to quote special characters in a prefix or suffix, for example,`"'#'#"`formats 123 to`"#123"`. To create a single quote itself, use two in a row:`"# o''clock"`. |
|------------------------|---------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

### Scientific Notation

Numbers in scientific notation are expressed as the product of a mantissa and a power of ten, for example, 1234 can be expressed as 1.234 x 10\^3. The mantissa is often in the range 1.0 ≤ x \< 10.0, but it need not be.`DecimalFormat`can be instructed to format and parse scientific notation*only via a pattern* ; there is currently no factory method that creates a scientific notation format. In a pattern, the exponent character immediately followed by one or more digit characters indicates scientific notation. Example:`"0.###E0"`formats the number 1234 as`"1.234E3"`.

- The number of digit characters after the exponent character gives the minimum exponent digit count. There is no maximum. Negative exponents are formatted using the localized minus sign,*not* the prefix and suffix from the pattern. This allows patterns such as`"0.###E0 m/s"`.
- The minimum and maximum number of integer digits are interpreted together:
 - If the maximum number of integer digits is greater than their minimum number and greater than 1, it forces the exponent to be a multiple of the maximum number of integer digits, and the minimum number of integer digits to be interpreted as 1. The most common use of this is to generate*engineering notation* , in which the exponent is a multiple of three, e.g.,`"##0.#####E0"`. Using this pattern, the number 12345 formats to`"12.345E3"`, and 123456 formats to`"123.456E3"`.
 - Otherwise, the minimum number of integer digits is achieved by adjusting the exponent. Example: 0.00123 formatted with`"00.###E0"`yields`"12.3E-4"`.
- The number of significant digits in the mantissa is the sum of the*minimum integer* and*maximum fraction* digits, and is unaffected by the maximum integer digits. For example, 12345 formatted with`"##0.##E0"`is`"12.3E3"`. To show all digits, set the significant digits count to zero. The number of significant digits does not affect parsing.
- Exponential patterns may not contain grouping separators.

### Rounding

`DecimalFormat`provides rounding modes defined in [java.math.RoundingMode](../java.math/RoundingMode.md) for formatting. By default, it uses [RoundingMode.HALF_EVEN](../java.math/RoundingMode.md).

### Digits

For formatting,`DecimalFormat`uses the ten consecutive characters starting with the localized zero digit defined in the`DecimalFormatSymbols`object as digits. For parsing, these digits as well as all Unicode decimal digits, as defined by java.lang.Character#digit, are recognized.

#### Special Values

`NaN`is formatted as a string, which typically has a single character`&#92;uFFFD`. This string is determined by the`DecimalFormatSymbols`object. This is the only value for which the prefixes and suffixes are not used.

Infinity is formatted as a string, which typically has a single character`&#92;u221E`, with the positive or negative prefixes and suffixes applied. The infinity string is determined by the`DecimalFormatSymbols`object.

Negative zero (`"-0"`) parses to

- `BigDecimal(0)`if`isParseBigDecimal()`is true,
- `Long(0)`if`isParseBigDecimal()`is false and`isParseIntegerOnly()`is true,
- `Double(-0.0)`if both`isParseBigDecimal()`and`isParseIntegerOnly()`are false.

### Synchronization

Decimal formats are generally not synchronized. It is recommended to create separate format instances for each thread. If multiple threads access a format concurrently, it must be synchronized externally.

### Example

```kotlin
<strong><code>// Print out a number using the localized number, integer, currency, // and percent format for each locale</code></strong><code>Locale[] locales = NumberFormat.getAvailableLocales();
  double myNumber = -1234.56;
  NumberFormat form;
  for (int j = 0; j &lt; 4; ++j) {
      System.out.println("FORMAT");
      for (int i = 0; i &lt; locales.length; ++i) {
          if (locales[i].getCountry().length() == 0) {
             continue; // Skip language-only locales
          }
          System.out.print(locales[i].getDisplayName());
          switch (j) {
          case 0:
              form = NumberFormat.getInstance(locales[i]); break;
          case 1:
              form = NumberFormat.getIntegerInstance(locales[i]); break;
          case 2:
              form = NumberFormat.getCurrencyInstance(locales[i]); break;
          default:
              form = NumberFormat.getPercentInstance(locales[i]); break;
          }
          if (form instanceof DecimalFormat) {
              System.out.print(": " + ((DecimalFormat) form).toPattern());
          }
          System.out.print(" -&gt; " + form.format(myNumber));
          try {
              System.out.println(" -&gt; " + form.parse(form.format(myNumber)));
          } catch (ParseException e) {}
      }
  }
  </code>
```

## Summary

| Inherited constants ||
|---|---|
| From class [NumberFormat](NumberFormat.md) |----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FRACTION_FIELD](NumberFormat.md) <br /> Field constant used to construct a FieldPosition object. Signifies that the position of the fraction part of a formatted number should be returned. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTEGER_FIELD](NumberFormat.md) <br /> Field constant used to construct a FieldPosition object. Signifies that the position of the integer part of a formatted number should be returned. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DecimalFormat](DecimalFormat.md))`()` Creates a DecimalFormat using the default pattern and symbols for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| [DecimalFormat](DecimalFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a DecimalFormat using the given pattern and the symbols for the default [FORMAT](../java/util/Locale.Category.md) locale. |
| [DecimalFormat](DecimalFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `symbols:` ` [DecimalFormatSymbols](DecimalFormatSymbols.md)!`)` Creates a DecimalFormat using the given pattern and symbols. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyLocalizedPattern](DecimalFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Apply the given pattern to this Format object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [applyPattern](DecimalFormat.md))`(`pattern:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Apply the given pattern to this Format object. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](DecimalFormat.md))`()` Standard override; no change in semantics. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](DecimalFormat.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Overrides equals |
| open [StringBuffer](../java.lang/StringBuffer.md) | [format](DecimalFormat.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `result:` ` [StringBuffer](../java.lang/StringBuffer.md)`, `fieldPosition:` ` [FieldPosition](FieldPosition.md)`)` Formats a double to produce a string. |
| [StringBuffer](../java.lang/StringBuffer.md) | [format](DecimalFormat.md))`(`number:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`, `toAppendTo:` ` [StringBuffer](../java.lang/StringBuffer.md)`, `pos:` ` [FieldPosition](FieldPosition.md)`)` Formats a number and appends the resulting text to the given string buffer. |
| --- | --- |
| open [StringBuffer](../java.lang/StringBuffer.md) | [format](DecimalFormat.md))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `result:` ` [StringBuffer](../java.lang/StringBuffer.md)`, `fieldPosition:` ` [FieldPosition](FieldPosition.md)`)` Format a long to produce a string. |
| open [AttributedCharacterIterator](AttributedCharacterIterator.md)! | [formatToCharacterIterator](DecimalFormat.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Formats an Object producing an`AttributedCharacterIterator`. |
| open [Currency](../java.util/Currency.md)? | [getCurrency](DecimalFormat.md))`()` Gets the currency used by this decimal format when formatting currency values. |
| --- | --- |
| open [DecimalFormatSymbols](DecimalFormatSymbols.md)! | [getDecimalFormatSymbols](DecimalFormat.md))`()` Returns a copy of the decimal format symbols, which is generally not changed by the programmer or user. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupingSize](DecimalFormat.md))`()` Return the grouping size. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumFractionDigits](DecimalFormat.md))`()` Gets the maximum number of digits allowed in the fraction portion of a number. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaximumIntegerDigits](DecimalFormat.md))`()` Gets the maximum number of digits allowed in the integer portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumFractionDigits](DecimalFormat.md))`()` Gets the minimum number of digits allowed in the fraction portion of a number. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMinimumIntegerDigits](DecimalFormat.md))`()` Gets the minimum number of digits allowed in the integer portion of a number. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMultiplier](DecimalFormat.md))`()` Gets the multiplier for use in percent, per mille, and similar formats. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNegativePrefix](DecimalFormat.md))`()` Get the negative prefix. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNegativeSuffix](DecimalFormat.md))`()` Get the negative suffix. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPositivePrefix](DecimalFormat.md))`()` Get the positive prefix. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPositiveSuffix](DecimalFormat.md))`()` Get the positive suffix. |
| open [RoundingMode](../java.math/RoundingMode.md) | [getRoundingMode](DecimalFormat.md))`()` Gets the [java.math.RoundingMode](../java.math/RoundingMode.md) used in this DecimalFormat. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](DecimalFormat.md))`()` Overrides hashCode |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDecimalSeparatorAlwaysShown](DecimalFormat.md))`()` Allows you to get the behavior of the decimal separator with integers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGroupingUsed](DecimalFormat.md))`()` Returns true if grouping is used in this format. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseBigDecimal](DecimalFormat.md))`()` Returns whether the [parse(java.lang.String,java.text.ParsePosition)](DecimalFormat.md))method returns`BigDecimal`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isParseIntegerOnly](DecimalFormat.md))`()` Returns true if this format will parse numbers as integers only. |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](DecimalFormat.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](ParsePosition.md)`)` Parses text from a string to produce a`Number`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrency](DecimalFormat.md))`(`currency:` ` [Currency](../java.util/Currency.md)`)` Sets the currency used by this number format when formatting currency values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalFormatSymbols](DecimalFormat.md))`(`newSymbols:` ` [DecimalFormatSymbols](DecimalFormatSymbols.md)!`)` Sets the decimal format symbols, which is generally not changed by the programmer or user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecimalSeparatorAlwaysShown](DecimalFormat.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Allows you to set the behavior of the decimal separator with integers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingSize](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the grouping size. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupingUsed](DecimalFormat.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether or not grouping will be used in this format. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumFractionDigits](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the fraction portion of a number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaximumIntegerDigits](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the maximum number of digits allowed in the integer portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumFractionDigits](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the fraction portion of a number. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinimumIntegerDigits](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits allowed in the integer portion of a number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMultiplier](DecimalFormat.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the multiplier for use in percent, per mille, and similar formats. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativePrefix](DecimalFormat.md))`(`newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the negative prefix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativeSuffix](DecimalFormat.md))`(`newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the negative suffix. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseBigDecimal](DecimalFormat.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the [parse(java.lang.String,java.text.ParsePosition)](DecimalFormat.md))method returns`BigDecimal`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParseIntegerOnly](DecimalFormat.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether or not numbers should be parsed as integers only. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositivePrefix](DecimalFormat.md))`(`newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the positive prefix. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositiveSuffix](DecimalFormat.md))`(`newValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the positive suffix. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoundingMode](DecimalFormat.md))`(`roundingMode:` ` [RoundingMode](../java.math/RoundingMode.md)?`)` Sets the [java.math.RoundingMode](../java.math/RoundingMode.md) used in this DecimalFormat. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLocalizedPattern](DecimalFormat.md))`()` Synthesizes a localized pattern string that represents the current state of this Format object. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toPattern](DecimalFormat.md))`()` Synthesizes a pattern string that represents the current state of this Format object. |

| Inherited functions ||
|---|---|
| From class [NumberFormat](NumberFormat.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](NumberFormat.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` <br /> Specialization of format. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [format](NumberFormat.md))`(`number:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Specialization of format. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](../java.util/Locale.md)!> | [getAvailableLocales](NumberFormat.md))`()` <br /> Returns a scientific format for the current default locale. /\*public\* static final NumberFormat getScientificInstance() { return getInstance(Locale.getDefault(Locale.Category.FORMAT), null, SCIENTIFICSTYLE); } /\*\* Returns a scientific format for the specified locale. <br /> | | [NumberFormat](NumberFormat.md) | [getCurrencyInstance](NumberFormat.md))`()` <br /> Returns a currency format for the current default [FORMAT](../java/util/Locale.Category.md) locale. This is equivalent to calling [getCurrencyInstance(Locale.getDefault(Locale.Category.FORMAT))](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getCurrencyInstance](NumberFormat.md))`(`inLocale:` ` [Locale](../java.util/Locale.md)`)` <br /> Returns a currency format for the specified locale. If the specified locale contains the "`cf`" ([currency format style](https://www.unicode.org/reports/tr35/tr35.html#UnicodeCurrencyFormatIdentifier)) [Unicode extension](../java.util/Locale.md), the returned currency format uses the style if it is available. Otherwise, the style uses the default "`standard`" currency format. For example, if the style designates "`account`", negative currency amounts use a pair of parentheses in some locales. <br /> | | [NumberFormat](NumberFormat.md) | [getInstance](NumberFormat.md))`()` <br /> Returns a general-purpose number format for the current default [FORMAT](../java/util/Locale.Category.md) locale. This is the same as calling [getNumberInstance()](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getInstance](NumberFormat.md))`(`inLocale:` ` [Locale](../java.util/Locale.md)`)` <br /> Returns a general-purpose number format for the specified locale. This is the same as calling [getNumberInstance(inLocale)](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getIntegerInstance](NumberFormat.md))`()` <br /> Returns an integer number format for the current default [FORMAT](../java/util/Locale.Category.md) locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](../java.math/RoundingMode.md)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](NumberFormat.md))). This is equivalent to calling [getIntegerInstance(Locale.getDefault(Locale.Category.FORMAT))](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getIntegerInstance](NumberFormat.md))`(`inLocale:` ` [Locale](../java.util/Locale.md)`)` <br /> Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using half-even rounding (see [RoundingMode.HALF_EVEN](../java.math/RoundingMode.md)) for formatting, and to parse only the integer part of an input string (see [isParseIntegerOnly](NumberFormat.md))). <br /> | | [NumberFormat](NumberFormat.md) | [getNumberInstance](NumberFormat.md))`()` <br /> Returns a general-purpose number format for the current default [FORMAT](../java/util/Locale.Category.md) locale. This is equivalent to calling [getNumberInstance(Locale.getDefault(Locale.Category.FORMAT))](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getNumberInstance](NumberFormat.md))`(`inLocale:` ` [Locale](../java.util/Locale.md)`)` <br /> Returns a general-purpose number format for the specified locale. <br /> | | [NumberFormat](NumberFormat.md) | [getPercentInstance](NumberFormat.md))`()` <br /> Returns a percentage format for the current default [FORMAT](../java/util/Locale.Category.md) locale. This is equivalent to calling [getPercentInstance(Locale.getDefault(Locale.Category.FORMAT))](NumberFormat.md)). <br /> | | [NumberFormat](NumberFormat.md) | [getPercentInstance](NumberFormat.md))`(`inLocale:` ` [Locale](../java.util/Locale.md)`)` <br /> Returns a percentage format for the specified locale. <br /> | | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | [parse](NumberFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> Parses text from the beginning of the given string to produce a number. The method may not use the entire text of the given string. See the [parse(java.lang.String,java.text.ParsePosition)](NumberFormat.md))method for more information on number parsing. **WARNING:** Don't use this method to deserialize a number. The underlying localized number format and parsing behaviors can change across Android versions as common usage in the locale changes. Consider using the parse methods in the boxed types, e.g. [Long.parseLong(String)](../java.lang/Long.md)), or [java.math.BigDecimal](../java.math/BigDecimal.md) for deserializing a locale-independent decimal number. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [parseObject](NumberFormat.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `pos:` ` [ParsePosition](ParsePosition.md)`)` <br /> Parses text from a string to produce a`Number`. The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed number is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned. See the [parse(java.lang.String,java.text.ParsePosition)](NumberFormat.md))method for more information on number parsing. <br /> | ||
| From class [Format](Format.md) |----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [format](Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an object to produce a string. This is equivalent to [format](Format.md))`(obj, new StringBuffer(), new FieldPosition(0)).toString();` <br /> | | [AttributedCharacterIterator](AttributedCharacterIterator.md)! | [formatToCharacterIterator](Format.md))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String. Each attribute key of the AttributedCharacterIterator will be of type`Field`. It is up to each`Format`implementation to define what the legal values are for each attribute in the`AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value. The default implementation creates an`AttributedCharacterIterator`with no attributes. Subclasses that support fields should override this and create an`AttributedCharacterIterator`with meaningful attributes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [parseObject](Format.md))`(`source:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Parses text from the beginning of the given string to produce an object. The method may not use the entire text of the given string. <br /> | ||

## Public constructors

### DecimalFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormat()
```

Creates a DecimalFormat using the default pattern and symbols for the default [FORMAT](../java/util/Locale.Category.md) locale. This is a convenient way to obtain a DecimalFormat when internationalization is not the main concern.

To obtain standard formats for a given locale, use the factory methods on NumberFormat such as getNumberInstance. These factories will return the most appropriate sub-class of NumberFormat for a given locale. 
**See Also**

### DecimalFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormat(pattern: String!)
```

Creates a DecimalFormat using the given pattern and the symbols for the default [FORMAT](../java/util/Locale.Category.md) locale. This is a convenient way to obtain a DecimalFormat when internationalization is not the main concern.

To obtain standard formats for a given locale, use the factory methods on NumberFormat such as getNumberInstance. These factories will return the most appropriate sub-class of NumberFormat for a given locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a non-localized pattern string. |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if`pattern`is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid. |

**See Also**

### DecimalFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DecimalFormat(
    pattern: String!, 
    symbols: DecimalFormatSymbols!)
```

Creates a DecimalFormat using the given pattern and symbols. Use this constructor when you need to completely customize the behavior of the format.

To obtain standard formats for a given locale, use the factory methods on NumberFormat such as getInstance or getCurrencyInstance. If you need only minor adjustments to a standard format, you can modify the format returned by a NumberFormat factory method.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a non-localized pattern string |
| `symbols` | [DecimalFormatSymbols](DecimalFormatSymbols.md)!:the set of symbols to be used |

| Exceptions ||
|--------------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if any of the given arguments is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

**See Also**

- [java.text.DecimalFormatSymbols](DecimalFormatSymbols.md)

## Public methods

### applyLocalizedPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyLocalizedPattern(pattern: String!): Unit
```

Apply the given pattern to this Format object. The pattern is assumed to be in a localized notation. A pattern is a short-hand specification for the various formatting properties. These properties can also be changed individually through the various setter methods.

There is no limit to integer digits set by this routine, since that is the typical end-user desire; use setMaximumInteger if you want to set a real value. For negative numbers, use a second pattern, separated by a semicolon

Example`"#,#00.0#"`→ 1,234.56

This means a minimum of 2 integer digits, 1 fraction digit, and a maximum of 2 fraction digits.

Example:`"#,#00.0#;(#,#00.0#)"`for negatives in parentheses.

In negative patterns, the minimum and maximum counts are ignored; these are presumed to be set in the positive pattern.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a new pattern |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if`pattern`is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid. |

### applyPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun applyPattern(pattern: String!): Unit
```

Apply the given pattern to this Format object. A pattern is a short-hand specification for the various formatting properties. These properties can also be changed individually through the various setter methods.

There is no limit to integer digits set by this routine, since that is the typical end-user desire; use setMaximumInteger if you want to set a real value. For negative numbers, use a second pattern, separated by a semicolon

Example`"#,#00.0#"`→ 1,234.56

This means a minimum of 2 integer digits, 1 fraction digit, and a maximum of 2 fraction digits.

Example:`"#,#00.0#;(#,#00.0#)"`for negatives in parentheses.

In negative patterns, the minimum and maximum counts are ignored; these are presumed to be set in the positive pattern.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a new pattern |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if`pattern`is null |
| `java.lang.IllegalArgumentException` | if the given pattern is invalid. |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Standard override; no change in semantics.

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

Overrides equals

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
    result: StringBuffer, 
    fieldPosition: FieldPosition
): StringBuffer
```

Formats a double to produce a string.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The double to format |
| `toAppendTo` | the StringBuffer to which the formatted text is to be appended |
| `pos` | keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](NumberFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |
| --- | --- |
| `result` | [StringBuffer](../java.lang/StringBuffer.md):where the text is to be appended |
| `fieldPosition` | [FieldPosition](FieldPosition.md):keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](NumberFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [StringBuffer](../java.lang/StringBuffer.md) | The formatted number string |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |
| `java.lang.NullPointerException` | if`result`or`fieldPosition`is`null` |

**See Also**

- [java.text.FieldPosition](FieldPosition.md) 

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun format(
    number: Any, 
    toAppendTo: StringBuffer, 
    pos: FieldPosition
): StringBuffer
```

Formats a number and appends the resulting text to the given string buffer. The number can be of any subclass of [java.lang.Number](../java.lang/Number.md).

This implementation uses the maximum precision permitted.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | The object to format |
| `toAppendTo` | [StringBuffer](../java.lang/StringBuffer.md):the`StringBuffer`to which the formatted text is to be appended |
| `pos` | [FieldPosition](FieldPosition.md):keeps track on the position of the field within the returned string. For example, for formatting a number`1234567.89`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](NumberFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 9, respectively for the output string`1,234,567.89`. |
| --- | --- |
| `number` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the number to format |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------------|
| [StringBuffer](../java.lang/StringBuffer.md) | the value passed in as`toAppendTo` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`toAppendTo`or`pos`is null |
| `java.lang.IllegalArgumentException` | if`number`is null or not an instance of`Number`. |
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |
| --- | --- |

**See Also**

- [java.text.FieldPosition](FieldPosition.md) 

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(
    number: Long, 
    result: StringBuffer, 
    fieldPosition: FieldPosition
): StringBuffer
```

Format a long to produce a string.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `number` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The long to format |
| `toAppendTo` | the StringBuffer to which the formatted text is to be appended |
| `pos` | keeps track on the position of the field within the returned string. For example, for formatting a number`123456789`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](NumberFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 11, respectively for the output string`123,456,789`. |
| --- | --- |
| `result` | [StringBuffer](../java.lang/StringBuffer.md):where the text is to be appended |
| `fieldPosition` | [FieldPosition](FieldPosition.md):keeps track on the position of the field within the returned string. For example, for formatting a number`123456789`in`Locale.US`locale, if the given`fieldPosition`is [NumberFormat.INTEGER_FIELD](NumberFormat.md), the begin index and end index of`fieldPosition`will be set to 0 and 11, respectively for the output string`123,456,789`. |

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [StringBuffer](../java.lang/StringBuffer.md) | The formatted number string |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |
| `java.lang.NullPointerException` | if`result`or`fieldPosition`is`null` |

**See Also**

- [java.text.FieldPosition](FieldPosition.md) 

### formatToCharacterIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Formats an Object producing an`AttributedCharacterIterator`. You can use the returned`AttributedCharacterIterator`to build the resulting String, as well as to determine information about the resulting String.

Each attribute key of the AttributedCharacterIterator will be of type`NumberFormat.Field`, with the attribute value being the same as the attribute key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to format |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [AttributedCharacterIterator](AttributedCharacterIterator.md)! | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if obj is null. |
| `java.lang.IllegalArgumentException` | when the Format cannot format the given object. |
| `java.lang.ArithmeticException` | if rounding is needed with rounding mode being set to RoundingMode.UNNECESSARY |
| --- | --- |

### getCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency?
```

Gets the currency used by this decimal format when formatting currency values. The currency is obtained by calling [DecimalFormatSymbols.getCurrency](DecimalFormatSymbols.md))on this number format's symbols.

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------|
| [Currency](../java.util/Currency.md)? | the currency used by this decimal format, or`null` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the number format class doesn't implement currency formatting |

### getDecimalFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecimalFormatSymbols(): DecimalFormatSymbols!
```

Returns a copy of the decimal format symbols, which is generally not changed by the programmer or user.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [DecimalFormatSymbols](DecimalFormatSymbols.md)! | a copy of the desired DecimalFormatSymbols |

**See Also**

- [java.text.DecimalFormatSymbols](DecimalFormatSymbols.md) 

### getGroupingSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGroupingSize(): Int
```

Return the grouping size. Grouping size is the number of digits between grouping separators in the integer portion of a number. For example, in the number "123,456.78", the grouping size is 3. Grouping size of zero designates that grouping is not used, which provides the same formatting as if calling [setGroupingUsed(false)](DecimalFormat.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the grouping size |

**See Also**

- [#setGroupingSize](DecimalFormat.md))
- [java.text.NumberFormat#isGroupingUsed](NumberFormat.md))
- [java.text.DecimalFormatSymbols#getGroupingSeparator](DecimalFormatSymbols.md)) 

### getMaximumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumFractionDigits(): Int
```

Gets the maximum number of digits allowed in the fraction portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of the return value and 340 is used.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of digits. |

**See Also**

- [#setMaximumFractionDigits](DecimalFormat.md)) 

### getMaximumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaximumIntegerDigits(): Int
```

Gets the maximum number of digits allowed in the integer portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of the return value and 309 is used.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of digits |

**See Also**

- [#setMaximumIntegerDigits](DecimalFormat.md)) 

### getMinimumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumFractionDigits(): Int
```

Gets the minimum number of digits allowed in the fraction portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of the return value and 340 is used.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of digits |

**See Also**

- [#setMinimumFractionDigits](DecimalFormat.md)) 

### getMinimumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinimumIntegerDigits(): Int
```

Gets the minimum number of digits allowed in the integer portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of the return value and 309 is used.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum number of digits |

**See Also**

- [#setMinimumIntegerDigits](DecimalFormat.md)) 

### getMultiplier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMultiplier(): Int
```

Gets the multiplier for use in percent, per mille, and similar formats.

| Return ||
|----------------------------------------------------------------------------|----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the multiplier |

**See Also**

- [#setMultiplier(int)](DecimalFormat.md)) 

### getNegativePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNegativePrefix(): String!
```

Get the negative prefix.

Examples: -123, ($123) (with negative suffix), sFr-123

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the negative prefix |

### getNegativeSuffix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNegativeSuffix(): String!
```

Get the negative suffix.

Examples: -123%, ($123) (with positive suffixes)

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the negative suffix |

### getPositivePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositivePrefix(): String!
```

Get the positive prefix.

Examples: +123, $123, sFr123

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the positive prefix |

### getPositiveSuffix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositiveSuffix(): String!
```

Get the positive suffix.

Example: 123%

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the positive suffix |

### getRoundingMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundingMode(): RoundingMode
```

Gets the [java.math.RoundingMode](../java.math/RoundingMode.md) used in this DecimalFormat.

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [RoundingMode](../java.math/RoundingMode.md) | The`RoundingMode`used for this DecimalFormat. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | The default implementation always throws this exception |

**See Also**

- [#setRoundingMode(RoundingMode)](DecimalFormat.md)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Overrides hashCode

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isDecimalSeparatorAlwaysShown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDecimalSeparatorAlwaysShown(): Boolean
```

Allows you to get the behavior of the decimal separator with integers. (The decimal separator will always appear with decimals.)

Example: Decimal ON: 12345 → 12345.; OFF: 12345 → 12345

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the decimal separator is always shown;`false`otherwise |

### isGroupingUsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isGroupingUsed(): Boolean
```

Returns true if grouping is used in this format. For example, in the English locale, with grouping on, the number 1234567 might be formatted as "1,234,567". The grouping separator as well as the size of each group is locale dependent and is determined by sub-classes of NumberFormat.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if grouping is used;`false`otherwise |

### isParseBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isParseBigDecimal(): Boolean
```

Returns whether the [parse(java.lang.String,java.text.ParsePosition)](DecimalFormat.md))method returns`BigDecimal`. The default value is false.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the parse method returns BigDecimal;`false`otherwise |

**See Also**

- [#setParseBigDecimal](DecimalFormat.md)) 

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
open fun parse(
    text: String, 
    pos: ParsePosition
): Number?
```

Parses text from a string to produce a`Number`.

The method attempts to parse text starting at the index given by`pos`. If parsing succeeds, then the index of`pos`is updated to the index after the last character used (parsing does not necessarily use all characters up to the end of the string), and the parsed number is returned. The updated`pos`can be used to indicate the starting point for the next call to this method. If an error occurs, then the index of`pos`is not changed, the error index of`pos`is set to the index of the character where the error occurred, and null is returned.

The subclass returned depends on the value of [isParseBigDecimal](DecimalFormat.md))as well as on the string being parsed.

- If`isParseBigDecimal()`is false (the default), most integer values are returned as`Long`objects, no matter how they are written:`"17"`and`"17.000"`both parse to`Long(17)`. Values that cannot fit into a`Long`are returned as`Double`s. This includes values with a fractional part, infinite values,`NaN`, and the value -0.0.`DecimalFormat`does*not* decide whether to return a`Double`or a`Long`based on the presence of a decimal separator in the source string. Doing so would prevent integers that overflow the mantissa of a double, such as`"-9,223,372,036,854,775,808.00"`, from being parsed accurately.

 Callers may use the`Number`methods`doubleValue`,`longValue`, etc., to obtain the type they want.
- If`isParseBigDecimal()`is true, values are returned as`BigDecimal`objects. The values are the ones constructed by [java.math.BigDecimal#BigDecimal(String)](../java.math/BigDecimal.md))for corresponding strings in locale-independent format. The special cases negative and positive infinity and NaN are returned as`Double`instances holding the values of the corresponding`Double`constants.

`DecimalFormat`parses all Unicode characters that represent decimal digits, as defined by`Character.digit()`. In addition,`DecimalFormat`also recognizes as digits the ten consecutive characters starting with the localized zero digit defined in the`DecimalFormatSymbols`object.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | the String to parse |
| `parsePosition` | the parse position |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the string to be parsed |
| --- | --- |
| `pos` | [ParsePosition](ParsePosition.md):A`ParsePosition`object with index and error index information as described above. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | the parsed value, or`null`if the parse fails |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`text`or`pos`is null. |

### setCurrency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCurrency(currency: Currency): Unit
```

Sets the currency used by this number format when formatting currency values. This does not update the minimum or maximum number of fraction digits used by the number format. The currency is set by calling [DecimalFormatSymbols.setCurrency](DecimalFormatSymbols.md))on this number format's symbols.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `currency` | [Currency](../java.util/Currency.md):the new currency to be used by this decimal format |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the number format class doesn't implement currency formatting |
| `java.lang.NullPointerException` | if`currency`is null |

### setDecimalFormatSymbols

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecimalFormatSymbols(newSymbols: DecimalFormatSymbols!): Unit
```

Sets the decimal format symbols, which is generally not changed by the programmer or user.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `newSymbols` | [DecimalFormatSymbols](DecimalFormatSymbols.md)!:desired DecimalFormatSymbols |

**See Also**

- [java.text.DecimalFormatSymbols](DecimalFormatSymbols.md) 

### setDecimalSeparatorAlwaysShown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecimalSeparatorAlwaysShown(newValue: Boolean): Unit
```

Allows you to set the behavior of the decimal separator with integers. (The decimal separator will always appear with decimals.)

Example: Decimal ON: 12345 → 12345.; OFF: 12345 → 12345

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the decimal separator is always shown;`false`otherwise |

### setGroupingSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingSize(newValue: Int): Unit
```

Set the grouping size. Grouping size is the number of digits between grouping separators in the integer portion of a number. For example, in the number "123,456.78", the grouping size is 3. Grouping size of zero designates that grouping is not used, which provides the same formatting as if calling [setGroupingUsed(false)](DecimalFormat.md)).

The value passed in is converted to a byte, which may lose information. Values that are negative or greater than [Byte.MAX_VALUE](../java.lang/Byte.md), will throw an`IllegalArgumentException`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new grouping size |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`newValue`is negative or greater than [Byte.MAX_VALUE](../java.lang/Byte.md) |

**See Also**

- [#getGroupingSize](DecimalFormat.md))
- [java.text.NumberFormat#setGroupingUsed](NumberFormat.md))
- [java.text.DecimalFormatSymbols#setGroupingSeparator](DecimalFormatSymbols.md)) 

### setGroupingUsed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupingUsed(newValue: Boolean): Unit
```

Set whether or not grouping will be used in this format.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if grouping is used;`false`otherwise |

### setMaximumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumFractionDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the fraction portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of`newValue`and 340 is used. Negative input values are replaced with 0.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [java.text.NumberFormat#setMaximumFractionDigits](NumberFormat.md)) 

### setMaximumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaximumIntegerDigits(newValue: Int): Unit
```

Sets the maximum number of digits allowed in the integer portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of`newValue`and 309 is used. Negative input values are replaced with 0.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of integer digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [java.text.NumberFormat#setMaximumIntegerDigits](NumberFormat.md)) 

### setMinimumFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumFractionDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the fraction portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of`newValue`and 340 is used. Negative input values are replaced with 0.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [java.text.NumberFormat#setMinimumFractionDigits](NumberFormat.md)) 

### setMinimumIntegerDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinimumIntegerDigits(newValue: Int): Unit
```

Sets the minimum number of digits allowed in the integer portion of a number. For formatting numbers other than`BigInteger`and`BigDecimal`objects, the lower of`newValue`and 309 is used. Negative input values are replaced with 0.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum number of integer digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |

**See Also**

- [java.text.NumberFormat#setMinimumIntegerDigits](NumberFormat.md)) 

### setMultiplier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMultiplier(newValue: Int): Unit
```

Sets the multiplier for use in percent, per mille, and similar formats. For a percent format, set the multiplier to 100 and the suffixes to have '%' (for Arabic, use the Arabic percent sign). For a per mille format, set the multiplier to 1000 and the suffixes to have '\\u2030'.

Example: with multiplier 100, 1.23 is formatted as "123", and "123" is parsed into 1.23.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new multiplier |

**See Also**

- [#getMultiplier](DecimalFormat.md)) 

### setNegativePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNegativePrefix(newValue: String!): Unit
```

Set the negative prefix.

Examples: -123, ($123) (with negative suffix), sFr-123

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new negative prefix |

### setNegativeSuffix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNegativeSuffix(newValue: String!): Unit
```

Set the negative suffix.

Examples: 123%

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new negative suffix |

### setParseBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParseBigDecimal(newValue: Boolean): Unit
```

Sets whether the [parse(java.lang.String,java.text.ParsePosition)](DecimalFormat.md))method returns`BigDecimal`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the parse method returns BigDecimal;`false`otherwise |

**See Also**

- [#isParseBigDecimal](DecimalFormat.md)) 

### setParseIntegerOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParseIntegerOnly(value: Boolean): Unit
```

Sets whether or not numbers should be parsed as integers only.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if numbers should be parsed as integers only;`false`otherwise |

### setPositivePrefix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositivePrefix(newValue: String!): Unit
```

Set the positive prefix.

Examples: +123, $123, sFr123

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new positive prefix |

### setPositiveSuffix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositiveSuffix(newValue: String!): Unit
```

Set the positive suffix.

Example: 123%

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------|
| `newValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the new positive suffix |

### setRoundingMode

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRoundingMode(roundingMode: RoundingMode?): Unit
```

Sets the [java.math.RoundingMode](../java.math/RoundingMode.md) used in this DecimalFormat.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------|
| `roundingMode` | [RoundingMode](../java.math/RoundingMode.md)?:The`RoundingMode`to be used |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | The default implementation always throws this exception |
| `java.lang.NullPointerException` | if`roundingMode`is null. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/text/DecimalFormat#getRoundingMode()> 

### toLocalizedPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLocalizedPattern(): String!
```

Synthesizes a localized pattern string that represents the current state of this Format object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a localized pattern string |

**See Also**

- [#applyPattern](DecimalFormat.md)) 

### toPattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toPattern(): String!
```

Synthesizes a pattern string that represents the current state of this Format object.

| Return ||
|-----------------------------------------------------------------------------------|------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a pattern string |

**See Also**

- [#applyPattern](DecimalFormat.md))
