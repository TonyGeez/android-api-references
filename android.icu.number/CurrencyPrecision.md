# CurrencyPrecision

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CurrencyPrecision

Kotlin| [Java](CurrencyPrecision.md) 
| --- | --- |

```
abstract class CurrencyPrecision : Precision
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.number.Precision](Precision.md) ||
| | ↳ | [android.icu.number.CurrencyPrecision](CurrencyPrecision.md) |

A class that defines a rounding strategy parameterized by a currency to be used when formatting numbers in NumberFormatter.

To create a CurrencyPrecision, use one of the factory methods on Precision.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Precision](Precision.md)! | [withCurrency](CurrencyPrecision.md))`(`currency:` ` [Currency](../android.icu.util/Currency.md)!`)` Associates a currency with this rounding strategy. |

| Inherited functions ||
|---|---|
| From class [Precision](Precision.md) |------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CurrencyPrecision](CurrencyPrecision.md)! | [currency](Precision.md))`(`currencyUsage:` ` [Currency.CurrencyUsage](../android/icu/util/Currency.CurrencyUsage.md)!`)` <br /> Show numbers rounded and padded according to the rules for the currency unit. The most common rounding precision settings for currencies include`Precision.fixedFraction(2)`,`Precision.integer()`, and`Precision.increment(0.05)`for cash transactions ("nickel rounding"). The exact rounding details will be resolved at runtime based on the currency unit specified in the NumberFormatter chain. To round according to the rules for one currency while displaying the symbol for another currency, the withCurrency() method can be called on the return value of this method. <br /> | | [FractionPrecision](FractionPrecision.md)! | [fixedFraction](Precision.md))`(`minMaxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Additionally, pad with zeros to ensure that this number of places are always shown. Example output with minMaxFractionPlaces = 3: 87,650.000 8,765.000 876.500 87.650 8.765 0.876 0.088 0.009 0.000 (zero) This method is equivalent to [minMaxFraction](Precision.md))with both arguments equal. <br /> | | [Precision](Precision.md)! | [fixedSignificantDigits](Precision.md))`(`minMaxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of significant digits or significant figures. Additionally, pad with zeros to ensure that this number of significant digits/figures are always shown. This method is equivalent to [minMaxSignificantDigits](Precision.md))with both arguments equal. <br /> | | [Precision](Precision.md)! | [increment](Precision.md))`(`roundingIncrement:` ` [BigDecimal](../java.math/BigDecimal.md)!`)` <br /> Show numbers rounded if necessary to the closest multiple of a certain rounding increment. For example, if the rounding increment is 0.5, then round 1.2 to 1 and round 1.3 to 1.5. In order to ensure that numbers are padded to the appropriate number of fraction places, set the scale on the rounding increment BigDecimal. For example, to round to the nearest 0.5 and always display 2 numerals after the decimal separator (to display 1.2 as "1.00" and 1.3 as "1.50"), you can run: ```kotlin Precision.increment(new BigDecimal("0.50")) ``` For more information on the scale of Java BigDecimal, see [java.math.BigDecimal#scale()](../java.math/BigDecimal.md)). <br /> | | [FractionPrecision](FractionPrecision.md)! | [integer](Precision.md))`()` <br /> Show numbers rounded if necessary to the nearest integer. <br /> | | [FractionPrecision](FractionPrecision.md)! | [maxFraction](Precision.md))`(`maxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Unlike the other fraction rounding strategies, this strategy does*not*pad zeros to the end of the number. <br /> | | [Precision](Precision.md)! | [maxSignificantDigits](Precision.md))`(`maxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of significant digits/figures. <br /> | | [FractionPrecision](FractionPrecision.md)! | [minFraction](Precision.md))`(`minFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Always show at least a certain number of fraction places after the decimal separator, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision). **NOTE:** If you are formatting*doubles* , see the performance note in [unlimited](Precision.md)). <br /> | | [FractionPrecision](FractionPrecision.md)! | [minMaxFraction](Precision.md))`(`minFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator); in addition, always show at least a certain number of places after the decimal separator, padding with zeros if necessary. <br /> | | [Precision](Precision.md)! | [minMaxSignificantDigits](Precision.md))`(`minSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Show numbers rounded if necessary to a certain number of significant digits/figures; in addition, always show at least a certain number of significant digits, padding with zeros if necessary. <br /> | | [Precision](Precision.md)! | [minSignificantDigits](Precision.md))`(`minSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Always show at least a certain number of significant digits/figures, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision). **NOTE:** If you are formatting*doubles* , see the performance note in [unlimited](Precision.md)). <br /> | | [Precision](Precision.md)! | [trailingZeroDisplay](Precision.md))`(`trailingZeroDisplay:` ` [NumberFormatter.TrailingZeroDisplay](../android/icu/number/NumberFormatter.TrailingZeroDisplay.md)!`)` <br /> Configure how trailing zeros are displayed on numbers. For example, to hide trailing zeros when the number is an integer, use HIDE_IF_WHOLE. <br /> | | [Precision](Precision.md)! | [unlimited](Precision.md))`()` <br /> Show all available digits to full precision. **NOTE:** When formatting a*double* , this method, along with [minFraction](Precision.md))and [minSignificantDigits](Precision.md)), will trigger complex algorithm similar to*Dragon4* to determine the low-order digits and the number of digits to display based on the value of the double. If the number of fraction places or significant digits can be bounded, consider using [maxFraction](Precision.md))or [maxSignificantDigits](Precision.md))instead to maximize performance. For more information, read the following blog post. http://www.serpentine.com/blog/2011/06/29/here-be-dragons-advances-in-problems-you-didnt-even-know-you-had/ <br /> | ||

## Public methods

### withCurrency

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withCurrency(currency: Currency!): Precision!
```

Associates a currency with this rounding strategy.

**Calling this method is*not required***, because the currency specified in unit() or via a CurrencyAmount passed into format(Measure) is automatically applied to currency rounding strategies. However, this method enables you to override that automatic association.

This method also enables numbers to be formatted using currency rounding rules without explicitly using a currency format.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `currency` | [Currency](../android.icu.util/Currency.md)!:The currency to associate with this rounding strategy. |

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Precision](Precision.md)! | A Precision for chaining or passing to the NumberFormatter rounding() setter. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | for null Currency |

**See Also**

- [android.icu.number.NumberFormatter](NumberFormatter.md)
