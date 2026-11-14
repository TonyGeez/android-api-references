# LocalizedNumberFormatter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LocalizedNumberFormatter

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/LocalizedNumberFormatter "View this page in Java") 
| --- | --- |

```
open class LocalizedNumberFormatter : NumberFormatterSettings<LocalizedNumberFormatter!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.number.NumberFormatterSettings](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings)\< [android.icu.number.LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#)\> ||
| | ↳ | [android.icu.number.LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#) |

A NumberFormatter that has a locale associated with it; this means .format() methods are available. Instances of this class are immutable and thread-safe.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | [format](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#format(android.icu.util.Measure))`(`input:` ` [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure.html#)!`)` Format the given [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure.html#) or [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#) to a string using the settings specified in the NumberFormatter fluent setting chain. |
| open [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | [format](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#format(kotlin.Double))`(`input:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Format the given float or double to a string using the settings specified in the NumberFormatter fluent setting chain. |
| open [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | [format](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#format(kotlin.Number))`(`input:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`)` Format the given [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#), [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#), or other [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) to a string using the settings specified in the NumberFormatter fluent setting chain. |
| --- | --- |
| open [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | [format](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#format(kotlin.Long))`(`input:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Format the given byte, short, int, or long to a string using the settings specified in the NumberFormatter fluent setting chain. |
| open [Format](https://developer.android.com/reference/kotlin/java/text/Format.html#)! | [toFormat](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#toFormat())`()` Creates a representation of this LocalizedNumberFormat as a [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#), enabling the use of this number formatter with APIs that need an object of that type, such as MessageFormat. |
| open [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)! | [withoutLocale](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#withoutLocale())`()` Disassociate the locale from this formatter. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [NumberFormatterSettings](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | T | [decimal](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#decimal(android.icu.number.NumberFormatter.DecimalSeparatorDisplay))`(`style:` ` [NumberFormatter.DecimalSeparatorDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.DecimalSeparatorDisplay)!`)` <br /> Sets the decimal separator display strategy. This affects integer numbers with no fraction part. Most common values: - Auto: "1" - Always: "1." <br /> Pass an element from the [DecimalSeparatorDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.DecimalSeparatorDisplay) enum to this setter. For example: ```kotlin NumberFormatter.with().decimal(DecimalSeparatorDisplay.ALWAYS) ``` The default is AUTO decimal separator display. <br /> | | T | [displayOptions](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#displayOptions(android.icu.text.DisplayOptions))`(`displayOptions:` ` [DisplayOptions](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions.html#)!`)` <br /> Specifies the`DisplayOptions`. For example,`GrammaticalCase`specifies the desired case for a unit formatter's output (e.g. accusative, dative, genitive). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Indicates whether some other object is "equal to" this one. The`equals`method implements an equivalence relation on non-null object references: - It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`. - It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`. - It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`. - It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified. - For any non-null reference value`x`,`x.equals(null)`should return`false`. An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes. <br /> | | T | [grouping](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#grouping(android.icu.number.NumberFormatter.GroupingStrategy))`(`strategy:` ` [NumberFormatter.GroupingStrategy](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.GroupingStrategy)!`)` <br /> Specifies the grouping strategy to use when formatting numbers. - Default grouping: "12,300" and "1,230" - Grouping with at least 2 digits: "12,300" and "1230" - No grouping: "12300" and "1230" <br /> The exact grouping widths will be chosen based on the locale. Pass this method an element from the [GroupingStrategy](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.GroupingStrategy) enum. For example: ```kotlin NumberFormatter.with().grouping(GroupingStrategy.MIN2) ``` The default is to perform grouping according to locale data; most locales, but not all locales, enable it by default. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#hashCode())`()` <br /> Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#). The general contract of`hashCode`is: - Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application. - If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result. - It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables. <br /> | | T | [integerWidth](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#integerWidth(android.icu.number.IntegerWidth))`(`style:` ` [IntegerWidth](https://developer.android.com/reference/kotlin/android/icu/number/IntegerWidth)!`)` <br /> Specifies the minimum and maximum number of digits to render before the decimal mark. - Zero minimum integer digits: ".08" - One minimum integer digit: "0.08" - Two minimum integer digits: "00.08" <br /> Pass this method the return value of [IntegerWidth.zeroFillTo(int)](https://developer.android.com/reference/kotlin/android/icu/number/IntegerWidth#zeroFillTo(kotlin.Int)). For example: ```kotlin NumberFormatter.with().integerWidth(IntegerWidth.zeroFillTo(2)) ``` The default is to have one minimum integer digit. <br /> | | T | [notation](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#notation(android.icu.number.Notation))`(`notation:` ` [Notation](https://developer.android.com/reference/kotlin/android/icu/number/Notation)!`)` <br /> Specifies the notation style (simple, scientific, or compact) for rendering numbers. - Simple notation: "12,300" - Scientific notation: "1.23E4" - Compact notation: "12K" <br /> All notation styles will be properly localized with locale data, and all notation styles are compatible with units, rounding strategies, and other number formatter settings. Pass this method the return value of a [Notation](https://developer.android.com/reference/kotlin/android/icu/number/Notation) factory method. For example: ```kotlin NumberFormatter.with().notation(Notation.compactShort()) ``` The default is to use simple notation. <br /> | | T | [perUnit](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#perUnit(android.icu.util.MeasureUnit))`(`perUnit:` ` [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#)!`)` <br /> Sets a unit to be used in the denominator. For example, to format "3 m/s", pass METER to the unit and SECOND to the perUnit. Pass this method any instance of [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#). For example: ```kotlin NumberFormatter.with().unit(MeasureUnit.METER).perUnit(MeasureUnit.SECOND) ``` The default is not to display any unit in the denominator. If a per-unit is specified without a primary unit via [unit](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#unit(android.icu.util.MeasureUnit)), the behavior is undefined. <br /> | | T | [precision](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#precision(android.icu.number.Precision))`(`precision:` ` [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision)!`)` <br /> Specifies the rounding precision to use when formatting numbers. - Round to 3 decimal places: "3.142" - Round to 3 significant figures: "3.14" - Round to the closest nickel: "3.15" - Do not perform rounding: "3.1415926..." <br /> Pass this method the return value of one of the factory methods on [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision). For example: ```kotlin NumberFormatter.with().precision(Precision.fixedFraction(2)) ``` In most cases, the default rounding precision is to round to 6 fraction places; i.e.,`Precision.maxFraction(6)`. The exceptions are if compact notation is being used, then the compact notation rounding precision is used (see [Notation.compactShort](https://developer.android.com/reference/kotlin/android/icu/number/Notation#compactShort())for details), or if the unit is a currency, then standard currency rounding is used, which varies from currency to currency (see [Precision.currency](https://developer.android.com/reference/kotlin/android/icu/number/Precision#currency(android.icu.util.Currency.CurrencyUsage))for details). <br /> | | T | [roundingMode](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#roundingMode(java.math.RoundingMode))`(`roundingMode:` ` [RoundingMode](https://developer.android.com/reference/kotlin/java/math/RoundingMode.html#)!`)` <br /> Specifies how to determine the direction to round a number when it has more digits than fit in the desired precision. When formatting 1.235: - Ceiling rounding mode with integer precision: "2" - Half-down rounding mode with 2 fixed fraction digits: "1.23" - Half-up rounding mode with 2 fixed fraction digits: "1.24" The default is HALF_EVEN. For more information on rounding mode, see the ICU userguide here: https://unicode-org.github.io/icu/userguide/format_parse/numbers/rounding-modes <br /> <br /> | | T | [scale](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#scale(android.icu.number.Scale))`(`scale:` ` [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale)!`)` <br /> Sets a scale (multiplier) to be used to scale the number by an arbitrary amount before formatting. Most common values: - Multiply by 100: useful for percentages. - Multiply by an arbitrary value: useful for unit conversions. <br /> Pass an element from a [Scale](https://developer.android.com/reference/kotlin/android/icu/number/Scale) factory method to this setter. For example: ```kotlin NumberFormatter.with().scale(Scale.powerOfTen(2)) ``` The default is to not apply any multiplier. <br /> | | T | [sign](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#sign(android.icu.number.NumberFormatter.SignDisplay))`(`style:` ` [NumberFormatter.SignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.SignDisplay)!`)` <br /> Sets the plus/minus sign display strategy. Most common values: - Auto: "123", "-123" - Always: "+123", "-123" - Accounting: "$123", "($123)" <br /> Pass an element from the [SignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.SignDisplay) enum to this setter. For example: ```kotlin NumberFormatter.with().sign(SignDisplay.ALWAYS) ``` The default is AUTO sign display. <br /> | | T | [symbols](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#symbols(android.icu.text.DecimalFormatSymbols))`(`symbols:` ` [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols.html#)!`)` <br /> Specifies the symbols (decimal separator, grouping separator, percent sign, numerals, etc.) to use when rendering numbers. - *en_US*symbols: "12,345.67" - *fr_FR*symbols: "12 345,67" - *de_CH*symbols: "12'345.67" - *my_MY*symbols: "၁၂,၃၄၅.၆၇" <br /> Pass this method an instance of [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols.html#). For example: ```kotlin NumberFormatter.with().symbols(DecimalFormatSymbols.getInstance(new ULocale("de_CH"))) ``` **Note:**DecimalFormatSymbols automatically chooses the best numbering system based on the locale. In the examples above, the first three are using the Latin numbering system, and the fourth is using the Myanmar numbering system. **Note:**The instance of DecimalFormatSymbols will be copied: changes made to the symbols object after passing it into the fluent chain will not be seen. **Note:** Calling this method will override the NumberingSystem previously specified in [symbols(android.icu.text.NumberingSystem)](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#symbols(android.icu.text.NumberingSystem)). The default is to choose the symbols based on the locale specified in the fluent chain. <br /> | | T | [symbols](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#symbols(android.icu.text.NumberingSystem))`(`ns:` ` [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem.html#)!`)` <br /> Specifies that the given numbering system should be used when fetching symbols. - Latin numbering system: "12,345" - Myanmar numbering system: "၁၂,၃၄၅" - Math Sans Bold numbering system: "𝟭𝟮,𝟯𝟰𝟱" <br /> Pass this method an instance of [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem.html#). For example, to force the locale to always use the Latin alphabet numbering system (ASCII digits): ```kotlin NumberFormatter.with().symbols(NumberingSystem.LATIN) ``` **Note:** Calling this method will override the DecimalFormatSymbols previously specified in [symbols(android.icu.text.DecimalFormatSymbols)](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#symbols(android.icu.text.DecimalFormatSymbols)). The default is to choose the best numbering system for the locale. <br /> | | T | [unit](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#unit(android.icu.util.MeasureUnit))`(`unit:` ` [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#)!`)` <br /> Specifies the unit (unit of measure, currency, or percent) to associate with rendered numbers. - Unit of measure: "12.3 meters" - Currency: "$12.30" - Percent: "12.3%" <br /> **Note:** The unit can also be specified by passing a [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure.html#) to [LocalizedNumberFormatter.format(Measure)](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter#format(android.icu.util.Measure)). Units specified via the format method take precedence over units specified here. This setter is designed for situations when the unit is constant for the duration of the number formatting process. All units will be properly localized with locale data, and all units are compatible with notation styles, rounding strategies, and other number formatter settings. Pass this method any instance of [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.html#). For units of measure: ```kotlin NumberFormatter.with().unit(MeasureUnit.METER) ``` Currency: ```kotlin NumberFormatter.with().unit(Currency.getInstance("USD")) ``` See [perUnit](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#perUnit(android.icu.util.MeasureUnit))for information on how to format strings like "5 meters per second". If the input usage is correctly set the output unit**will change** according to`usage`,`locale`and`unit`value. <br /> | | T | [unitWidth](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#unitWidth(android.icu.number.NumberFormatter.UnitWidth))`(`style:` ` [NumberFormatter.UnitWidth](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.UnitWidth)!`)` <br /> Sets the width of the unit (measure unit or currency). Most common values: - Short: "$12.00", "12 m" - ISO Code: "USD 12.00" - Full name: "12.00 US dollars", "12 meters" <br /> Pass an element from the [UnitWidth](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.UnitWidth) enum to this setter. For example: ```kotlin NumberFormatter.with().unitWidth(UnitWidth.FULL_NAME) ``` The default is the SHORT width. <br /> | | T | [usage](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings#usage(kotlin.String))`(`usage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Specifies the usage for which numbers will be formatted ("person-height", "road", "rainfall", etc.) When a`usage`is specified, the output unit will change depending on the`Locale`and the unit quantity. For example, formatting length measurements specified in meters: ```kotlin NumberFormatter.with().usage("person").unit(MeasureUnit.METER).locale(new ULocale("en-US")) ``` - When formatting 0.25, the output will be "10 inches". - When formatting 1.50, the output will be "4 feet and 11 inches". The input unit specified via unit() determines the type of measurement being formatted (e.g. "length" when the unit is "foot"). The usage requested will be looked for only within this category of measurement units. The output unit can be found via FormattedNumber.getOutputUnit(). If the usage has multiple parts (e.g. "land-agriculture-grain") and does not match a known usage preference, the last part will be dropped repeatedly until a match is found (e.g. trying "land-agriculture", then "land"). If a match is still not found, usage will fall back to "default". Setting usage to an empty string clears the usage (disables usage-based localized formatting). Setting a usage string but not a correct input unit will result in an U_ILLEGAL_ARGUMENT_ERROR. When using usage, specifying rounding or precision is unnecessary. Specifying a precision in some manner will override the default formatting. <br /> | ||

## Public methods

### format

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(input: Measure!): FormattedNumber!
```

Format the given [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure.html#) or [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount.html#) to a string using the settings specified in the NumberFormatter fluent setting chain.

The unit specified here overrides any unit that may have been specified in the setter chain. This method is intended for cases when each input to the number formatter has a different unit.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `input` | [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure.html#)!:The number to format. |

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | A FormattedNumber object; call .toString() to get the string. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### format

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(input: Double): FormattedNumber!
```

Format the given float or double to a string using the settings specified in the NumberFormatter fluent setting chain.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):The number to format. |

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | A FormattedNumber object; call .toString() to get the string. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### format

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(input: Number!): FormattedNumber!
```

Format the given [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#), [BigDecimal](https://developer.android.com/reference/kotlin/android/icu/math/BigDecimal.html#), or other [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#) to a string using the settings specified in the NumberFormatter fluent setting chain.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `input` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:The number to format. |

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | A FormattedNumber object; call .toString() to get the string. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### format

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun format(input: Long): FormattedNumber!
```

Format the given byte, short, int, or long to a string using the settings specified in the NumberFormatter fluent setting chain.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `input` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The number to format. |

| Return ||
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [FormattedNumber](https://developer.android.com/reference/kotlin/android/icu/number/FormattedNumber)! | A FormattedNumber object; call .toString() to get the string. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### toFormat

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFormat(): Format!
```

Creates a representation of this LocalizedNumberFormat as a [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#), enabling the use of this number formatter with APIs that need an object of that type, such as MessageFormat.

This API is not intended to be used other than for enabling API compatibility. The #format methods should normally be used when formatting numbers, not the Format object returned by this method.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------|
| [Format](https://developer.android.com/reference/kotlin/java/text/Format.html#)! | A Format wrapping this LocalizedNumberFormatter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### withoutLocale

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withoutLocale(): UnlocalizedNumberFormatter!
```

Disassociate the locale from this formatter.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|-------------------|
| [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)! | The fluent chain. |
