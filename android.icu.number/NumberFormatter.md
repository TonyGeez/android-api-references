# NumberFormatter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberFormatter

Kotlin| [Java](../android/icu/number/NumberFormatter.md) 
| --- | --- |

```
class NumberFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.NumberFormatter](../android/icu/number/NumberFormatter.md) |

All-in-one formatter for localized numbers, currencies, and units. For a full list of options, see [NumberFormatterSettings](../android/icu/number/NumberFormatterSettings.md). 

```kotlin
// Most basic usage:
  NumberFormatter.withLocale(...).format(123).toString();  // 1,234 in en-US
 
  // Custom notation, unit, and rounding strategy:
  NumberFormatter.with()
      .notation(Notation.compactShort())
      .unit(Currency.getInstance("EUR"))
      .precision(Precision.maxDigits(2))
      .locale(...)
      .format(1234)
      .toString();  // €1.2K in en-US
 
  // Create a formatter in a private static final field:
  private static final LocalizedNumberFormatter formatter = NumberFormatter.withLocale(...)
      .unit(NoUnit.PERCENT)
      .precision(Precision.fixedFraction(3));
  formatter.format(5.9831).toString();  // 5.983% in en-US
 
  // Create a "template" in a private static final field but without setting a locale until the call site:
  private static final UnlocalizedNumberFormatter template = NumberFormatter.with()
      .sign(SignDisplay.ALWAYS)
      .unitWidth(UnitWidth.FULL_NAME);
  template.locale(...).format(new Measure(1234, MeasureUnit.METER)).toString();  // +1,234 meters in en-US
  
```

<br />

This API offers more features than [android.icu.text.DecimalFormat](../android/icu/text/DecimalFormat.md) and is geared toward new users of ICU.

NumberFormatter instances (i.e., LocalizedNumberFormatter and UnlocalizedNumberFormatter) are immutable and thread safe. This means that invoking a configuration method has no effect on the receiving instance; you must store and use the new number formatter instance it returns instead. 

```kotlin
UnlocalizedNumberFormatter formatter = UnlocalizedNumberFormatter.with()
          .notation(Notation.scientific());
  formatter.precision(Precision.maxFraction(2)); // does nothing!
  formatter.locale(ULocale.ENGLISH).format(9.8765).toString(); // prints "9.8765E0", not "9.88E0"
  
```

This API is based on the*fluent* design pattern popularized by libraries such as Google's Guava. For extensive details on the design of this API, read [the design doc](https://goo.gl/szi5VB).

Note: To format monetary/currency values, specify the currency in the \`.unit()\` function.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DecimalSeparatorDisplay](../android/icu/number/NumberFormatter.DecimalSeparatorDisplay.md) An enum declaring how to render the decimal separator. |
| | [GroupingStrategy](../android/icu/number/NumberFormatter.GroupingStrategy.md) An enum declaring the strategy for when and how to display grouping separators (i.e., the separator, often a comma or period, after every 2-3 powers of ten). |
| | [RoundingPriority](../android/icu/number/NumberFormatter.RoundingPriority.md) An enum declaring how to resolve conflicts between maximum fraction digits and maximum significant digits. |
| --- | --- |
| | [SignDisplay](../android/icu/number/NumberFormatter.SignDisplay.md) An enum declaring how to denote positive and negative numbers. |
| | [TrailingZeroDisplay](../android/icu/number/NumberFormatter.TrailingZeroDisplay.md) An enum declaring how to render trailing zeros. |
| | [UnitWidth](../android/icu/number/NumberFormatter.UnitWidth.md) An enum declaring how to render units, including currencies. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md)! | [with](../android/icu/number/NumberFormatter.md))`()` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is not currently known at the call site. |
| static [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md)! | [withLocale](../android/icu/number/NumberFormatter.md))`(`locale:` ` [ULocale](../android/icu/util/ULocale.md)!`)` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site. |
| static [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md)! | [withLocale](../android/icu/number/NumberFormatter.md))`(`locale:` ` [Locale](../java/util/Locale.md)!`)` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site. |
| --- | --- |

## Public methods

### with

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun with(): UnlocalizedNumberFormatter!
```

Call this method at the beginning of a NumberFormatter fluent chain in which the locale is not currently known at the call site.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md)! | An [UnlocalizedNumberFormatter](../android/icu/number/UnlocalizedNumberFormatter.md), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun withLocale(locale: ULocale!): LocalizedNumberFormatter!
```

Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android/icu/util/ULocale.md)!:The locale from which to load formats and symbols for number formatting. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md)! | A [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun withLocale(locale: Locale!): LocalizedNumberFormatter!
```

Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](../java/util/Locale.md)!:The locale from which to load formats and symbols for number formatting. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md)! | A [LocalizedNumberFormatter](../android/icu/number/LocalizedNumberFormatter.md), to be used for chaining. |
