Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalFormat

Kotlin | [Java](../android/icu/text/DecimalFormat.md)
| --- | --- |

```
open class DecimalFormat : NumberFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.text.Format](../java/text/Format.md) ||||
| | ↳ | [android.icu.text.UFormat](../android/icu/text/UFormat.md) |||
| | | ↳ | [android.icu.text.NumberFormat](../android/icu/text/NumberFormat.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.icu.text.DecimalFormat](../android/icu/text/DecimalFormat.md) |

| Known Direct Subclasses [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) |---|---| | [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. | |
| --- | --- | --- | --- | --- | --- | --- |

**\[icu enhancement\]** ICU's replacement for `https://developer.android.com/reference/kotlin/java/text/DecimalFormat.html#`. Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]**'.

**IMPORTANT:** New users are strongly encouraged to see if `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` fits their use case. Although not deprecated, this class, DecimalFormat, is only provided for java.text.DecimalFormat compatibility.
`DecimalFormat` is the primary concrete subclass of `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat`. It has a variety of features designed to make it possible to parse and format numbers in any locale, including support for Western, Arabic, or Indic digits. It supports different flavors of numbers, including integers ("123"), fixed-point numbers ("123.4"), scientific notation ("1.23E4"), percentages ("12%"), and currency amounts ("$123.00", "USD123.00", "123.00 US dollars"). All of these flavors can be easily localized.

To obtain a number formatter for a specific locale (including the default locale), call one of NumberFormat's factory methods such as android.icu.text.NumberFormat#getInstance. Do not call DecimalFormat constructors directly unless you know what you are doing.

DecimalFormat aims to comply with the specification [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns). Read the specification for more information on how all the properties in DecimalFormat fit together.

**NOTE:** Starting in ICU 60, there is a new set of APIs for localized number formatting that are designed to be an improvement over DecimalFormat. New users are discouraged from using DecimalFormat. For more information, see the package android.icu.number.

### Example Usage

Customize settings on a DecimalFormat instance from the NumberFormat factory:

```kotlin
NumberFormat f = NumberFormat.getInstance(loc);
  if (f instanceof DecimalFormat) {
      ((DecimalFormat) f).setDecimalSeparatorAlwaysShown(true);
      ((DecimalFormat) f).setMinimumGroupingDigits(2);
  }
  
```

Quick and dirty print out a number using the localized number, currency, and percent format for each locale:

```kotlin
for (ULocale uloc : ULocale.getAvailableLocales()) {
      System.out.print(uloc + ":\t");
      System.out.print(NumberFormat.getInstance(uloc).format(1.23));
      System.out.print("\t");
      System.out.print(NumberFormat.getCurrencyInstance(uloc).format(1.23));
      System.out.print("\t");
      System.out.print(NumberFormat.getPercentInstance(uloc).format(1.23));
      System.out.println();
  }
  
```

### Properties and Symbols

A DecimalFormat object encapsulates a set of *properties* and a set of *symbols*. Grouping size, rounding mode, and affixes are examples of properties. Locale digits and the characters used for grouping and decimal separators are examples of symbols.

To set a custom set of symbols, use `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalFormatSymbols(android.icu.text.DecimalFormatSymbols)`. Use the various other setters in this class to set custom values for the properties.

### Rounding

DecimalFormat provides three main strategies to specify the position at which numbers should be rounded:

1. **Magnitude:** Display a fixed number of fraction digits; this is the most common form.
2. **Increment:** Round numbers to the closest multiple of a certain increment, such as 0.05. This is common in currencies.
3. **Significant Digits:** Round numbers such that a fixed number of nonzero digits are shown. This is most common in scientific notation.

It is not possible to specify more than one rounding strategy. For example, setting a rounding increment in conjunction with significant digits results in undefined behavior.

