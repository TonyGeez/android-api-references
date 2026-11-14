# Currency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Currency

```
class Currency : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Currency](https://developer.android.com/reference/kotlin/java/util/Currency#) |

Represents a currency. Currencies are identified by their ISO 4217 currency codes. Visit the [ISO web site](http://www.iso.org/iso/home/standards/currency_codes.htm) for more information.

The class is designed so that there's never more than one`Currency`instance for any given currency. Therefore, there's no public constructor. You obtain a`Currency`instance using the`getInstance`methods.

It is recommended to use [java.math.BigDecimal](https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#) class while dealing with`Currency`or monetary values as it provides better handling of floating point numbers and their operations.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)!\>! | [getAvailableCurrencies](https://developer.android.com/reference/kotlin/java/util/Currency#getAvailableCurrencies())`()` Gets the set of available currencies. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrencyCode](https://developer.android.com/reference/kotlin/java/util/Currency#getCurrencyCode())`()` Gets the ISO 4217 currency code of this currency. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultFractionDigits](https://developer.android.com/reference/kotlin/java/util/Currency#getDefaultFractionDigits())`()` Gets the default number of fraction digits used with this currency. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Currency#getDisplayName())`()` Gets the name that is suitable for displaying this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/java/util/Currency#getDisplayName(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` Gets the name that is suitable for displaying this currency for the specified locale. |
| static [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)! | [getInstance](https://developer.android.com/reference/kotlin/java/util/Currency#getInstance(kotlin.String))`(`currencyCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the`Currency`instance for the given currency code. |
| static [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)! | [getInstance](https://developer.android.com/reference/kotlin/java/util/Currency#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` Returns the`Currency`instance for the country of the given locale. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericCode](https://developer.android.com/reference/kotlin/java/util/Currency#getNumericCode())`()` Returns the ISO 4217 numeric code of this currency. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getNumericCodeAsString](https://developer.android.com/reference/kotlin/java/util/Currency#getNumericCodeAsString())`()` Returns the 3 digit ISO 4217 numeric code of this currency as a`String`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSymbol](https://developer.android.com/reference/kotlin/java/util/Currency#getSymbol())`()` Gets the symbol of this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSymbol](https://developer.android.com/reference/kotlin/java/util/Currency#getSymbol(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!`)` Gets the symbol of this currency for the specified locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/Currency#toString())`()` Returns the ISO 4217 currency code of this currency. |

## Public methods

### getAvailableCurrencies

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableCurrencies(): MutableSet<Currency!>!
```

Gets the set of available currencies. The returned set of currencies contains all of the available currencies, which may include currencies that represent obsolete ISO 4217 codes. The set can be modified without affecting the available currencies in the runtime.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)!>! | the set of available currencies. If there is no currency available in the runtime, the returned set is empty. |

### getCurrencyCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCurrencyCode(): String!
```

Gets the ISO 4217 currency code of this currency.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the ISO 4217 currency code of this currency. |

### getDefaultFractionDigits

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultFractionDigits(): Int
```

Gets the default number of fraction digits used with this currency. Note that the number of fraction digits is the same as ISO 4217's minor unit for the currency. For example, the default number of fraction digits for the Euro is 2, while for the Japanese Yen it's 0. In the case of pseudo-currencies, such as IMF Special Drawing Rights, -1 is returned.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default number of fraction digits used with this currency |

### getDisplayName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): String!
```

Gets the name that is suitable for displaying this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. If there is no suitable display name found for the default locale, the ISO 4217 currency code is returned.

This is equivalent to calling [getDisplayName(Locale.getDefault(Locale.Category.DISPLAY))](https://developer.android.com/reference/kotlin/java/util/Currency#getDisplayName(java.util.Locale)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale |

### getDisplayName

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(locale: Locale!): String!
```

Gets the name that is suitable for displaying this currency for the specified locale. If there is no suitable display name found for the specified locale, the ISO 4217 currency code is returned.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!:the locale for which a display name for this currency is needed |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the display name of this currency for the specified locale |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(currencyCode: String!): Currency!
```

Returns the`Currency`instance for the given currency code.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------|
| `currencyCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the ISO 4217 code of the currency |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)! | the`Currency`instance for the given currency code |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.NullPointerException` | if`currencyCode`is null |
| `java.lang.IllegalArgumentException` | if`currencyCode`is not a supported ISO 4217 code. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(locale: Locale!): Currency!
```

Returns the`Currency`instance for the country of the given locale. The language and variant components of the locale are ignored. The result may vary over time, as countries change their currencies. For example, for the original member countries of the European Monetary Union, the method returns the old national currencies until December 31, 2001, and the Euro from January 1, 2002, local time of the respective countries.

If the specified`locale`contains "cu" java.util.Locale#, the instance returned from this method reflects the values specified with those extensions.

The method returns`null`for territories that don't have a currency, such as Antarctica.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!:the locale for whose country a`Currency`instance is needed |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/java/util/Currency#)! | the`Currency`instance for the country of the given locale, or`null` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`locale`is`null` |
| `java.lang.IllegalArgumentException` | if the country of the given`locale`is not a supported ISO 3166 country code. |

### getNumericCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNumericCode(): Int
```

Returns the ISO 4217 numeric code of this currency.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the ISO 4217 numeric code of this currency |

### getNumericCodeAsString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNumericCodeAsString(): String!
```

Returns the 3 digit ISO 4217 numeric code of this currency as a`String`. Unlike [getNumericCode()](https://developer.android.com/reference/kotlin/java/util/Currency#getNumericCode()), which returns the numeric code as`int`, this method always returns the numeric code as a 3 digit string. e.g. a numeric value of 32 would be returned as "032", and a numeric value of 6 would be returned as "006".

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the 3 digit ISO 4217 numeric code of this currency as a`String` |

### getSymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSymbol(): String!
```

Gets the symbol of this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale. For example, for the US Dollar, the symbol is "$" if the default locale is the US, while for other locales it may be "US$". If no symbol can be determined, the ISO 4217 currency code is returned.

This is equivalent to calling [getSymbol(Locale.getDefault(Locale.Category.DISPLAY))](https://developer.android.com/reference/kotlin/java/util/Currency#getSymbol(java.util.Locale)).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the symbol of this currency for the default [DISPLAY](https://developer.android.com/reference/kotlin/java/util/Locale.Category) locale |

### getSymbol

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSymbol(locale: Locale!): String!
```

Gets the symbol of this currency for the specified locale. For example, for the US Dollar, the symbol is "$" if the specified locale is the US, while for other locales it may be "US$". If no symbol can be determined, the ISO 4217 currency code is returned.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale)!:the locale for which a display name for this currency is needed |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the symbol of this currency for the specified locale |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`locale`is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the ISO 4217 currency code of this currency.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the ISO 4217 currency code of this currency |
