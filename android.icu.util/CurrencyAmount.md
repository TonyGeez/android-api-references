# CurrencyAmount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CurrencyAmount

Kotlin| [Java](CurrencyAmount.md) 
| --- | --- |

```
open class CurrencyAmount : Measure
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.icu.util.Measure](Measure.md) ||
| | ↳ | [android.icu.util.CurrencyAmount](CurrencyAmount.md) |

An amount of currency, consisting of a Number and a Currency. CurrencyAmount objects are immutable.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CurrencyAmount](CurrencyAmount.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](Currency.md)!`)` Constructs a new object given a double value and a currency. |
| [CurrencyAmount](CurrencyAmount.md))`(`number:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `currency:` ` [Currency](../java.util/Currency.md)!`)` Constructs a new object given a double value and a Java currency. |
| [CurrencyAmount](CurrencyAmount.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](Currency.md)!`)` Constructs a new object given a number and a currency. |
| [CurrencyAmount](CurrencyAmount.md))`(`number:` ` [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)!`, `currency:` ` [Currency](../java.util/Currency.md)!`)` Constructs a new object given a number and a Java currency. |

| Public methods ||
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Currency](Currency.md)! | [getCurrency](CurrencyAmount.md))`()` Returns the currency of this object. |

| Inherited functions ||
|---|---|
| From class [Measure](Measure.md) |---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Measure.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Returns true if the given object is equal to this object. <br /> | | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)! | [getNumber](Measure.md))`()` <br /> Returns the numeric value of this object. <br /> | | [MeasureUnit](MeasureUnit.md)! | [getUnit](Measure.md))`()` <br /> Returns the unit of this object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Measure.md))`()` <br /> Returns a hashcode for this object. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Measure.md))`()` <br /> Returns a string representation of this object. <br /> | ||

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
| `currency` | [Currency](Currency.md)!:the currency |

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
| `currency` | [Currency](../java.util/Currency.md)!:the currency |

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
| `currency` | [Currency](Currency.md)!:the currency |

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
| `currency` | [Currency](../java.util/Currency.md)!:the currency |

## Public methods

### getCurrency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrency(): Currency!
```

Returns the currency of this object.

| Return ||
|---------------------------------------------------------------------------------------|------------------------|
| [Currency](Currency.md)! | this object's Currency |