It is also possible to specify the *rounding mode* to use. The default rounding mode is "half even", which rounds numbers to their closest increment, with ties broken in favor of trailing numbers being even. For more information, see `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)` and [the ICU User Guide](https://unicode-org.github.io/icu/userguide/format_parse/numbers/rounding-modes).

### Pattern Strings

A *pattern string* is a way to serialize some of the available properties for decimal formatting. However, not all properties are capable of being serialized into a pattern string; see `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyPattern(kotlin.String)` for more information.

Most users should not need to interface with pattern strings directly.

ICU DecimalFormat aims to follow the specification for pattern strings in [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns). Refer to that specification for more information on pattern string syntax.

#### Pattern String BNF

The following BNF is used when parsing the pattern string into property values:

```kotlin
pattern    := subpattern (';' subpattern)?
  subpattern := prefix? number exponent? suffix?
  number     := (integer ('.' fraction)?) | sigDigits
  prefix     := '\u0000'..'\uFFFD' - specialCharacters
  suffix     := '\u0000'..'\uFFFD' - specialCharacters
  integer    := '#'* '0'* '0'
  fraction   := '0'* '#'*
  sigDigits  := '#'* '@' '@'* '#'*
  exponent   := 'E' '+'? '0'* '0'
  padSpec    := '*' padChar
  padChar    := '\u0000'..'\uFFFD' - quote
   
  Notation:
    X*       0 or more instances of X
    X?       0 or 1 instances of X
    X|Y      either X or Y
    C..D     any character from C up to D, inclusive
    S-T      characters in S, except those in T
  
```

The first subpattern is for positive numbers. The second (optional) subpattern is for negative numbers.

Not indicated in the BNF syntax above:

- The grouping separator ',' can occur inside the integer and sigDigits elements, between any two pattern characters of that element, as long as the integer or sigDigits element is not followed by the exponent element.
- Two grouping intervals are recognized: That between the decimal point and the first grouping symbol, and that between the first and second grouping symbols. These intervals are identical in most locales, but in some locales they differ. For example, the pattern "#,##,###" formats the number 123456789 as "12,34,56,789".
- The pad specifier `padSpec` may appear before the prefix, after the prefix, before the suffix, after the suffix, or not at all.
- In place of '0', the digits '1' through '9' may be used to indicate a rounding increment.

### Parsing

DecimalFormat aims to be able to parse anything that it can output as a formatted string.

There are two primary parse modes: *lenient* and *strict* . Lenient mode should be used if the goal is to parse user input to a number; strict mode should be used if the goal is validation. The default is lenient mode. For more information, see `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseStrict(kotlin.Boolean)`.

`DecimalFormat` parses all Unicode characters that represent decimal digits, as defined by android.icu.lang.UCharacter#digit. In addition, `DecimalFormat` also recognizes as digits the ten consecutive characters starting with the localized zero digit defined in the `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols` object. During formatting, the `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols`-based digits are output.

Grouping separators are ignored in lenient mode (default). In strict mode, grouping separators must match the locale-specified grouping sizes.

When using `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#parseCurrency(kotlin.CharSequence,%20java.text.ParsePosition)`, all currencies are accepted, not just the currency currently set in the formatter. In addition, the formatter is able to parse every currency style format for a particular locale no matter which style the formatter is constructed with. For example, a formatter instance gotten from NumberFormat.getInstance(ULocale, NumberFormat.CURRENCYSTYLE) can parse both "USD1.00" and "3.00 US dollars".

Whitespace characters (lenient mode) and control characters (lenient and strict mode), collectively called "ignorables", do not need to match in identity or quantity between the pattern string and the input string. For example, the pattern "# %" matches "35 %" (with a single space), "35%" (with no space), "35 %" (with a non-breaking space), and "35 %" (with multiple spaces). Arbitrary ignorables are also allowed at boundaries between the parts of the number: prefix, number, exponent separator, and suffix. Ignorable whitespace characters are those having the Unicode "blank" property for regular expressions, defined in UTS #18 Annex C, which is "horizontal" whitespace, like spaces and tabs, but not "vertical" whitespace, like line breaks. Ignorable control characters are those in the Unicode set \[:Default_Ignorable_Code_Point:\].

If `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#parse(kotlin.String,%20java.text.ParsePosition)` fails to parse a string, it returns `null` and leaves the parse position unchanged. The convenience method `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parse(kotlin.String)` indicates parse failure by throwing a `https://developer.android.com/reference/kotlin/java/text/ParseException.html#`.

Under the hood, a state table parsing engine is used. To debug a parsing failure during development, use the following pattern to print details about the state table transitions:

```kotlin
android.icu.impl.number.Parse.DEBUGGING = true;
  df.parse("123.45", ppos);
  android.icu.impl.number.Parse.DEBUGGING = false;
  
```

### Thread Safety and Best Practices

Starting with ICU 59, instances of DecimalFormat are thread-safe.

Under the hood, DecimalFormat maintains an immutable formatter object that is rebuilt whenever any of the property setters are called. It is therefore best practice to call property setters only during construction and not when formatting numbers online.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#MINIMUM_GROUPING_DIGITS_AUTO:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)` to specify display grouping using the default strategy for all locales. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#MINIMUM_GROUPING_DIGITS_MIN2:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)` to specify display grouping using locale defaults, except do not show grouping on values smaller than 10000 (such that there is a minimum of two digits before the first separator). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_PREFIX:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted after the prefix. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_SUFFIX:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted after the suffix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_PREFIX:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted before the prefix. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_SUFFIX:kotlin.Int` **\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted before the suffix. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#ACCOUNTINGCURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify currency style of format which uses currency symbol to represent currency for accounting, for example: "($3.00), instead of "-$3.00" (`https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CURRENCYSTYLE:kotlin.Int`). Overrides any style specified using -cf- key in locale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CASHCURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify currency cash style of format which uses currency ISO code to represent currency, for example: "NT$3" instead of "NT$3.23". <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#CURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify general currency style of format. Defaults to STANDARDCURRENCYSTYLE, using currency symbol, for example "$3.00", with non-accounting style for negative values (e.g. minus sign). The specific style may be specified using the -cf- locale key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#FRACTION_FIELD:kotlin.Int` Field constant used to construct a FieldPosition object. Signifies that the position of the fraction part of a formatted number should be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#INTEGERSTYLE:kotlin.Int` **\[icu\]** Constant to specify a integer number style format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#INTEGER_FIELD:kotlin.Int` Field constant used to construct a FieldPosition object. Signifies that the position of the integer part of a formatted number should be returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#ISOCURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify currency style of format which uses currency ISO code to represent currency, for example: "USD3.00". <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#NUMBERSTYLE:kotlin.Int` **\[icu\]** Constant to specify normal number style of format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#PERCENTSTYLE:kotlin.Int` **\[icu\]** Constant to specify a style of format to display percent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#PLURALCURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify currency style of format which uses currency long name with plural format to represent currency, for example, "3.00 US Dollars". <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#SCIENTIFICSTYLE:kotlin.Int` **\[icu\]** Constant to specify a style of format to display scientific number. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#STANDARDCURRENCYSTYLE:kotlin.Int` **\[icu\]** Constant to specify currency style of format which uses currency symbol to represent currency, for example "$3.00", using non-accounting style for negative values (e.g. minus sign). Overrides any style specified using -cf- key in locale. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#DecimalFormat()()` Creates a DecimalFormat based on the number pattern and symbols for the default locale. |
| `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#DecimalFormat(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a DecimalFormat based on the given pattern, using symbols for the default locale. |
| `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#DecimalFormat(kotlin.String,%20android.icu.text.DecimalFormatSymbols)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, symbols: https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols!)` Creates a DecimalFormat based on the given pattern and symbols. |
| `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#DecimalFormat(kotlin.String,%20android.icu.text.DecimalFormatSymbols,%20android.icu.text.CurrencyPluralInfo,%20kotlin.Int)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, symbols: https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols!, infoInput: https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo!, style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a DecimalFormat based on the given pattern and symbols, with additional control over the behavior of currency. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyLocalizedPattern(kotlin.String)(localizedPattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Converts the given string to standard notation and then parses it using `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyPattern(kotlin.String)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyPattern(kotlin.String)(pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parses the given pattern string and overwrites the settings specified in the pattern string. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#areSignificantDigitsUsed()()` **\[icu\]** Returns whether significant digits are being used in rounding. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#clone()()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Tests for equality between this formatter and another formatter. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(android.icu.math.BigDecimal,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#!, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` **\[icu\]** Formats an ICU BigDecimal. |
| --- | --- |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(android.icu.util.CurrencyAmount,%20java.lang.StringBuffer,%20java.text.FieldPosition)(currAmt: https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#!, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` **\[icu\]** Formats a CurrencyAmount. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(kotlin.Double,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Specialization of format. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(java.math.BigDecimal,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` **\[icu\]** Formats a BigDecimal. |
| --- | --- |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(java.math.BigInteger,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` **\[icu\]** Formats a BigInteger. |
| open [StringBuffer](../java/lang/StringBuffer.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#format(kotlin.Long,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, result: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, fieldPosition: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Specialization of format. |
| open [AttributedCharacterIterator](../java/text/AttributedCharacterIterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#formatToCharacterIterator(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Formats an Object producing an `AttributedCharacterIterator`. |
| --- | --- |
| open [Currency](../android/icu/util/Currency.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getCurrency()()` Returns the currency used to display currency amounts. |
| open [CurrencyPluralInfo](../android/icu/text/CurrencyPluralInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getCurrencyPluralInfo()()` **\[icu\]** Returns the current instance of CurrencyPluralInfo. |
| open [Currency.CurrencyUsage](../android/icu/util/Currency.CurrencyUsage.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getCurrencyUsage()()` **\[icu\]** Returns the strategy for rounding currency amounts. |
| --- | --- |
| open [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getDecimalFormatSymbols()()` Returns a copy of the decimal format symbols used by this formatter. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getFormatWidth()()` Returns the minimum number of characters in formatted output. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getGroupingSize()()` Returns the primary grouping size in use. |
| --- | --- |
| open [MathContext](../java/math/MathContext.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMathContext()()` **\[icu\]** Returns the `https://developer.android.com/reference/kotlin/java/math/MathContext.html#` being used to round numbers. |
| open [MathContext](../android/icu/math/MathContext.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMathContextICU()()` **\[icu\]** Returns the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext.html#` being used to round numbers. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMaximumFractionDigits()()` Returns the effective maximum number of integer digits after the decimal separator. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMaximumIntegerDigits()()` Returns the effective maximum number of digits before the decimal separator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMaximumSignificantDigits()()` **\[icu\]** Returns the effective maximum number of significant digits displayed. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMinimumExponentDigits()()` **\[icu\]** Returns the minimum number of digits printed in the exponent in scientific notation. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMinimumFractionDigits()()` Returns the effective minimum number of integer digits after the decimal separator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMinimumGroupingDigits()()` **\[icu\]** Returns the minimum number of digits before grouping is triggered. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMinimumIntegerDigits()()` Returns the effective minimum number of digits before the decimal separator. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMinimumSignificantDigits()()` **\[icu\]** Returns the effective minimum number of significant digits displayed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getMultiplier()()` Returns the multiplier being applied to numbers before they are formatted. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getNegativePrefix()()` **Affixes:** Gets the negative prefix string currently being used to format numbers. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getNegativeSuffix()()` **Affixes:** Gets the negative suffix string currently being used to format numbers. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadCharacter()()` **\[icu\]** Returns the character used for padding. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()()` **\[icu\]** Returns the position used for padding. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getParseMaxDigits()()` Always returns 1000, the default prior to ICU 59. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPositivePrefix()()` **Affixes:** Gets the positive prefix string currently being used to format numbers. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPositiveSuffix()()` **Affixes:** Gets the positive suffix string currently being used to format numbers. |
| --- | --- |
| open [BigDecimal](../java/math/BigDecimal.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getRoundingIncrement()()` **\[icu\]** Returns the increment to which numbers are being rounded. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getRoundingMode()()` Returns the rounding mode being used to round numbers. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getSecondaryGroupingSize()()` **\[icu\]** Returns the secondary grouping size in use. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#hashCode()()` Returns a hash code value for the object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isDecimalPatternMatchRequired()()` **\[icu\]** Returns whether the presence of a decimal point must match the pattern. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isDecimalSeparatorAlwaysShown()()` Returns whether the decimal separator is shown on integers. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isExponentSignAlwaysShown()()` **\[icu\]** Returns whether the sign (plus or minus) is always printed in scientific notation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isGroupingUsed()()` Returns whether or not grouping separators are being printed in the output. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isParseBigDecimal()()` Returns whether #parse will always return a BigDecimal. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isParseCaseSensitive()()` **\[icu\]** Returns whether to force case (uppercase/lowercase) to match when parsing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isParseIntegerOnly()()` Returns true if this format will parse numbers as integers only. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isParseNoExponent()()` **\[icu\]** Returns whether to ignore exponents when parsing. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isParseStrict()()` **\[icu\]** Returns whether strict parsing is in effect. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isScientificNotation()()` **\[icu\]** Returns whether scientific (exponential) notation is enabled on this formatter. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#isSignAlwaysShown()()` **\[icu\]** Returns whether the sign is being shown on positive numbers. |
| --- | --- |
| open [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#parse(kotlin.String,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parsePosition: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals); otherwise, returns another type, such as a BigDecimal, BigInteger, or Double. |
| open [CurrencyAmount](../android/icu/util/CurrencyAmount.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#parseCurrency(kotlin.CharSequence,%20java.text.ParsePosition)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, parsePosition: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses text from the given string as a CurrencyAmount. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrency(android.icu.util.Currency)(currency: https://developer.android.com/reference/kotlin/android/icu/util/Currency.html#!)` Sets the currency to be used when formatting numbers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrencyPluralInfo(android.icu.text.CurrencyPluralInfo)(newInfo: https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo!)` **\[icu\]** Sets a custom instance of CurrencyPluralInfo. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrencyUsage(android.icu.util.Currency.CurrencyUsage)(usage: https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage.html#!)` **\[icu\]** Sets the currency-dependent strategy to use when rounding numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalFormatSymbols(android.icu.text.DecimalFormatSymbols)(newSymbols: https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols!)` Sets the decimal format symbols used by this formatter. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalPatternMatchRequired(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** **Parsing:** This method is used to either *require* or the presence of a decimal point in the string being parsed (disabled by default). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalSeparatorAlwaysShown(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **Separators:** Sets whether the decimal separator (a period in *en-US*) is shown on integers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setExponentSignAlwaysShown(kotlin.Boolean)(expSignAlways: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** **Scientific Notation:** Sets whether the sign (plus or minus) is always to be shown in the exponent in scientific notation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Padding:** Sets the minimum width of the string output by the formatting pipeline. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingSize(kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Grouping:** Sets the primary grouping size (distance between grouping separators) used when formatting large numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingUsed(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **Grouping:** Sets whether grouping is to be used when formatting numbers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)(mathContext: https://developer.android.com/reference/kotlin/java/math/MathContext.html#!)` **\[icu\]** **Rounding and Digit Limits:** Sets the `https://developer.android.com/reference/kotlin/java/math/MathContext.html#` used to round numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContextICU(android.icu.math.MathContext)(mathContextICU: https://developer.android.com/reference/kotlin/android/icu/math/MathContext.html#!)` **\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)` for `https://developer.android.com/reference/kotlin/android/icu/math/MathContext.html#`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Rounding and Digit Limits:** Sets the maximum number of digits to display after the decimal separator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumIntegerDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Rounding and Digit Limits:** Sets the maximum number of digits to display before the decimal separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** **Rounding and Digit Limits:** Sets the maximum number of significant digits to be displayed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumExponentDigits(kotlin.Byte)(minExpDig: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)` **\[icu\]** **Scientific Notation:** Sets the minimum number of digits to be printed in the exponent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumFractionDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Rounding and Digit Limits:** Sets the minimum number of digits to display after the decimal separator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** Sets the minimum number of digits that must be before the first grouping separator in order for the grouping separator to be printed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumIntegerDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Rounding and Digit Limits:** Sets the minimum number of digits to display before the decimal separator. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumSignificantDigits(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** **Rounding and Digit Limits:** Sets the minimum number of significant digits to be displayed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMultiplier(kotlin.Int)(multiplier: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets a number that will be used to multiply all numbers prior to formatting. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setNegativePrefix(kotlin.String)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Affixes:** Sets the string to prepend to negative numbers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setNegativeSuffix(kotlin.String)(suffix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Affixes:** Sets the string to append to negative numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadCharacter(kotlin.Char)(padChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` **\[icu\]** **Padding:** Sets the character used to pad numbers that are narrower than the width specified in `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)(padPos: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** **Padding:** Sets the position where to insert the pad character when narrower than the width specified in `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseBigDecimal(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to make #parse prefer returning a `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#` when possible. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseCaseSensitive(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** Specifies whether parsing should require cases to match in affixes, exponent separators, and currency codes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseIntegerOnly(kotlin.Boolean)(parseIntegerOnly: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **Parsing:** Sets whether to ignore the fraction part of a number when parsing (defaults to false). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseMaxDigits(kotlin.Int)(maxDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseNoExponent(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** Specifies whether to stop parsing when an exponent separator is encountered. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseStrict(kotlin.Boolean)(parseStrict: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** Sets whether strict parsing is in effect. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPositivePrefix(kotlin.String)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Affixes:** Sets the string to prepend to positive numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPositiveSuffix(kotlin.String)(suffix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Affixes:** Sets the string to append to positive numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(android.icu.math.BigDecimal)(increment: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#!)` **\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(java.math.BigDecimal)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(kotlin.Double)(increment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` **\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(java.math.BigDecimal)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(java.math.BigDecimal)(increment: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` **\[icu\]** **Rounding and Digit Limits:** Sets an increment, or interval, to which numbers are rounded. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)(roundingMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Rounding and Digit Limits:** Sets the `https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#` used to round numbers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setScientificNotation(kotlin.Boolean)(useScientific: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** **Scientific Notation:** Sets whether this formatter should print in scientific (exponential) notation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSecondaryGroupingSize(kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **\[icu\]** **Grouping:** Sets the secondary grouping size (distance between grouping separators after the first separator) used when formatting large numbers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSignAlwaysShown(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to always shown the plus sign ('+' in *en*) on positive numbers. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSignificantDigitsUsed(kotlin.Boolean)(useSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` **\[icu\]** **Rounding and Digit Limits:** Sets whether significant digits are to be used in rounding. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#toLocalizedPattern()()` Calls `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#toPattern()` and converts the string to localized notation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#toPattern()()` Serializes this formatter object to a decimal format pattern string. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#toString()()` Returns the default value of toString() with extra DecimalFormat-specific information appended to the end of the string. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.math.BigDecimal)(number: https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#!)` **\[icu\]** Convenience method to format an ICU BigDecimal. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(android.icu.util.CurrencyAmount)(currAmt: https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#!)` **\[icu\]** Convenience method to format a CurrencyAmount. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Double)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Specialization of format. <br /> | | `https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Any,%20java.lang.StringBuffer,%20java.text.FieldPosition)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!, toAppendTo: https://developer.android.com/reference/kotlin/java/lang/StringBuffer.html#!, pos: https://developer.android.com/reference/kotlin/java/text/FieldPosition.html#!)` Formats a number and appends the resulting text to the given string buffer. **\[icu\] Note:** recognizes `BigInteger` and `BigDecimal` objects. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigDecimal)(number: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` Convenience method to format a BigDecimal. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(java.math.BigInteger)(number: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!)` **\[icu\]** Convenience method to format a BigInteger. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#format(kotlin.Long)(number: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Specialization of format. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.html#!>!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getAvailableLocales()()` Returns the list of Locales for which NumberFormats are available. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getContext(android.icu.text.DisplayContext.Type)(type: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext.Type!)` **\[icu\]** Get the formatter's DisplayContext value for the specified DisplayContext.Type, such as CAPITALIZATION. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a currency format for the current default `FORMAT` locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a currency format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getCurrencyInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a currency format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns the default number format for the current default `FORMAT` locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getIntegerInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(android.icu.util.ULocale,%20kotlin.Int)(desiredLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, choice: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a specific style number format for a specific locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(kotlin.Int)(style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a specific style number format for default `FORMAT` locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns the default number format for the specified locale. The default format is one of the styles provided by the other factory methods: getNumberInstance, getCurrencyInstance or getPercentInstance. Exactly which one is locale-dependent. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getInstance(java.util.Locale,%20kotlin.Int)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!, style: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a specific style number format for a specific locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns an integer number format for the current default `FORMAT` locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int`) for formatting, and to parse only the integer part of an input string (see `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly()`). <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int`) for formatting, and to parse only the integer part of an input string (see `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly()`). <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getIntegerInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns an integer number format for the specified locale. The returned number format is configured to round floating point numbers to the nearest integer using IEEE half-even rounding (see `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#ROUND_HALF_EVEN:kotlin.Int`) for formatting, and to parse only the integer part of an input string (see `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#isParseIntegerOnly()`). <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a general-purpose number format for the current default `FORMAT` locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a general-purpose number format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getNumberInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a general-purpose number format for the specified locale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPattern(android.icu.util.ULocale,%20kotlin.Int)(forLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!, choice: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the pattern for the provided locale and choice. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a percentage format for the current default `FORMAT` locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a percentage format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getPercentInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. Returns a percentage format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance()()` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a scientific format for the current default `FORMAT` locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance(android.icu.util.ULocale)(inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a scientific format for the specified locale. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#getScientificInstance(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` **NOTE:** New users are strongly encouraged to use `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.html#` instead of NumberFormat. **\[icu\]** Returns a scientific format for the specified locale. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parse(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Parses text from the beginning of the given string to produce a number. The method might not use the entire text of the given string. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#parseObject(kotlin.String,%20java.text.ParsePosition)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, parsePosition: https://developer.android.com/reference/kotlin/java/text/ParsePosition.html#!)` Parses text from a string to produce a number. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat#setContext(android.icu.text.DisplayContext)(context: https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext!)` **\[icu\]** Set a particular DisplayContext value in the formatter, such as CAPITALIZATION_FOR_STANDALONE. <br /> | ||

## Constants

### MINIMUM_GROUPING_DIGITS_AUTO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINIMUM_GROUPING_DIGITS_AUTO: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)` to specify display grouping using the default strategy for all locales.

 Value: -2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#MINIMUM_GROUPING_DIGITS_MIN2:kotlin.Int`

### MINIMUM_GROUPING_DIGITS_MIN2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MINIMUM_GROUPING_DIGITS_MIN2: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)` to specify display grouping using locale defaults, except do not show grouping on values smaller than 10000 (such that there is a minimum of two digits before the first separator).

 Value: -3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#MINIMUM_GROUPING_DIGITS_AUTO:kotlin.Int`

### PAD_AFTER_PREFIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAD_AFTER_PREFIX: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted after the prefix.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_SUFFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_SUFFIX:kotlin.Int`

### PAD_AFTER_SUFFIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAD_AFTER_SUFFIX: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted after the suffix.

 Value: 3

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_SUFFIX:kotlin.Int`

### PAD_BEFORE_PREFIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAD_BEFORE_PREFIX: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted before the prefix.

 Value: 0

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_SUFFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_SUFFIX:kotlin.Int`

### PAD_BEFORE_SUFFIX

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAD_BEFORE_SUFFIX: Int
```

**\[icu\]** Constant for `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)` to specify pad characters inserted before the suffix.

 Value: 2

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#getPadPosition()`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_PREFIX:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_SUFFIX:kotlin.Int`

## Public constructors

### DecimalFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormat()
```

Creates a DecimalFormat based on the number pattern and symbols for the default locale. This is a convenient way to obtain a DecimalFormat instance when internationalization is not the main concern.

Most users should call the factory methods on NumberFormat, such as android.icu.text.NumberFormat#getNumberInstance, which return localized formatter objects, instead of the DecimalFormat constructors.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### DecimalFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormat(pattern: String!)
```

Creates a DecimalFormat based on the given pattern, using symbols for the default locale. This is a convenient way to obtain a DecimalFormat instance when internationalization is not the main concern.

Most users should call the factory methods on NumberFormat, such as android.icu.text.NumberFormat#getNumberInstance, which return localized formatter objects, instead of the DecimalFormat constructors.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A pattern string such as "#,##0.00" conforming to [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns). |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given pattern is invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### DecimalFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormat(
    pattern: String!, 
    symbols: DecimalFormatSymbols!)
```

Creates a DecimalFormat based on the given pattern and symbols. Use this constructor if you want complete control over the behavior of the formatter.

Most users should call the factory methods on NumberFormat, such as android.icu.text.NumberFormat#getNumberInstance, which return localized formatter objects, instead of the DecimalFormat constructors.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A pattern string such as "#,##0.00" conforming to [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns). |
| `symbols` | [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)!: The set of symbols to be used. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given pattern is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols`

### DecimalFormat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DecimalFormat(
    pattern: String!, 
    symbols: DecimalFormatSymbols!, 
    infoInput: CurrencyPluralInfo!, 
    style: Int)
```

Creates a DecimalFormat based on the given pattern and symbols, with additional control over the behavior of currency. The style argument determines whether currency rounding rules should override the pattern, and the `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo` object is used for customizing the plural forms used for currency long names.

Most users should call the factory methods on NumberFormat, such as android.icu.text.NumberFormat#getNumberInstance, which return localized formatter objects, instead of the DecimalFormat constructors.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a non-localized pattern string |
| `symbols` | [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)!: the set of symbols to be used |
| `infoInput` | [CurrencyPluralInfo](../android/icu/text/CurrencyPluralInfo.md)!: the information used for currency plural format, including currency plural patterns and plural rules. |
| --- | --- |
| `style` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the decimal formatting style, it is one of the following values: NumberFormat.NUMBERSTYLE; NumberFormat.CURRENCYSTYLE; NumberFormat.PERCENTSTYLE; NumberFormat.SCIENTIFICSTYLE; NumberFormat.INTEGERSTYLE; NumberFormat.ISOCURRENCYSTYLE; NumberFormat.PLURALCURRENCYSTYLE; |

## Public methods

### applyLocalizedPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyLocalizedPattern(localizedPattern: String!): Unit
```

Converts the given string to standard notation and then parses it using `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyPattern(kotlin.String)`. This method is provided for backwards compatibility and should not be used in new projects.

Localized notation means that instead of using generic placeholders in the pattern, you use the corresponding locale-specific characters instead. For example, in locale *fr-FR*, the period in the pattern "0.000" means "decimal" in standard notation (as it does in every other locale), but it means "grouping" in localized notation.

| Parameters ||
|---|---|
| `localizedPattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The pattern string in localized notation. |

### applyPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyPattern(pattern: String!): Unit
```

Parses the given pattern string and overwrites the settings specified in the pattern string. The properties corresponding to the following setters are overwritten, either with their default values or with the value specified in the pattern string:

1. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalSeparatorAlwaysShown(kotlin.Boolean)`
2. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setExponentSignAlwaysShown(kotlin.Boolean)`
3. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`
4. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingSize(kotlin.Int)`
5. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMultiplier(kotlin.Int)` (percent/permille)
6. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)`
7. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumIntegerDigits(kotlin.Int)`
8. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)`
9. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumExponentDigits(kotlin.Byte)`
10. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumFractionDigits(kotlin.Int)`
11. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumIntegerDigits(kotlin.Int)`
12. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumSignificantDigits(kotlin.Int)`
13. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`
14. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadCharacter(kotlin.Char)`
15. setRoundingIncrement
16. `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSecondaryGroupingSize(kotlin.Int)`

All other settings remain untouched.

<br />

For more information on pattern strings, see [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns).

### areSignificantDigitsUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun areSignificantDigitsUsed(): Boolean
```

**\[icu\]** Returns whether significant digits are being used in rounding.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSignificantDigitsUsed(kotlin.Boolean)`

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Tests for equality between this formatter and another formatter.

If two DecimalFormat instances are equal, then they will always produce the same output. However, the reverse is not necessarily true: if two DecimalFormat instances always produce the same output, they are not necessarily equal.

| Parameters ||
|---|---|
| `obj` | the object to compare against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the object is equal to this. |

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    number: BigDecimal!, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

**\[icu\]** Formats an ICU BigDecimal. Specialization of format.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    currAmt: CurrencyAmount!, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

**\[icu\]** Formats a CurrencyAmount. Specialization of format.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    number: Double, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Specialization of format.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    number: BigDecimal!, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

**\[icu\]** Formats a BigDecimal. Specialization of format.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    number: BigInteger!, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

**\[icu\]** Formats a BigInteger. Specialization of format.

### format

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun format(
    number: Long, 
    result: StringBuffer!, 
    fieldPosition: FieldPosition!
): StringBuffer!
```

Specialization of format.

### formatToCharacterIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun formatToCharacterIterator(obj: Any!): AttributedCharacterIterator!
```

Formats an Object producing an `AttributedCharacterIterator`. You can use the returned `AttributedCharacterIterator` to build the resulting String, as well as to determine information about the resulting String.

Each attribute key of the AttributedCharacterIterator will be of type `Field`. It is up to each `Format` implementation to define what the legal values are for each attribute in the `AttributedCharacterIterator`, but typically the attribute key is also used as the attribute value.

The default implementation creates an `AttributedCharacterIterator` with no attributes. Subclasses that support fields should override this and create an `AttributedCharacterIterator` with meaningful attributes.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The object to format |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/text/AttributedCharacterIterator.html#!` | AttributedCharacterIterator describing the formatted value. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when the Format cannot format the given object. |
| `java.lang.NullPointerException` | if obj is null. |

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrency(): Currency!
```

Returns the currency used to display currency amounts. May be null.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrency(android.icu.util.Currency)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols#getCurrency()`

### getCurrencyPluralInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrencyPluralInfo(): CurrencyPluralInfo!
```

**\[icu\]** Returns the current instance of CurrencyPluralInfo.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrencyPluralInfo(android.icu.text.CurrencyPluralInfo)`

### getCurrencyUsage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrencyUsage(): Currency.CurrencyUsage!
```

**\[icu\]** Returns the strategy for rounding currency amounts.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrencyUsage(android.icu.util.Currency.CurrencyUsage)`

### getDecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDecimalFormatSymbols(): DecimalFormatSymbols!
```

Returns a copy of the decimal format symbols used by this formatter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols!` | desired DecimalFormatSymbols |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols`

### getFormatWidth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFormatWidth(): Int
```

Returns the minimum number of characters in formatted output.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`

### getGroupingSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGroupingSize(): Int
```

Returns the primary grouping size in use.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingSize(kotlin.Int)`

### getMathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMathContext(): MathContext!
```

**\[icu\]** Returns the `https://developer.android.com/reference/kotlin/java/math/MathContext.html#` being used to round numbers.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)`

### getMathContextICU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMathContextICU(): MathContext!
```

**\[icu\]** Returns the `https://developer.android.com/reference/kotlin/android/icu/math/MathContext.html#` being used to round numbers.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)`

### getMaximumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaximumFractionDigits(): Int
```

Returns the effective maximum number of integer digits after the decimal separator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of fraction digits |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumIntegerDigits(kotlin.Int)`

### getMaximumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaximumIntegerDigits(): Int
```

Returns the effective maximum number of digits before the decimal separator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum number of integer digits |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumIntegerDigits(kotlin.Int)`

### getMaximumSignificantDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaximumSignificantDigits(): Int
```

**\[icu\]** Returns the effective maximum number of significant digits displayed.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)`

### getMinimumExponentDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumExponentDigits(): Byte
```

**\[icu\]** Returns the minimum number of digits printed in the exponent in scientific notation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumExponentDigits(kotlin.Byte)`

### getMinimumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumFractionDigits(): Int
```

Returns the effective minimum number of integer digits after the decimal separator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum number of fraction digits |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumIntegerDigits(kotlin.Int)`

### getMinimumGroupingDigits

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumGroupingDigits(): Int
```

**\[icu\]** Returns the minimum number of digits before grouping is triggered.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumGroupingDigits(kotlin.Int)`

### getMinimumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumIntegerDigits(): Int
```

Returns the effective minimum number of digits before the decimal separator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the minimum number of integer digits |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumIntegerDigits(kotlin.Int)`

### getMinimumSignificantDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMinimumSignificantDigits(): Int
```

**\[icu\]** Returns the effective minimum number of significant digits displayed.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumSignificantDigits(kotlin.Int)`

### getMultiplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMultiplier(): Int
```

Returns the multiplier being applied to numbers before they are formatted.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMultiplier(kotlin.Int)`

### getNegativePrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNegativePrefix(): String!
```

**Affixes:** Gets the negative prefix string currently being used to format numbers.

If the affix was specified via the pattern, the string returned by this method will have locale symbols substituted in place of special characters according to the LDML specification. If the affix was specified via `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setNegativePrefix(kotlin.String)`, the string will be returned literally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string being prepended to negative numbers. |

### getNegativeSuffix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNegativeSuffix(): String!
```

**Affixes:** Gets the negative suffix string currently being used to format numbers.

If the affix was specified via the pattern, the string returned by this method will have locale symbols substituted in place of special characters according to the LDML specification. If the affix was specified via `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setNegativeSuffix(kotlin.String)`, the string will be returned literally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string being appended to negative numbers. |

### getPadCharacter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPadCharacter(): Char
```

**\[icu\]** Returns the character used for padding.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadCharacter(kotlin.Char)`

### getPadPosition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPadPosition(): Int
```

**\[icu\]** Returns the position used for padding.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`

### getParseMaxDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParseMaxDigits(): Int
```

**Deprecated:** *Setting max parse digits has no effect since ICU4J 59.*

Always returns 1000, the default prior to ICU 59.

### getPositivePrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPositivePrefix(): String!
```

**Affixes:** Gets the positive prefix string currently being used to format numbers.

If the affix was specified via the pattern, the string returned by this method will have locale symbols substituted in place of special characters according to the LDML specification. If the affix was specified via `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPositivePrefix(kotlin.String)`, the string will be returned literally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string being prepended to positive numbers. |

### getPositiveSuffix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPositiveSuffix(): String!
```

**Affixes:** Gets the positive suffix string currently being used to format numbers.

If the affix was specified via the pattern, the string returned by this method will have locale symbols substituted in place of special characters according to the LDML specification. If the affix was specified via `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPositiveSuffix(kotlin.String)`, the string will be returned literally.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The string being appended to positive numbers. |

### getRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoundingIncrement(): BigDecimal!
```

**\[icu\]** Returns the increment to which numbers are being rounded.
**See Also**

### getRoundingMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoundingMode(): Int
```

Returns the rounding mode being used to round numbers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A rounding mode, between `BigDecimal.ROUND_UP` and `BigDecimal.ROUND_UNNECESSARY`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)`

### getSecondaryGroupingSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSecondaryGroupingSize(): Int
```

**\[icu\]** Returns the secondary grouping size in use.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSecondaryGroupingSize(kotlin.Int)`

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isDecimalPatternMatchRequired

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDecimalPatternMatchRequired(): Boolean
```

**\[icu\]** Returns whether the presence of a decimal point must match the pattern.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalPatternMatchRequired(kotlin.Boolean)`

### isDecimalSeparatorAlwaysShown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDecimalSeparatorAlwaysShown(): Boolean
```

Returns whether the decimal separator is shown on integers.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalSeparatorAlwaysShown(kotlin.Boolean)`

### isExponentSignAlwaysShown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExponentSignAlwaysShown(): Boolean
```

**\[icu\]** Returns whether the sign (plus or minus) is always printed in scientific notation.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setExponentSignAlwaysShown(kotlin.Boolean)`

### isGroupingUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isGroupingUsed(): Boolean
```

Returns whether or not grouping separators are being printed in the output.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if grouping is used |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingUsed(kotlin.Boolean)`

### isParseBigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isParseBigDecimal(): Boolean
```

Returns whether #parse will always return a BigDecimal.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseBigDecimal(kotlin.Boolean)`

### isParseCaseSensitive

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isParseCaseSensitive(): Boolean
```

**\[icu\]** Returns whether to force case (uppercase/lowercase) to match when parsing.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseNoExponent(kotlin.Boolean)`

### isParseIntegerOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isParseIntegerOnly(): Boolean
```

Returns true if this format will parse numbers as integers only. For example in the English locale, with ParseIntegerOnly true, the string "1234." would be parsed as the integer value 1234 and parsing would stop at the "." character. The decimal separator accepted by the parse operation is locale-dependent and determined by the subclass.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this will parse integers only |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseIntegerOnly(kotlin.Boolean)`

### isParseNoExponent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isParseNoExponent(): Boolean
```

**\[icu\]** Returns whether to ignore exponents when parsing.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseNoExponent(kotlin.Boolean)`

### isParseStrict

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isParseStrict(): Boolean
```

**\[icu\]** Returns whether strict parsing is in effect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if strict parsing is in effect |

### isScientificNotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isScientificNotation(): Boolean
```

**\[icu\]** Returns whether scientific (exponential) notation is enabled on this formatter.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setScientificNotation(kotlin.Boolean)`

### isSignAlwaysShown

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSignAlwaysShown(): Boolean
```

**\[icu\]** Returns whether the sign is being shown on positive numbers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the sign is shown on positive numbers and zero. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSignAlwaysShown(kotlin.Boolean)`

### parse

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parse(
    text: String!, 
    parsePosition: ParsePosition!
): Number!
```

Returns a Long if possible (e.g., within the range \[Long.MIN_VALUE, Long.MAX_VALUE\] and with no decimals); otherwise, returns another type, such as a BigDecimal, BigInteger, or Double. The return type is not guaranteed other than for the Long case.

If IntegerOnly is set, will stop at a decimal point (or equivalent; e.g., for rational numbers "1 2/3", will stop after the 1).

Does not throw an exception; if no object can be parsed, index is unchanged!

For more detail on parsing, see the "Parsing" header in the class documentation of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#`.

### parseCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseCurrency(
    text: CharSequence!, 
    parsePosition: ParsePosition!
): CurrencyAmount!
```

Parses text from the given string as a CurrencyAmount. Unlike the parse() method, this method will attempt to parse a generic currency name, searching for a match of this object's locale's currency display names, or for a 3-letter ISO currency code. This method will fail if this format is not a currency format, that is, if it does not contain the currency pattern symbol (U+00A4) in its prefix or suffix.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the text to parse |
| `pos` | input-output position; on input, the position within text to match; must have 0 \<= pos.getIndex() \< text.length(); on output, the position after the last matched character. If the parse fails, the position in unchanged upon output. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#!` | a CurrencyAmount, or null upon failure |

### setCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrency(currency: Currency!): Unit
```

Sets the currency to be used when formatting numbers. The effect is twofold:

1. Substitutions for currency symbols in the pattern string will use this currency
2. The rounding mode will obey the rules for this currency (see `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setCurrencyUsage(android.icu.util.Currency.CurrencyUsage)`)

**Important:** Displaying the currency in the output requires that the patter associated with this formatter contains a currency symbol '¤'. This will be the case if the instance was created via #getCurrencyInstance or one of its friends.

<br />

| Parameters ||
|---|---|
| `theCurrency` | new currency object to use. May be null for some subclasses. |
| `currency` | [Currency](../android/icu/util/Currency.md)!: The currency to use. |

### setCurrencyPluralInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrencyPluralInfo(newInfo: CurrencyPluralInfo!): Unit
```

**\[icu\]** Sets a custom instance of CurrencyPluralInfo. CurrencyPluralInfo generates pattern strings for printing currency long names.

**Most users should not call this method directly.** You should instead create your formatter via `NumberFormat.getInstance(NumberFormat.PLURALCURRENCYSTYLE)`.

| Parameters ||
|---|---|
| `newInfo` | [CurrencyPluralInfo](../android/icu/text/CurrencyPluralInfo.md)!: The CurrencyPluralInfo to use when printing currency long names. |

### setCurrencyUsage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrencyUsage(usage: Currency.CurrencyUsage!): Unit
```

**\[icu\]** Sets the currency-dependent strategy to use when rounding numbers. There are two strategies:

- STANDARD: When the amount displayed is intended for banking statements or electronic transfer.
- CASH: When the amount displayed is intended to be representable in physical currency, like at a cash register.

CASH mode is relevant in currencies that do not have tender down to the penny. For more information on the two rounding strategies, see [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Supplemental_Currency_Data). If omitted, the strategy defaults to STANDARD. To override currency rounding altogether, use `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumFractionDigits(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)` or #setRoundingIncrement.

<br />

| Parameters ||
|---|---|
| `usage` | [Currency.CurrencyUsage](../android/icu/util/Currency.CurrencyUsage.md)!: The strategy to use when rounding in the current currency. |

### setDecimalFormatSymbols

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecimalFormatSymbols(newSymbols: DecimalFormatSymbols!): Unit
```

Sets the decimal format symbols used by this formatter. The formatter uses a copy of the provided symbols.

| Parameters ||
|---|---|
| `newSymbols` | [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md)!: desired DecimalFormatSymbols |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols`

### setDecimalPatternMatchRequired

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecimalPatternMatchRequired(value: Boolean): Unit
```

**\[icu\]** **Parsing:** This method is used to either *require* or the presence of a decimal point in the string being parsed (disabled by default). This feature was designed to be an extra layer of strictness on top of strict parsing, although it can be used in either lenient mode or strict mode.

To *require* a decimal point, call this method in combination with either a pattern containing a decimal point or with `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalSeparatorAlwaysShown(kotlin.Boolean)`.

```kotlin
// Require a decimal point in the string being parsed:
  df.applyPattern("#.");
  df.setDecimalPatternMatchRequired(true);
 
  // Alternatively:
  df.setDecimalSeparatorAlwaysShown(true);
  df.setDecimalPatternMatchRequired(true);
  
```
To *forbid* a decimal point, call this method in combination with a pattern containing no decimal point. Alternatively, use `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseIntegerOnly(kotlin.Boolean)` for the same behavior without depending on the contents of the pattern string.

```kotlin
// Forbid a decimal point in the string being parsed:
  df.applyPattern("#");
  df.setDecimalPatternMatchRequired(true);
  
```

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to either require or forbid the decimal point according to the pattern; false to disable this feature. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setParseIntegerOnly(kotlin.Boolean)`

### setDecimalSeparatorAlwaysShown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDecimalSeparatorAlwaysShown(value: Boolean): Unit
```

**Separators:** Sets whether the decimal separator (a period in *en-US*) is shown on integers. For example, if this setting is turned on, formatting 123 will result in "123." with the decimal separator.

This setting can be specified in the pattern for integer formats: "#,##0." is an example.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to always show the decimal separator; false to show it only when there is a fraction part of the number. |

### setExponentSignAlwaysShown

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExponentSignAlwaysShown(expSignAlways: Boolean): Unit
```

**\[icu\]** **Scientific Notation:** Sets whether the sign (plus or minus) is always to be shown in the exponent in scientific notation. For example, if this setting is enabled, the number 123000 will be printed as "1.23E+5" in locale *en-US* . The number 0.0000123 will always be printed as "1.23E-5" in locale *en-US* whether or not this setting is enabled.

This setting corresponds to the '+' in a pattern such as "0.00E+0".

| Parameters ||
|---|---|
| `expSignAlways` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to always shown the sign in the exponent; false to show it for negatives but not positives. |

### setFormatWidth

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFormatWidth(width: Int): Unit
```

**Padding:** Sets the minimum width of the string output by the formatting pipeline. For example, if padding is enabled and paddingWidth is set to 6, formatting the number "3.14159" with the pattern "0.00" will result in "··3.14" if '·' is your padding string.

If the number is longer than your padding width, the number will display as if no padding width had been specified, which may result in strings longer than the padding width.

Padding can be specified in the pattern string using the '\*' symbol. For example, the format "\*x######0" has a format width of 7 and a pad character of 'x'.

Padding is currently counted in UTF-16 code units; see [ticket #13034](https://unicode-org.atlassian.net/browse/ICU-13034) for more information.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of characters in the output. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadCharacter(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setPadPosition(kotlin.Int)`

### setGroupingSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGroupingSize(width: Int): Unit
```

**Grouping:** Sets the primary grouping size (distance between grouping separators) used when formatting large numbers. For most locales, this defaults to 3: the number of digits between the ones and thousands place, between thousands and millions, and so forth.

For example, with a grouping size of 3, the number 1234567 will be formatted as "1,234,567".

Grouping size can also be specified in the pattern: for example, "#,##0" corresponds to a grouping size of 3.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The grouping size to use. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSecondaryGroupingSize(kotlin.Int)`

### setGroupingUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setGroupingUsed(enabled: Boolean): Unit
```

**Grouping:** Sets whether grouping is to be used when formatting numbers. Grouping means whether the thousands, millions, billions, and larger powers of ten should be separated by a grouping separator (a comma in *en-US*).

For example, if grouping is enabled, 12345 will be printed as "12,345" in *en-US*. If grouping were disabled, it would instead be printed as simply "12345".

| Parameters ||
|---|---|
| `newValue` | true to use grouping. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable grouping separators; false to disable them. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingSize(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setSecondaryGroupingSize(kotlin.Int)`

### setMathContext

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMathContext(mathContext: MathContext!): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Sets the `https://developer.android.com/reference/kotlin/java/math/MathContext.html#` used to round numbers. A "math context" encodes both a rounding mode and a number of significant digits. Most users should call `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)` and/or `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)` instead of this method.

When formatting, since no division is ever performed, the default MathContext is unlimited significant digits. However, when division occurs during parsing to correct for percentages and multipliers, a MathContext of 34 digits, the IEEE 754R Decimal128 standard, is used by default. If you require more than 34 digits when parsing, you can set a custom MathContext using this method.

| Parameters ||
|---|---|
| `mathContext` | [MathContext](../java/math/MathContext.md)!: The MathContext to use when rounding numbers. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when inverting multiplier produces a non-terminating decimal result in conjunction with MathContext of unlimited precision. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/math/MathContext.html#`

### setMathContextICU

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMathContextICU(mathContextICU: MathContext!): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)` for `https://developer.android.com/reference/kotlin/android/icu/math/MathContext.html#`.

| Parameters ||
|---|---|
| `mathContextICU` | [MathContext](../android/icu/math/MathContext.md)!: The MathContext to use when rounding numbers. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when inverting multiplier produces a non-terminating decimal result in conjunction with MathContext of unlimited precision. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMathContext(java.math.MathContext)`

### setMaximumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaximumFractionDigits(value: Int): Unit
```

**Rounding and Digit Limits:** Sets the maximum number of digits to display after the decimal separator. If the number has more than this many digits, the number is rounded according to the rounding mode.

For example, if maximum fraction digits is 2, the number 123.456 will be printed as "123.46".

Minimum integer and minimum and maximum fraction digits can be specified via the pattern string. For example, "#,#00.00#" has 2 minimum integer digits, 2 minimum fraction digits, and 3 maximum fraction digits. Note that it is not possible to specify maximum integer digits in the pattern except in scientific notation.

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

| Parameters ||
|---|---|
| `newValue` | the maximum number of fraction digits to be shown; if less than zero, then zero is used. The concrete subclass may enforce an upper limit to this value appropriate to the numeric type being formatted. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of integer digits after the decimal separator. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)`

### setMaximumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaximumIntegerDigits(value: Int): Unit
```

**Rounding and Digit Limits:** Sets the maximum number of digits to display before the decimal separator. If the number has more than this many digits, the number is truncated.

For example, if maximum integer digits is 3, the number 12345 will be printed as "345".

Minimum integer and minimum and maximum fraction digits can be specified via the pattern string. For example, "#,#00.00#" has 2 minimum integer digits, 2 minimum fraction digits, and 3 maximum fraction digits. Note that it is not possible to specify maximum integer digits in the pattern except in scientific notation.

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

| Parameters ||
|---|---|
| `newValue` | the maximum number of integer digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of digits before the decimal separator. |

### setMaximumSignificantDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMaximumSignificantDigits(value: Int): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Sets the maximum number of significant digits to be displayed. If the number of significant digits in the number exceeds this value, the number will be rounded according to the current rounding mode.

For example, if maximum significant digits is 3 and the number is 12345, the number will be printed as "12300".

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

See #setRoundingIncrement and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)` for two other ways of specifying rounding strategies.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of significant digits to display. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)`

### setMinimumExponentDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumExponentDigits(minExpDig: Byte): Unit
```

**\[icu\]** **Scientific Notation:** Sets the minimum number of digits to be printed in the exponent. For example, if minimum exponent digits is 3, the number 123000 will be printed as "1.23E005".

This setting corresponds to the number of zeros after the 'E' in a pattern string such as "0.00E000".

| Parameters ||
|---|---|
| `minExpDig` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html): The minimum number of digits in the exponent. |

### setMinimumFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumFractionDigits(value: Int): Unit
```

**Rounding and Digit Limits:** Sets the minimum number of digits to display after the decimal separator. If the number has fewer than this many digits, the number is padded with zeros.

For example, if minimum fraction digits is 2, the number 123.4 will be printed as "123.40".

Minimum integer and minimum and maximum fraction digits can be specified via the pattern string. For example, "#,#00.00#" has 2 minimum integer digits, 2 minimum fraction digits, and 3 maximum fraction digits. Note that it is not possible to specify maximum integer digits in the pattern except in scientific notation.

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

See #setRoundingIncrement and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)` for two other ways of specifying rounding strategies.

| Parameters ||
|---|---|
| `newValue` | the minimum number of fraction digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of integer digits after the decimal separator. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)`

### setMinimumGroupingDigits

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumGroupingDigits(number: Int): Unit
```

