Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FractionPrecision

Kotlin | [Java](FractionPrecision.md)
| --- | --- |

```
abstract class FractionPrecision : Precision
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.number.Precision](Precision.md) ||
| | ↳ | [android.icu.number.FractionPrecision](FractionPrecision.md) |

A class that defines a rounding strategy based on a number of fraction places and optionally significant digits to be used when formatting numbers in NumberFormatter.

To create a FractionPrecision, use one of the factory methods on Precision.

## Summary

| Public methods ||
|---|---|
| open [Precision](Precision.md)! | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#withMaxDigits(kotlin.Int)(maxSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ensure that no more than this number of significant digits are retained when rounding according to fraction rules. |
| open [Precision](Precision.md)! | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#withMinDigits(kotlin.Int)(minSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ensure that no less than this number of significant digits are retained when rounding according to fraction rules. |
| open [Precision](Precision.md)! | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#withSignificantDigits(kotlin.Int,%20kotlin.Int,%20android.icu.number.NumberFormatter.RoundingPriority)(minSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, priority: https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.RoundingPriority!)` Override maximum fraction digits with maximum significant digits depending on the magnitude of the number. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/icu/number/Precision` |---|---| | `https://developer.android.com/reference/kotlin/android/icu/number/CurrencyPrecision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#currency(android.icu.util.Currency.CurrencyUsage)(currencyUsage: https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage.html#!)` Show numbers rounded and padded according to the rules for the currency unit. The most common rounding precision settings for currencies include `Precision.fixedFraction(2)`, `Precision.integer()`, and `Precision.increment(0.05)` for cash transactions ("nickel rounding"). The exact rounding details will be resolved at runtime based on the currency unit specified in the NumberFormatter chain. To round according to the rules for one currency while displaying the symbol for another currency, the withCurrency() method can be called on the return value of this method. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#fixedFraction(kotlin.Int)(minMaxFractionPlaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Additionally, pad with zeros to ensure that this number of places are always shown. Example output with minMaxFractionPlaces = 3: 87,650.000 8,765.000 876.500 87.650 8.765 0.876 0.088 0.009 0.000 (zero) This method is equivalent to `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxFraction(kotlin.Int,%20kotlin.Int)` with both arguments equal. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#fixedSignificantDigits(kotlin.Int)(minMaxSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of significant digits or significant figures. Additionally, pad with zeros to ensure that this number of significant digits/figures are always shown. This method is equivalent to `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxSignificantDigits(kotlin.Int,%20kotlin.Int)` with both arguments equal. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#increment(java.math.BigDecimal)(roundingIncrement: https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!)` Show numbers rounded if necessary to the closest multiple of a certain rounding increment. For example, if the rounding increment is 0.5, then round 1.2 to 1 and round 1.3 to 1.5. In order to ensure that numbers are padded to the appropriate number of fraction places, set the scale on the rounding increment BigDecimal. For example, to round to the nearest 0.5 and always display 2 numerals after the decimal separator (to display 1.2 as "1.00" and 1.3 as "1.50"), you can run: ```kotlin Precision.increment(new BigDecimal("0.50")) ``` For more information on the scale of Java BigDecimal, see `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#scale()`. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#integer()()` Show numbers rounded if necessary to the nearest integer. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxFraction(kotlin.Int)(maxFractionPlaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Unlike the other fraction rounding strategies, this strategy does *not* pad zeros to the end of the number. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxSignificantDigits(kotlin.Int)(maxSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of significant digits/figures. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minFraction(kotlin.Int)(minFractionPlaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Always show at least a certain number of fraction places after the decimal separator, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision). **NOTE:** If you are formatting *doubles* , see the performance note in `https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited()`. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision#!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxFraction(kotlin.Int,%20kotlin.Int)(minFractionPlaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxFractionPlaces: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator); in addition, always show at least a certain number of places after the decimal separator, padding with zeros if necessary. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxSignificantDigits(kotlin.Int,%20kotlin.Int)(minSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, maxSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Show numbers rounded if necessary to a certain number of significant digits/figures; in addition, always show at least a certain number of significant digits, padding with zeros if necessary. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minSignificantDigits(kotlin.Int)(minSignificantDigits: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Always show at least a certain number of significant digits/figures, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision). **NOTE:** If you are formatting *doubles* , see the performance note in `https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited()`. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#trailingZeroDisplay(android.icu.number.NumberFormatter.TrailingZeroDisplay)(trailingZeroDisplay: https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.TrailingZeroDisplay!)` Configure how trailing zeros are displayed on numbers. For example, to hide trailing zeros when the number is an integer, use HIDE_IF_WHOLE. <br /> | | `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | `https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited()()` Show all available digits to full precision. **NOTE:** When formatting a *double* , this method, along with `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minFraction(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/icu/number/Precision#minSignificantDigits(kotlin.Int)`, will trigger complex algorithm similar to *Dragon4* to determine the low-order digits and the number of digits to display based on the value of the double. If the number of fraction places or significant digits can be bounded, consider using `https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxFraction(kotlin.Int)` or `https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxSignificantDigits(kotlin.Int)` instead to maximize performance. For more information, read the following blog post. http://www.serpentine.com/blog/2011/06/29/here-be-dragons-advances-in-problems-you-didnt-even-know-you-had/ <br /> | ||

## Public methods

### withMaxDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun withMaxDigits(maxSignificantDigits: Int): Precision!
```

Ensure that no more than this number of significant digits are retained when rounding according to fraction rules.

For example, with integer rounding, the number 123.4 becomes "123". However, with maximum figures set to 2, 123.4 becomes "120" instead.

This setting does not affect the number of trailing zeros. For example, with fixed fraction of 2, 123.4 would become "120.00".

This is equivalent to `withSignificantDigits(1, maxSignificantDigits, STRICT)`.

| Parameters ||
|---|---|
| `maxSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Round the number to no more than this number of significant figures. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | A Precision for chaining or passing to the NumberFormatter rounding() setter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter`

### withMinDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun withMinDigits(minSignificantDigits: Int): Precision!
```

Ensure that no less than this number of significant digits are retained when rounding according to fraction rules.

For example, with integer rounding, the number 3.141 becomes "3". However, with minimum figures set to 2, 3.141 becomes "3.1" instead.

This setting does not affect the number of trailing zeros. For example, 3.01 would print as "3", not "3.0".

This is equivalent to `withSignificantDigits(1, minSignificantDigits, RELAXED)`.

| Parameters ||
|---|---|
| `minSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of significant figures to guarantee. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | A Precision for chaining or passing to the NumberFormatter rounding() setter. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter`

### withSignificantDigits

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun withSignificantDigits(
    minSignificantDigits: Int, 
    maxSignificantDigits: Int, 
    priority: NumberFormatter.RoundingPriority!
): Precision!
```

Override maximum fraction digits with maximum significant digits depending on the magnitude of the number. See UNumberRoundingPriority.

| Parameters ||
|---|---|
| `minSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Pad trailing zeros to achieve this minimum number of significant digits. |
| `maxSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Round the number to achieve this maximum number of significant digits. |
| `priority` | [NumberFormatter.RoundingPriority](../android/icu/number/NumberFormatter.RoundingPriority.md)!: How to disambiguate between fraction digits and significant digits. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/number/Precision!` | A precision for chaining or passing to the NumberFormatter precision() setter. |
