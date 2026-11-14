# NumberRangeFormatter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberRangeFormatter

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/NumberRangeFormatter "View this page in Java") 
| --- | --- |

```
abstract class NumberRangeFormatter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.NumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter#) |

The main entrypoint to the formatting of ranges of numbers, including currencies and other units of measurement.

Usage example: 

```kotlin
NumberRangeFormatter.with()
          .identityFallback(RangeIdentityFallback.APPROXIMATELY_OR_SINGLE_VALUE)
          .numberFormatterFirst(NumberFormatter.with().unit(MeasureUnit.METER))
          .numberFormatterSecond(NumberFormatter.with().unit(MeasureUnit.KILOMETER))
          .locale(ULocale.UK)
          .formatRange(750, 1.2)
          .toString();
  // => "750 m - 1.2 km"
  
```

Like NumberFormatter, NumberRangeFormatter instances (i.e., LocalizedNumberRangeFormatter and UnlocalizedNumberRangeFormatter) are immutable and thread-safe. This API is based on the*fluent*design pattern popularized by libraries such as Google's Guava.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [RangeCollapse](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeCollapse) Defines how to merge fields that are identical across the range sign. |
| | [RangeIdentityFallback](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeIdentityFallback) Defines the behavior when the two numbers in the range are identical after rounding. |
| | [RangeIdentityResult](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter.RangeIdentityResult) Used in the result class FormattedNumberRange to indicate to the user whether the numbers formatted in the range were equal or not, and whether or not the identity fallback was applied. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter)! | [with](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter#with())`()` Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is not currently known at the call site. |
| openstatic [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter)! | [withLocale](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter#withLocale(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!`)` Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is known at the call site. |
| openstatic [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter)! | [withLocale](https://developer.android.com/reference/kotlin/android/icu/number/NumberRangeFormatter#withLocale(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is known at the call site. |
| --- | --- |

## Public methods

### with

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun with(): UnlocalizedNumberRangeFormatter!
```

Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is not currently known at the call site.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter)! | An [UnlocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/UnlocalizedNumberRangeFormatter), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withLocale(locale: ULocale!): LocalizedNumberRangeFormatter!
```

Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)!:The locale from which to load formats and symbols for number range formatting. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter)! | A [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter), to be used for chaining. |

### withLocale

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun withLocale(locale: Locale!): LocalizedNumberRangeFormatter!
```

Call this method at the beginning of a NumberRangeFormatter fluent chain in which the locale is known at the call site.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:The locale from which to load formats and symbols for number range formatting. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter)! | A [LocalizedNumberRangeFormatter](https://developer.android.com/reference/kotlin/android/icu/number/LocalizedNumberRangeFormatter), to be used for chaining. |
