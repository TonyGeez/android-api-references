# CurrencyAmount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CurrencyAmount

Kotlin| [Java](../android/icu/util/CurrencyAmount.md) 
| --- | --- |

```
open class CurrencyAmount : Measure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.util.Measure](../android/icu/util/Measure.md) ||
| | ↳ | [android.icu.util.CurrencyAmount](../android/icu/util/CurrencyAmount.md) |

An amount of currency, consisting of a Number and a Currency. CurrencyAmount objects are immutable.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CurrencyAmount](../android/icu/util/CurrencyAmount.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](../android/icu/util/Currency.md)!`)` Constructs a new object given a double value and a currency. |
| [CurrencyAmount](../android/icu/util/CurrencyAmount.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](../java/util/Currency.md)!`)` Constructs a new object given a double value and a Java currency. |
| [CurrencyAmount](../android/icu/util/CurrencyAmount.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](../android/icu/util/Currency.md)!`)` Constructs a new object given a number and a currency. |
| [CurrencyAmount](../android/icu/util/CurrencyAmount.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](../java/util/Currency.md)!`)` Constructs a new object given a number and a Java currency. |

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Currency](../android/icu/util/Currency.md)! | [getCurrency](../android/icu/util/CurrencyAmount.md))`()` Returns the currency of this object. |

| Inherited functions ||
|---|---|
| From class [Measure](../android/icu/util/Measure.md) |---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/icu/util/Measure.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Returns true if the given object is equal to this object. <br /> | | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getNumber](../android/icu/util/Measure.md))`()` <br /> Returns the numeric value of this object. <br /> | | [MeasureUnit](../android/icu/util/MeasureUnit.md)! | [getUnit](../android/icu/util/Measure.md))`()` <br /> Returns the unit of this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/icu/util/Measure.md))`()` <br /> Returns a hashcode for this object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/icu/util/Measure.md))`()` <br /> Returns a string representation of this object. <br /> | ||

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
| `currency` | [Currency](../android/icu/util/Currency.md)!:the currency |

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
| `currency` | [Currency](../java/util/Currency.md)!:the currency |

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
| `currency` | [Currency](../android/icu/util/Currency.md)!:the currency |

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
| `currency` | [Currency](../java/util/Currency.md)!:the currency |

## Public methods

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the currency of this object.

| Return ||
|---------------------------------------------------------------------------------------|------------------------|
| [Currency](../android/icu/util/Currency.md)! | this object's Currency |