**\[icu\]** Sets the minimum number of digits that must be before the first grouping separator in order for the grouping separator to be printed. For example, if minimum grouping digits is set to 2, in *en-US*, 1234 will be printed as "1234" and 12345 will be printed as "12,345". Set the value to:

- 1 to turn off minimum grouping digits.
- MINIMUM_GROUPING_DIGITS_AUTO to display grouping using the default strategy for all locales.
- MINIMUM_GROUPING_DIGITS_MIN2 to display grouping using locale defaults, except do not show grouping on values smaller than 10000 (such that there is a minimum of two digits before the first separator).

<br />

| Parameters ||
|---|---|
| `number` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of digits before grouping is triggered. |

### setMinimumIntegerDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumIntegerDigits(value: Int): Unit
```

**Rounding and Digit Limits:** Sets the minimum number of digits to display before the decimal separator. If the number has fewer than this many digits, the number is padded with zeros.

For example, if minimum integer digits is 3, the number 12.3 will be printed as "001.23".

Minimum integer and minimum and maximum fraction digits can be specified via the pattern string. For example, "#,#00.00#" has 2 minimum integer digits, 2 minimum fraction digits, and 3 maximum fraction digits. Note that it is not possible to specify maximum integer digits in the pattern except in scientific notation.

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

| Parameters ||
|---|---|
| `newValue` | the minimum number of integer digits to be shown; if less than zero, then zero is used. Subclasses might enforce an upper limit to this value appropriate to the numeric type being formatted. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of digits before the decimal separator. |

### setMinimumSignificantDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMinimumSignificantDigits(value: Int): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Sets the minimum number of significant digits to be displayed. If the number of significant digits is less than this value, the number will be padded with zeros as necessary.

For example, if minimum significant digits is 3 and the number is 1.2, the number will be printed as "1.20".

If minimum and maximum integer, fraction, or significant digits conflict with each other, the most recently specified value is used. For example, if there is a formatter with minInt=5, and then you set maxInt=3, then minInt will be changed to 3.

| Parameters ||
|---|---|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The minimum number of significant digits to display. |

### setMultiplier

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMultiplier(multiplier: Int): Unit
```

