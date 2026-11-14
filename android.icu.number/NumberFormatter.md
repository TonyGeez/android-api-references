# NumberFormatter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberFormatter

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/NumberFormatter "View this page in Java") 
| --- | --- |

```
class NumberFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter#) |

All-in-one formatter for localized numbers, currencies, and units. For a full list of options, see [NumberFormatterSettings](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatterSettings). 

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

This API offers more features than [android.icu.text.DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat.html#) and is geared toward new users of ICU.

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
| | [DecimalSeparatorDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.DecimalSeparatorDisplay) An enum declaring how to render the decimal separator. |
| | [GroupingStrategy](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.GroupingStrategy) An enum declaring the strategy for when and how to display grouping separators (i.e., the separator, often a comma or period, after every 2-3 powers of ten). |
| | [RoundingPriority](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.RoundingPriority) An enum declaring how to resolve conflicts between maximum fraction digits and maximum significant digits. |
| --- | --- |
| | [SignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.SignDisplay) An enum declaring how to denote positive and negative numbers. |
| | [TrailingZeroDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.TrailingZeroDisplay) An enum declaring how to render trailing zeros. |
| | [UnitWidth](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.UnitWidth) An enum declaring how to render units, including currencies. |
| --- | --- |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)! | [with](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter#with())`()` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is not currently known at the call site. |
| static [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter)! | [withLocale](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter#withLocale(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site. |
| static [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter)! | [withLocale](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter#withLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site. |
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
| [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter)! | An [UnlocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberFormatter), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun withLocale(locale: ULocale!): LocalizedNumberFormatter!
```

Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale from which to load formats and symbols for number formatting. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter)! | A [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun withLocale(locale: Locale!): LocalizedNumberFormatter!
```

Call this method at the beginning of a NumberFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The locale from which to load formats and symbols for number formatting. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter)! | A [LocalizedNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberFormatter), to be used for chaining. |
