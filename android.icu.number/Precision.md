# Precision

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Precision

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/Precision "View this page in Java") 
| --- | --- |

```
abstract class Precision
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.number.Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#) |

| Known Direct Subclasses [CurrencyPrecision](https://developer.android.com/reference/kotlin/android/icu/number/CurrencyPrecision), [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision) |----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CurrencyPrecision](https://developer.android.com/reference/kotlin/android/icu/number/CurrencyPrecision) | A class that defines a rounding strategy parameterized by a currency to be used when formatting numbers in NumberFormatter. | | [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision) | A class that defines a rounding strategy based on a number of fraction places and optionally significant digits to be used when formatting numbers in NumberFormatter. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A class that defines the rounding precision to be used when formatting numbers in NumberFormatter.

To create a Precision, use one of the factory methods.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [CurrencyPrecision](https://developer.android.com/reference/kotlin/android/icu/number/CurrencyPrecision)! | [currency](https://developer.android.com/reference/kotlin/android/icu/number/Precision#currency(android.icu.util.Currency.CurrencyUsage))`(`currencyUsage:` ` [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage.html#)!`)` Show numbers rounded and padded according to the rules for the currency unit. |
| openstatic [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | [fixedFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#fixedFraction(kotlin.Int))`(`minMaxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [fixedSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#fixedSignificantDigits(kotlin.Int))`(`minMaxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of significant digits or significant figures. |
| --- | --- |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [increment](https://developer.android.com/reference/kotlin/android/icu/number/Precision#increment(java.math.BigDecimal))`(`roundingIncrement:` ` [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!`)` Show numbers rounded if necessary to the closest multiple of a certain rounding increment. |
| openstatic [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | [integer](https://developer.android.com/reference/kotlin/android/icu/number/Precision#integer())`()` Show numbers rounded if necessary to the nearest integer. |
| openstatic [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | [maxFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxFraction(kotlin.Int))`(`maxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). |
| --- | --- |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [maxSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxSignificantDigits(kotlin.Int))`(`maxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of significant digits/figures. |
| openstatic [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | [minFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minFraction(kotlin.Int))`(`minFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Always show at least a certain number of fraction places after the decimal separator, padding with zeros if necessary. |
| openstatic [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | [minMaxFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxFraction(kotlin.Int,%20kotlin.Int))`(`minFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxFractionPlaces:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator); in addition, always show at least a certain number of places after the decimal separator, padding with zeros if necessary. |
| --- | --- |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [minMaxSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxSignificantDigits(kotlin.Int,%20kotlin.Int))`(`minSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Show numbers rounded if necessary to a certain number of significant digits/figures; in addition, always show at least a certain number of significant digits, padding with zeros if necessary. |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [minSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minSignificantDigits(kotlin.Int))`(`minSignificantDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Always show at least a certain number of significant digits/figures, padding with zeros if necessary. |
| open [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [trailingZeroDisplay](https://developer.android.com/reference/kotlin/android/icu/number/Precision#trailingZeroDisplay(android.icu.number.NumberFormatter.TrailingZeroDisplay))`(`trailingZeroDisplay:` ` [NumberFormatter.TrailingZeroDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.TrailingZeroDisplay)!`)` Configure how trailing zeros are displayed on numbers. |
| --- | --- |
| openstatic [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | [unlimited](https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited())`()` Show all available digits to full precision. |

## Public methods

### currency

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun currency(currencyUsage: Currency.CurrencyUsage!): CurrencyPrecision!
```

Show numbers rounded and padded according to the rules for the currency unit. The most common rounding precision settings for currencies include`Precision.fixedFraction(2)`,`Precision.integer()`, and`Precision.increment(0.05)`for cash transactions ("nickel rounding").

The exact rounding details will be resolved at runtime based on the currency unit specified in the NumberFormatter chain. To round according to the rules for one currency while displaying the symbol for another currency, the withCurrency() method can be called on the return value of this method.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currencyUsage` | [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage.html#)!:Either STANDARD (for digital transactions) or CASH (for transactions where the rounding increment may be limited by the available denominations of cash or coins). |

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [CurrencyPrecision](https://developer.android.com/reference/kotlin/android/icu/number/CurrencyPrecision)! | A CurrencyPrecision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if currencyUsage is null. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### fixedFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fixedFraction(minMaxFractionPlaces: Int): FractionPrecision!
```

Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Additionally, pad with zeros to ensure that this number of places are always shown.

Example output with minMaxFractionPlaces = 3:

87,650.000 
8,765.000 
876.500 
87.650 
8.765 
0.876 
0.088 
0.009 
0.000 (zero)

This method is equivalent to [minMaxFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxFraction(kotlin.Int,%20kotlin.Int))with both arguments equal.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minMaxFractionPlaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum and maximum number of numerals to display after the decimal separator (rounding if too long or padding with zeros if too short). |

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | A FractionPrecision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 0. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### fixedSignificantDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fixedSignificantDigits(minMaxSignificantDigits: Int): Precision!
```

Show numbers rounded if necessary to a certain number of significant digits or significant figures. Additionally, pad with zeros to ensure that this number of significant digits/figures are always shown.

This method is equivalent to [minMaxSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minMaxSignificantDigits(kotlin.Int,%20kotlin.Int))with both arguments equal.

| Parameters ||
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minMaxSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum and maximum number of significant digits to display (rounding if too long or padding with zeros if too short). |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### increment

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun increment(roundingIncrement: BigDecimal!): Precision!
```

Show numbers rounded if necessary to the closest multiple of a certain rounding increment. For example, if the rounding increment is 0.5, then round 1.2 to 1 and round 1.3 to 1.5.

In order to ensure that numbers are padded to the appropriate number of fraction places, set the scale on the rounding increment BigDecimal. For example, to round to the nearest 0.5 and always display 2 numerals after the decimal separator (to display 1.2 as "1.00" and 1.3 as "1.50"), you can run: 

```kotlin
Precision.increment(new BigDecimal("0.50"))
  
```

For more information on the scale of Java BigDecimal, see [java.math.BigDecimal#scale()](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#scale()).

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `roundingIncrement` | [BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#)!:The increment to which to round numbers. |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the rounding increment is null or non-positive. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### integer

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun integer(): FractionPrecision!
```

Show numbers rounded if necessary to the nearest integer.

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | A FractionPrecision for chaining or passing to the NumberFormatter precision() setter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### maxFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun maxFraction(maxFractionPlaces: Int): FractionPrecision!
```

Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator). Unlike the other fraction rounding strategies, this strategy does*not*pad zeros to the end of the number.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxFractionPlaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of numerals to display after the decimal mark (rounding if necessary). |

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | A FractionPrecision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 0. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### maxSignificantDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun maxSignificantDigits(maxSignificantDigits: Int): Precision!
```

Show numbers rounded if necessary to a certain number of significant digits/figures.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of significant digits to display (rounding if too long). |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### minFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun minFraction(minFractionPlaces: Int): FractionPrecision!
```

Always show at least a certain number of fraction places after the decimal separator, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision).

**NOTE:** If you are formatting*doubles* , see the performance note in [unlimited](https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited()).

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minFractionPlaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum number of numerals to display after the decimal separator (padding with zeros if necessary). |

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | A FractionPrecision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 0. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### minMaxFraction

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun minMaxFraction(
    minFractionPlaces: Int, 
    maxFractionPlaces: Int
): FractionPrecision!
```

Show numbers rounded if necessary to a certain number of fraction places (numerals after the decimal separator); in addition, always show at least a certain number of places after the decimal separator, padding with zeros if necessary.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minFractionPlaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum number of numerals to display after the decimal separator (padding with zeros if necessary). |
| `maxFractionPlaces` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of numerals to display after the decimal separator (rounding if necessary). |

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [FractionPrecision](https://developer.android.com/reference/kotlin/android/icu/number/FractionPrecision)! | A FractionPrecision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 0. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### minMaxSignificantDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun minMaxSignificantDigits(
    minSignificantDigits: Int, 
    maxSignificantDigits: Int
): Precision!
```

Show numbers rounded if necessary to a certain number of significant digits/figures; in addition, always show at least a certain number of significant digits, padding with zeros if necessary.

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum number of significant digits to display (padding with zeros if necessary). |
| `maxSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of significant digits to display (rounding if necessary). |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### minSignificantDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun minSignificantDigits(minSignificantDigits: Int): Precision!
```

Always show at least a certain number of significant digits/figures, padding with zeros if necessary. Do not perform rounding (display numbers to their full precision).

**NOTE:** If you are formatting*doubles* , see the performance note in [unlimited](https://developer.android.com/reference/kotlin/android/icu/number/Precision#unlimited()).

| Parameters ||
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `minSignificantDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum number of significant digits to display (padding with zeros if too short). |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the input number is too big or smaller than 1. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### trailingZeroDisplay

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trailingZeroDisplay(trailingZeroDisplay: NumberFormatter.TrailingZeroDisplay!): Precision!
```

Configure how trailing zeros are displayed on numbers. For example, to hide trailing zeros when the number is an integer, use HIDE_IF_WHOLE.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trailingZeroDisplay` | [NumberFormatter.TrailingZeroDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.TrailingZeroDisplay)!:Option to configure the display of trailing zeros. |

### unlimited

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun unlimited(): Precision!
```

Show all available digits to full precision.

**NOTE:** When formatting a*double* , this method, along with [minFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minFraction(kotlin.Int))and [minSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#minSignificantDigits(kotlin.Int)), will trigger complex algorithm similar to*Dragon4* to determine the low-order digits and the number of digits to display based on the value of the double. If the number of fraction places or significant digits can be bounded, consider using [maxFraction](https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxFraction(kotlin.Int))or [maxSignificantDigits](https://developer.android.com/reference/kotlin/android/icu/number/Precision#maxSignificantDigits(kotlin.Int))instead to maximize performance. For more information, read the following blog post.

http://www.serpentine.com/blog/2011/06/29/here-be-dragons-advances-in-problems-you-didnt-even-know-you-had/

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Precision](https://developer.android.com/reference/kotlin/android/icu/number/Precision#)! | A Precision for chaining or passing to the NumberFormatter precision() setter. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