Sets a number that will be used to multiply all numbers prior to formatting. For example, when formatting percents, a multiplier of 100 can be used.

If a percent or permille sign is specified in the pattern, the multiplier is automatically set to 100 or 1000, respectively.

If the number specified here is a power of 10, a more efficient code path will be used.

| Parameters ||
|---|---|
| `multiplier` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number by which all numbers passed to #format will be multiplied. |

| Exceptions ||
|---|---|
| `java.lang.ArithmeticException` | when inverting multiplier produces a non-terminating decimal result in conjunction with MathContext of unlimited precision. |
| `java.lang.IllegalArgumentException` | If the given multiplier is zero. |

### setNegativePrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNegativePrefix(prefix: String!): Unit
```

**Affixes:** Sets the string to prepend to negative numbers. For example, if you set the value "#", then the number -123 will be formatted as "#123" in the locale *en-US* (overriding the implicit default '-' in the pattern).

Using this method overrides the affix specified via the pattern, and unlike the pattern, the string given to this method will be interpreted literally WITHOUT locale symbol substitutions.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The literal string to prepend to negative numbers. |

### setNegativeSuffix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNegativeSuffix(suffix: String!): Unit
```

**Affixes:** Sets the string to append to negative numbers. For example, if you set the value "#", then the number 123 will be formatted as "123#" in the locale *en-US*.

