# CurrencyAmount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CurrencyAmount

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/CurrencyAmount "View this page in Java") 
| --- | --- |

```
open class CurrencyAmount : Measure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.util.Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure) ||
| | ↳ | [android.icu.util.CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#) |

An amount of currency, consisting of a Number and a Currency. CurrencyAmount objects are immutable.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#CurrencyAmount(kotlin.Double,%20android.icu.util.Currency))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)!`)` Constructs a new object given a double value and a currency. |
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#CurrencyAmount(kotlin.Double,%20java.util.Currency))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!`)` Constructs a new object given a double value and a Java currency. |
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#CurrencyAmount(kotlin.Number,%20android.icu.util.Currency))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)!`)` Constructs a new object given a number and a currency. |
| [CurrencyAmount](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#CurrencyAmount(kotlin.Number,%20java.util.Currency))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!`)` Constructs a new object given a number and a Java currency. |

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)! | [getCurrency](https://developer.android.com/reference/kotlin/android/icu/util/CurrencyAmount#getCurrency())`()` Returns the currency of this object. |

| Inherited functions ||
|---|---|
| From class [Measure](https://developer.android.com/reference/kotlin/android/icu/util/Measure) |---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/util/Measure#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Returns true if the given object is equal to this object. <br /> | | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getNumber](https://developer.android.com/reference/kotlin/android/icu/util/Measure#getNumber())`()` <br /> Returns the numeric value of this object. <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [getUnit](https://developer.android.com/reference/kotlin/android/icu/util/Measure#getUnit())`()` <br /> Returns the unit of this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/util/Measure#hashCode())`()` <br /> Returns a hashcode for this object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/util/Measure#toString())`()` <br /> Returns a string representation of this object. <br /> | ||

## Public constructors

### CurrencyAmount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CurrencyAmount(
    number: Double, 
    currency: Currency!)
```

Constructs a new object given a double value and a currency.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a double value |
| `currency` | [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)!:the currency |

### CurrencyAmount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CurrencyAmount(
    number: Double, 
    currency: Currency!)
```

Constructs a new object given a double value and a Java currency.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------|
| `number` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):a double value |
| `currency` | [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!:the currency |

### CurrencyAmount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CurrencyAmount(
    number: Number!, 
    currency: Currency!)
```

Constructs a new object given a number and a currency.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------|
| `number` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:the number |
| `currency` | [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)!:the currency |

### CurrencyAmount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CurrencyAmount(
    number: Number!, 
    currency: Currency!)
```

Constructs a new object given a number and a Java currency.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------|
| `number` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!:the number |
| `currency` | [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!:the currency |

## Public methods

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the currency of this object.

| Return ||
|---------------------------------------------------------------------------------------|------------------------|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency)! | this object's Currency |
