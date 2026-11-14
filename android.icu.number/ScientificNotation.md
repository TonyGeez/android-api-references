# ScientificNotation

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScientificNotation

Kotlin| [Java](https://developer.android.com/reference/android/icu/number/ScientificNotation "View this page in Java") 
| --- | --- |

```
open class ScientificNotation : Notation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.number.Notation](https://developer.android.com/reference/kotlin/android/icu/number/Notation) ||
| | ↳ | [android.icu.number.ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#) |

A class that defines the scientific notation style to be used when formatting numbers in NumberFormatter.

To create a ScientificNotation, use one of the factory methods in [Notation](https://developer.android.com/reference/kotlin/android/icu/number/Notation).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | [withExponentSignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#withExponentSignDisplay(android.icu.number.NumberFormatter.SignDisplay))`(`exponentSignDisplay:` ` [NumberFormatter.SignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.SignDisplay)!`)` Sets whether to show the sign on positive and negative exponents in scientific notation. |
| open [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | [withMinExponentDigits](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#withMinExponentDigits(kotlin.Int))`(`minExponentDigits:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the minimum number of digits to show in the exponent of scientific notation, padding with zeros if necessary. |

| Inherited functions ||
|---|---|
| From class [Notation](https://developer.android.com/reference/kotlin/android/icu/number/Notation) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CompactNotation](https://developer.android.com/reference/kotlin/android/icu/number/CompactNotation)! | [compactLong](https://developer.android.com/reference/kotlin/android/icu/number/Notation#compactLong())`()` <br /> Print the number using long-form compact notation. For more information on compact notation, see [compactShort](https://developer.android.com/reference/kotlin/android/icu/number/Notation#compactShort()). In long form, the powers of ten are spelled out fully. Example outputs in*en-US*when printing 8.765E7 through 8.765E0: ```kotlin 88 million 8.8 million 876 thousand 88 thousand 8.8 thousand 876 88 8.8 ``` <br /> | | [CompactNotation](https://developer.android.com/reference/kotlin/android/icu/number/CompactNotation)! | [compactShort](https://developer.android.com/reference/kotlin/android/icu/number/Notation#compactShort())`()` <br /> Print the number using short-form compact notation. *Compact notation*, defined in Unicode Technical Standard #35 Part 3 Section 2.4.1, prints numbers with localized prefixes or suffixes corresponding to different powers of ten. Compact notation is similar to engineering notation in how it scales numbers. Compact notation is ideal for displaying large numbers (over \~1000) to humans while at the same time minimizing screen real estate. In short form, the powers of ten are abbreviated. In*en-US* , the abbreviations are "K" for thousands, "M" for millions, "B" for billions, and "T" for trillions. Example outputs in*en-US*when printing 8.765E7 through 8.765E0: ```kotlin 88M 8.8M 876K 88K 8.8K 876 88 8.8 ``` When compact notation is specified without an explicit rounding strategy, numbers are rounded off to the closest integer after scaling the number by the corresponding power of 10, but with a digit shown after the decimal separator if there is only one digit before the decimal separator. The default compact notation rounding strategy is equivalent to: ```kotlin Rounder.integer().withMinDigits(2) ``` <br /> | | [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | [engineering](https://developer.android.com/reference/kotlin/android/icu/number/Notation#engineering())`()` <br /> Print the number using engineering notation, a variant of scientific notation in which the exponent must be divisible by 3. Example outputs in*en-US*when printing 8.765E4 through 8.765E-3: ```kotlin 87.65E3 8.765E3 876.5E0 87.65E0 8.765E0 876.5E-3 87.65E-3 8.765E-3 0E0 ``` <br /> | | [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | [scientific](https://developer.android.com/reference/kotlin/android/icu/number/Notation#scientific())`()` <br /> Print the number using scientific notation (also known as scientific form, standard index form, or standard form in the UK). The format for scientific notation varies by locale; for example, many Western locales display the number in the form "#E0", where the number is displayed with one digit before the decimal separator, zero or more digits after the decimal separator, and the corresponding power of 10 displayed after the "E". Example outputs in*en-US*when printing 8.765E4 through 8.765E-3: ```kotlin 8.765E4 8.765E3 8.765E2 8.765E1 8.765E0 8.765E-1 8.765E-2 8.765E-3 0E0 ``` <br /> | | [SimpleNotation](https://developer.android.com/reference/kotlin/android/icu/number/SimpleNotation)! | [simple](https://developer.android.com/reference/kotlin/android/icu/number/Notation#simple())`()` <br /> Print the number using simple notation without any scaling by powers of ten. This is the default behavior. Since this is the default behavior, this method needs to be called only when it is necessary to override a previous setting. Example outputs in*en-US*when printing 8.765E7 through 8.765E0: ```kotlin 87,650,000 8,765,000 876,500 87,650 8,765 876.5 87.65 8.765 ``` <br /> | ||

## Public methods

### withExponentSignDisplay

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withExponentSignDisplay(exponentSignDisplay: NumberFormatter.SignDisplay!): ScientificNotation!
```

Sets whether to show the sign on positive and negative exponents in scientific notation. The default is AUTO, showing the minus sign but not the plus sign.

For example, with exponentSignDisplay=ALWAYS, the number 123 will be printed as "1.23E+2" in*en-US*instead of the default "1.23E2".

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exponentSignDisplay` | [NumberFormatter.SignDisplay](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter.SignDisplay)!:The strategy for displaying the sign in the exponent. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | A ScientificNotation, for chaining. |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter) 

### withMinExponentDigits

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withMinExponentDigits(minExponentDigits: Int): ScientificNotation!
```

Sets the minimum number of digits to show in the exponent of scientific notation, padding with zeros if necessary. Useful for fixed-width display.

For example, with minExponentDigits=2, the number 123 will be printed as "1.23E02" in*en-US*instead of the default "1.23E2".

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------|
| `minExponentDigits` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The minimum number of digits to show in the exponent. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [ScientificNotation](https://developer.android.com/reference/kotlin/android/icu/number/ScientificNotation#)! | A ScientificNotation, for chaining. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if minExponentDigits is too big or smaller than 1 |

**See Also**

- [android.icu.number.NumberFormatter](https://developer.android.com/reference/kotlin/android/icu/number/NumberFormatter)