Using this method overrides the affix specified via the pattern, and unlike the pattern, the string given to this method will be interpreted literally WITHOUT locale symbol substitutions.

| Parameters ||
|---|---|
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The literal string to append to negative numbers. |

### setPadCharacter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPadCharacter(padChar: Char): Unit
```

**\[icu\]** **Padding:** Sets the character used to pad numbers that are narrower than the width specified in `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`.

In the pattern string, the padding character is the token that follows '\*' before or after the prefix or suffix.

| Parameters ||
|---|---|
| `padChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): The character used for padding. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`

### setPadPosition

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPadPosition(padPos: Int): Unit
```

**\[icu\]** **Padding:** Sets the position where to insert the pad character when narrower than the width specified in `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`. For example, consider the pattern "P123S" with padding width 8 and padding char "\*". The four positions are:

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_PREFIX:kotlin.Int` ⇒ "\*\*\*P123S"
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_PREFIX:kotlin.Int` ⇒ "P\*\*\*123S"
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_BEFORE_SUFFIX:kotlin.Int` ⇒ "P123\*\*\*S"
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#PAD_AFTER_SUFFIX:kotlin.Int` ⇒ "P123S\*\*\*"

<br />

| Parameters ||
|---|---|
| `padPos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position used for padding. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setFormatWidth(kotlin.Int)`

### setParseBigDecimal

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseBigDecimal(value: Boolean): Unit
```

Whether to make #parse prefer returning a `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#` when possible. For strings corresponding to return values of Infinity, -Infinity, NaN, and -0.0, a Double will be returned even if ParseBigDecimal is enabled.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to cause #parse to prefer BigDecimal; false to let #parse return additional data types like Long or BigInteger. |

### setParseCaseSensitive

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseCaseSensitive(value: Boolean): Unit
```

**\[icu\]** Specifies whether parsing should require cases to match in affixes, exponent separators, and currency codes. Case mapping is performed for each code point using android.icu.lang.UCharacter#foldCase.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to force case (uppercase/lowercase) to match when parsing; false to ignore case and perform case folding. |

### setParseIntegerOnly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseIntegerOnly(parseIntegerOnly: Boolean): Unit
```

**Parsing:** Sets whether to ignore the fraction part of a number when parsing (defaults to false). If a string contains a decimal point, parsing will stop before the decimal point. Note that determining whether a character is a decimal point depends on the locale.

For example, in *en-US*, parsing the string "123.45" will return the number 123 and parse position 3.

This is functionally equivalent to calling `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setDecimalPatternMatchRequired(kotlin.Boolean)` and a pattern without a decimal point.

| Parameters ||
|---|---|
| `value` | true if this should parse integers only |
| `parseIntegerOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to ignore fractional parts of numbers when parsing; false to consume fractional parts. |

### setParseMaxDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseMaxDigits(maxDigits: Int): Unit
```

**Deprecated:** *Setting max parse digits has no effect since ICU4J 59.*

| Parameters ||
|---|---|
| `maxDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Prior to ICU 59, the maximum number of digits in the output number after exponential notation is applied. |

### setParseNoExponent

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseNoExponent(value: Boolean): Unit
```

**\[icu\]** Specifies whether to stop parsing when an exponent separator is encountered. For example, parses "123E4" to 123 (with parse position 3) instead of 1230000 (with parse position 5).

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to prevent exponents from being parsed; false to allow them to be parsed. |

### setParseStrict

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParseStrict(parseStrict: Boolean): Unit
```

**\[icu\]** Sets whether strict parsing is in effect. When this is true, the string is required to be a stronger match to the pattern than when lenient parsing is in effect. More specifically, the following conditions cause a parse failure relative to lenient mode (examples use the pattern "#,##0.#"):

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
|---|---|
| `value` | True to enable strict parsing. Default is false. |

### setPositivePrefix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPositivePrefix(prefix: String!): Unit
```

**Affixes:** Sets the string to prepend to positive numbers. For example, if you set the value "#", then the number 123 will be formatted as "#123" in the locale *en-US*.

Using this method overrides the affix specified via the pattern, and unlike the pattern, the string given to this method will be interpreted literally WITHOUT locale symbol substitutions.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The literal string to prepend to positive numbers. |

### setPositiveSuffix

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPositiveSuffix(suffix: String!): Unit
```

**Affixes:** Sets the string to append to positive numbers. For example, if you set the value "#", then the number 123 will be formatted as "123#" in the locale *en-US*.

Using this method overrides the affix specified via the pattern, and unlike the pattern, the string given to this method will be interpreted literally WITHOUT locale symbol substitutions.

| Parameters ||
|---|---|
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The literal string to append to positive numbers. |

### setRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRoundingIncrement(increment: BigDecimal!): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(java.math.BigDecimal)`.

| Parameters ||
|---|---|
| `increment` | [BigDecimal](../android/icu/math/BigDecimal.md)!: The increment to which numbers are to be rounded. |

**See Also**

### setRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRoundingIncrement(increment: Double): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Overload of `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingIncrement(java.math.BigDecimal)`.

| Parameters ||
|---|---|
| `increment` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): The increment to which numbers are to be rounded. |

**See Also**

### setRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRoundingIncrement(increment: BigDecimal!): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Sets an increment, or interval, to which numbers are rounded. For example, a rounding increment of 0.05 will cause the number 1.23 to be rounded to 1.25 in the default rounding mode.

The rounding increment can be specified via the pattern string: for example, the pattern "#,##0.05" encodes a rounding increment of 0.05.

The rounding increment is applied *after* any multipliers might take effect; for example, in scientific notation or when `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMultiplier(kotlin.Int)` is used.

See `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)` for two other ways of specifying rounding strategies.

| Parameters ||
|---|---|
| `increment` | [BigDecimal](../java/math/BigDecimal.md)!: The increment to which numbers are to be rounded. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setRoundingMode(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumFractionDigits(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMaximumSignificantDigits(kotlin.Int)`

### setRoundingMode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRoundingMode(roundingMode: Int): Unit
```

**Rounding and Digit Limits:** Sets the `https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#` used to round numbers. The default rounding mode is HALF_EVEN, which rounds decimals to their closest whole number, and rounds to the closest even number if at the midpoint.

For more detail on rounding modes, see [the ICU User Guide](https://unicode-org.github.io/icu/userguide/format_parse/numbers/rounding-modes).

For backwards compatibility, the rounding mode is specified as an int argument, which can be from either the constants in `https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#` or the ordinal value of `https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#`. The following two calls are functionally equivalent.

```kotlin
df.setRoundingMode(BigDecimal.ROUND_CEILING);
  df.setRoundingMode(RoundingMode.CEILING.ordinal());
  
```

| Parameters ||
|---|---|
| `roundingMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The integer constant rounding mode to use when formatting numbers. |

### setScientificNotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setScientificNotation(useScientific: Boolean): Unit
```

**\[icu\]** **Scientific Notation:** Sets whether this formatter should print in scientific (exponential) notation. For example, if scientific notation is enabled, the number 123000 will be printed as "1.23E5" in locale *en-US*. A locale-specific symbol is used as the exponent separator.

Calling `df.setScientificNotation(true)` is functionally equivalent to calling `df.setMinimumExponentDigits(1)`.

| Parameters ||
|---|---|
| `useScientific` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable scientific notation; false to disable it. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setMinimumExponentDigits(kotlin.Byte)`

### setSecondaryGroupingSize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSecondaryGroupingSize(width: Int): Unit
```

**\[icu\]** **Grouping:** Sets the secondary grouping size (distance between grouping separators after the first separator) used when formatting large numbers. In many south Asian locales, this is set to 2.

For example, with primary grouping size 3 and secondary grouping size 2, the number 1234567 will be formatted as "12,34,567".

Grouping size can also be specified in the pattern: for example, "#,##,##0" corresponds to a primary grouping size of 3 and a secondary grouping size of 2.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The secondary grouping size to use. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#setGroupingSize(kotlin.Int)`

### setSignAlwaysShown

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSignAlwaysShown(value: Boolean): Unit
```

Sets whether to always shown the plus sign ('+' in *en*) on positive numbers. The rules in UTS #35 section 3.2.1 will be followed to ensure a locale-aware placement of the sign.

More specifically, the following strategy will be used to place the plus sign:

1. *Patterns without a negative subpattern:* The locale's plus sign will be prepended to the positive prefix.
2. *Patterns with a negative subpattern without a '-' sign (e.g., accounting):* The locale's plus sign will be prepended to the positive prefix, as in case 1.
3. *Patterns with a negative subpattern that has a '-' sign:* The locale's plus sign will substitute the '-' in the negative subpattern. The positive subpattern will be unused.

This method is designed to be used *instead of* applying a pattern containing an explicit plus sign, such as "+0;-0". The behavior when combining this method with explicit plus signs in the pattern is undefined.

| Parameters ||
|---|---|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to always show a sign; false to hide the sign on positive numbers and zero. |

### setSignificantDigitsUsed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSignificantDigitsUsed(useSignificantDigits: Boolean): Unit
```

**\[icu\]** **Rounding and Digit Limits:** Sets whether significant digits are to be used in rounding.

Calling `df.setSignificantDigitsUsed(true)` is functionally equivalent to:

```kotlin
df.setMinimumSignificantDigits(1);
  df.setMaximumSignificantDigits(6);
  
```

| Parameters ||
|---|---|
| `useSignificantDigits` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true to enable significant digit rounding; false to disable it. |

### toLocalizedPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLocalizedPattern(): String!
```

Calls `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#toPattern()` and converts the string to localized notation. For more information on localized notation, see `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyLocalizedPattern(kotlin.String)`. This method is provided for backwards compatibility and should not be used in new projects.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A decimal format pattern string in localized notation. |

### toPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toPattern(): String!
```

Serializes this formatter object to a decimal format pattern string. The result of this method is guaranteed to be *functionally* equivalent to the pattern string used to create this instance after incorporating values from the setter methods.

For more information on decimal format pattern strings, see [UTS #35](http://unicode.org/reports/tr35/tr35-numbers.html#Number_Format_Patterns).

**Important:** Not all properties are capable of being encoded in a pattern string. See a list of properties in `https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat#applyPattern(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | A decimal format pattern string. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the default value of toString() with extra DecimalFormat-specific information appended to the end of the string. This extra information is intended for debugging purposes, and the format is not guaranteed to be stable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
