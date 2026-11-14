# Currency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Currency

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/Currency "View this page in Java") 

```
open class Currency : MeasureUnit
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.icu.util.MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit) ||
| | ↳ | [android.icu.util.Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#) |

A class encapsulating a currency, as defined by ISO 4217. A Currency object can be created given a Locale or given an ISO 4217 code. Once created, the Currency object can return various data necessary to its proper display:

- A display symbol, for a specific locale
- The number of fraction digits to display
- A rounding increment

The DecimalFormat class uses these data to display currencies.

<br />

Note: This class deliberately resembles java.util.Currency but it has a completely independent implementation, and adds features not present in the JDK.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage) Currency Usage used for Decimal Format |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FORMAL_SYMBOL_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#FORMAL_SYMBOL_NAME:kotlin.Int) Selector for getName() indicating the formal currency symbol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LONG_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#LONG_NAME:kotlin.Int) Selector for getName() indicating the long name for a currency, such as "US Dollar" for USD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NARROW_SYMBOL_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#NARROW_SYMBOL_NAME:kotlin.Int) Selector for getName() indicating the narrow currency symbol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLURAL_LONG_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#PLURAL_LONG_NAME:kotlin.Int) Selector for getName() indicating the plural long name for a currency, such as "US dollar" for USD in "1 US dollar", and "US dollars" for USD in "2 US dollars". |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SYMBOL_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#SYMBOL_NAME:kotlin.Int) Selector for getName() indicating a symbolic name for a currency, such as "$" for USD. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VARIANT_SYMBOL_NAME](https://developer.android.com/reference/kotlin/android/icu/util/Currency#VARIANT_SYMBOL_NAME:kotlin.Int) Selector for getName() indicating the variant currency symbol. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#Currency(kotlin.String))`(`theISOCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a currency object for the given ISO 4217 3-letter code. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | [fromJavaCurrency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#fromJavaCurrency(java.util.Currency))`(`currency:` ` [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!`)` Returns a Currency object based on the currency represented by the given java. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)!\>! | [getAvailableCurrencies](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getAvailableCurrencies())`()` Returns the set of available currencies. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableCurrencyCodes](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getAvailableCurrencyCodes(android.icu.util.ULocale,%20java.util.Date))`(`loc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`, `d:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Returns an array of Strings which contain the currency identifiers that are valid for the given locale on the given date. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getAvailableCurrencyCodes](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getAvailableCurrencyCodes(java.util.Locale,%20java.util.Date))`(`loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `d:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Returns an array of Strings which contain the currency identifiers that are valid for the given [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) on the given date. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getAvailableLocales())`()` Return an array of the locales for which a currency is defined. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!\>! | [getAvailableULocales](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getAvailableULocales())`()` Return an array of the ulocales for which a currency is defined. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCurrencyCode](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getCurrencyCode())`()` Returns the ISO 4217 3-letter code for this currency object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultFractionDigits](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDefaultFractionDigits())`()` Returns the number of the number of fraction digits that should be displayed for this currency. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultFractionDigits](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDefaultFractionDigits(android.icu.util.Currency.CurrencyUsage))`(`Usage:` ` [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage)!`)` Returns the number of the number of fraction digits that should be displayed for this currency with Usage. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDisplayName())`()` Returns the display name for this currency in the default locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDisplayName(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns the display name for this currency in the given locale. |
| openstatic [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getInstance(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`)` Returns a currency object for the default currency in the given locale. |
| openstatic [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getInstance(kotlin.String))`(`theISOCode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a currency object given an ISO 4217 3-letter code. |
| openstatic [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | [getInstance](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getInstance(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Returns a currency object for the default currency in the given locale. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getKeywordValuesForLocale](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getKeywordValuesForLocale(kotlin.String,%20android.icu.util.ULocale,%20kotlin.Boolean))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`, `commonlyUsed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Given a key and a locale, returns an array of values for the key for which data exists. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(android.icu.util.ULocale,%20kotlin.Int,%20kotlin.BooleanArray))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`, `nameStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isChoiceFormat:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` Returns the display name for the given currency in the given locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(android.icu.util.ULocale,%20kotlin.Int,%20kotlin.String,%20kotlin.BooleanArray))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`, `nameStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pluralCount:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isChoiceFormat:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` Returns the display name for the given currency in the given locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(java.util.Locale,%20kotlin.Int,%20kotlin.BooleanArray))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `nameStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isChoiceFormat:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` Returns the display name for the given currency in the given locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(java.util.Locale,%20kotlin.Int,%20kotlin.String,%20kotlin.BooleanArray))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `nameStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pluralCount:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `isChoiceFormat:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` Returns the display name for the given currency in the given locale. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericCode](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getNumericCode())`()` Returns the ISO 4217 numeric code for this currency object. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getRoundingIncrement](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getRoundingIncrement())`()` Returns the rounding increment for this currency, or 0. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getRoundingIncrement](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getRoundingIncrement(android.icu.util.Currency.CurrencyUsage))`(`Usage:` ` [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage)!`)` Returns the rounding increment for this currency, or 0. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSymbol](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getSymbol())`()` Convenience and compatibility override of getName that requests the symbol name for the default`DISPLAY`locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSymbol](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getSymbol(android.icu.util.ULocale))`(`uloc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!`)` Convenience and compatibility override of getName that requests the symbol name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSymbol](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getSymbol(java.util.Locale))`(`loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Convenience and compatibility override of getName that requests the symbol name. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAvailable](https://developer.android.com/reference/kotlin/android/icu/util/Currency#isAvailable(kotlin.String,%20java.util.Date,%20java.util.Date))`(`code:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `from:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`, `to:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Queries if the given ISO 4217 3-letter code is available on the specified date range. |
| open [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)! | [toJavaCurrency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#toJavaCurrency())`()` Returns a java. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/util/Currency#toString())`()` Returns the ISO 4217 code for this currency. |

| Inherited functions ||
|---|---|
| From class [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Indicates whether some other object is "equal to" this one. The`equals`method implements an equivalence relation on non-null object references: - It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`. - It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`. - It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`. - It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified. - For any non-null reference value`x`,`x.equals(null)`should return`false`. An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes. <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [forIdentifier](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#forIdentifier(kotlin.String))`(`identifier:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Construct a MeasureUnit from a CLDR Core Unit Identifier, defined in UTS 35. (Core unit identifiers and mixed unit identifiers are supported, long unit identifiers are not.) Validates and canonicalizes the identifier. Note: dimensionless`MeasureUnit`is`null` ```kotlin MeasureUnit example = MeasureUnit::forIdentifier("furlong-per-nanosecond") ``` <br /> <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!>! | [getAvailable](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getAvailable())`()` <br /> Get all of the available units. Returned set is unmodifiable. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!>! | [getAvailable](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getAvailable(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> For the given type, return the available units. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getAvailableTypes](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getAvailableTypes())`()` <br /> Get all of the available units' types. Returned set is unmodifiable. <br /> | | [MeasureUnit.Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity)! | [getComplexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getComplexity())`()` <br /> Compute the complexity of the unit. See Complexity for more information. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDimensionality](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getDimensionality())`()` <br /> Returns the dimensionality (power) of this MeasureUnit. For example, if the unit is square, then 2 is returned. NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an exception will be thrown. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getIdentifier](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getIdentifier())`()` <br /> Get CLDR Unit Identifier for this MeasureUnit, as defined in UTS 35. <br /> | | [MeasureUnit.MeasurePrefix](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.MeasurePrefix)! | [getPrefix](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getPrefix())`()` <br /> Returns the current SI or binary prefix of this SINGLE unit. For example, if the unit has the prefix "kilo", then MeasurePrefix.KILO is returned. NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an error will occur. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSubtype](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getSubtype())`()` <br /> Get the subType, such as "foot". May return null. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#getType())`()` <br /> Get the type, such as "length". May return null. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#hashCode())`()` <br /> Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by [java.util.HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#). The general contract of`hashCode`is: - Whenever it is invoked on the same object more than once during an execution of a Java application, the`hashCode`method must consistently return the same integer, provided no information used in`equals`comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application. - If two objects are equal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce the same integer result. - It is*not* required that if two objects are unequal according to the [equals](https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any))method, then calling the`hashCode`method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables. <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [product](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#product(android.icu.util.MeasureUnit))`(`other:` ` [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!`)` <br /> Computes the product of this unit with another unit. This is a way to build units from constituent parts. The numerator and denominator are preserved through this operation. For example, if the receiver is "kilowatt" and the argument is "hour-per-day", then the unit "kilowatt-hour-per-day" is returned. NOTE: Only works on SINGLE and COMPOUND units. If either unit (receivee and argument) is a MIXED unit, an error will occur. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [reciprocal](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#reciprocal())`()` <br /> Computes the reciprocal of this MeasureUnit, with the numerator and denominator flipped. For example, if the receiver is "meter-per-second", the unit "second-per-meter" is returned. NOTE: Only works on SINGLE and COMPOUND units. If this is a MIXED unit, an error will occur. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)!>! | [splitToSingleUnits](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#splitToSingleUnits())`()` <br /> Returns the list of SINGLE units contained within a sequence of COMPOUND units. Examples: - Given "meter-kilogram-per-second", three units will be returned: "meter", "kilogram", and "per-second". - Given "hour+minute+second", three units will be returned: "hour", "minute", and "second". If this is a SINGLE unit, a list of length 1 will be returned. <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [withDimensionality](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#withDimensionality(kotlin.Int))`(`dimensionality:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a MeasureUnit which is this SINGLE unit augmented with the specified dimensionality (power). For example, if dimensionality is 2, the unit will be squared. NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an exception is thrown. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [withPrefix](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#withPrefix(android.icu.util.MeasureUnit.MeasurePrefix))`(`prefix:` ` [MeasureUnit.MeasurePrefix](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.MeasurePrefix)!`)` <br /> Creates a MeasureUnit which is this SINGLE unit augmented with the specified prefix. For example, MeasurePrefix.KILO for "kilo", or MeasurePrefix.KIBI for "kibi". May return`this`if this unit already has that prefix. There is sufficient locale data to format all standard prefixes. NOTE: Only works on SINGLE units. If this is a COMPOUND or MIXED unit, an error will occur. For more information, [Complexity](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit.Complexity). <br /> | ||

| Inherited properties ||
|---|---|
| From class [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit) |---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ACRE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ACRE:android.icu.util.MeasureUnit) <br /> Constant for unit of area: acre <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ACRE_FOOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ACRE_FOOT:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: acre-foot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [AMPERE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#AMPERE:android.icu.util.MeasureUnit) <br /> Constant for unit of electric: ampere <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ARC_MINUTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ARC_MINUTE:android.icu.util.MeasureUnit) <br /> Constant for unit of angle: arc-minute <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ARC_SECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ARC_SECOND:android.icu.util.MeasureUnit) <br /> Constant for unit of angle: arc-second <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ASTRONOMICAL_UNIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ASTRONOMICAL_UNIT:android.icu.util.MeasureUnit) <br /> Constant for unit of length: astronomical-unit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ATMOSPHERE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ATMOSPHERE:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: atmosphere <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [BEAUFORT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#BEAUFORT:android.icu.util.MeasureUnit) <br /> Constant for unit of speed: beaufort <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [BIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#BIT:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: bit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [BUSHEL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#BUSHEL:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: bushel <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [BYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#BYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: byte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CALORIE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CALORIE:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: calorie <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CANDELA](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CANDELA:android.icu.util.MeasureUnit) <br /> Constant for unit of light: candela <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CARAT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CARAT:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: carat <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CELSIUS](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CELSIUS:android.icu.util.MeasureUnit) <br /> Constant for unit of temperature: celsius <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CENTILITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CENTILITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: centiliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CENTIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CENTIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: centimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CENTURY](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CENTURY:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: century <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_CENTIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_CENTIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-centimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_FOOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_FOOT:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-foot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_KILOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_KILOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_METER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_METER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-meter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_MILE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_MILE:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-mile <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUBIC_YARD](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUBIC_YARD:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cubic-yard <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUP](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUP:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cup <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [CUP_METRIC](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#CUP_METRIC:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: cup-metric <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [DAY](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DAY:android.icu.util.TimeUnit) <br /> Constant for unit of duration: day <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DECADE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DECADE:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: decade <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DECILITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DECILITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: deciliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DECIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DECIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: decimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DEGREE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DEGREE:android.icu.util.MeasureUnit) <br /> Constant for unit of angle: degree <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DOT:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: dot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DOT_PER_CENTIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DOT_PER_CENTIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: dot-per-centimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [DOT_PER_INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#DOT_PER_INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: dot-per-inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [EM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#EM:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: em <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FAHRENHEIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FAHRENHEIT:android.icu.util.MeasureUnit) <br /> Constant for unit of temperature: fahrenheit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FATHOM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FATHOM:android.icu.util.MeasureUnit) <br /> Constant for unit of length: fathom <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FLUID_OUNCE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FLUID_OUNCE:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: fluid-ounce <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FOODCALORIE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FOODCALORIE:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: foodcalorie <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FOOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FOOT:android.icu.util.MeasureUnit) <br /> Constant for unit of length: foot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [FURLONG](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#FURLONG:android.icu.util.MeasureUnit) <br /> Constant for unit of length: furlong <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GALLON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GALLON:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: gallon <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GALLON_IMPERIAL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GALLON_IMPERIAL:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: gallon-imperial <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GASOLINE_ENERGY_DENSITY](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GASOLINE_ENERGY_DENSITY:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: gasoline-energy-density <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GENERIC_TEMPERATURE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GENERIC_TEMPERATURE:android.icu.util.MeasureUnit) <br /> Constant for unit of temperature: generic <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GIGABIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GIGABIT:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: gigabit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GIGABYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GIGABYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: gigabyte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GIGAHERTZ](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GIGAHERTZ:android.icu.util.MeasureUnit) <br /> Constant for unit of frequency: gigahertz <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GIGAWATT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GIGAWATT:android.icu.util.MeasureUnit) <br /> Constant for unit of power: gigawatt <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [GRAM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#GRAM:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: gram <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [G_FORCE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#G_FORCE:android.icu.util.MeasureUnit) <br /> Constant for unit of acceleration: g-force <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [HECTARE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HECTARE:android.icu.util.MeasureUnit) <br /> Constant for unit of area: hectare <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [HECTOLITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HECTOLITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: hectoliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [HECTOPASCAL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HECTOPASCAL:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: hectopascal <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [HERTZ](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HERTZ:android.icu.util.MeasureUnit) <br /> Constant for unit of frequency: hertz <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [HORSEPOWER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HORSEPOWER:android.icu.util.MeasureUnit) <br /> Constant for unit of power: horsepower <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [HOUR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#HOUR:android.icu.util.TimeUnit) <br /> Constant for unit of duration: hour <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of length: inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [INCH_HG](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#INCH_HG:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: inch-ofhg <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [ITEM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#ITEM:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: item <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [JOULE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#JOULE:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: joule <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KARAT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KARAT:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: karat <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KELVIN](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KELVIN:android.icu.util.MeasureUnit) <br /> Constant for unit of temperature: kelvin <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOBIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOBIT:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: kilobit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOBYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOBYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: kilobyte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOCALORIE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOCALORIE:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: kilocalorie <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOGRAM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOGRAM:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: kilogram <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOHERTZ](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOHERTZ:android.icu.util.MeasureUnit) <br /> Constant for unit of frequency: kilohertz <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOJOULE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOJOULE:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: kilojoule <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOMETER_PER_HOUR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOMETER_PER_HOUR:android.icu.util.MeasureUnit) <br /> Constant for unit of speed: kilometer-per-hour <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOWATT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOWATT:android.icu.util.MeasureUnit) <br /> Constant for unit of power: kilowatt <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOWATT_HOUR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOWATT_HOUR:android.icu.util.MeasureUnit) <br /> Constant for unit of energy: kilowatt-hour <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KILOWATT_HOUR_PER_100_KILOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KILOWATT_HOUR_PER_100_KILOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of force: kilowatt-hour-per-100-kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [KNOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#KNOT:android.icu.util.MeasureUnit) <br /> Constant for unit of speed: knot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LIGHT_YEAR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LIGHT_YEAR:android.icu.util.MeasureUnit) <br /> Constant for unit of length: light-year <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: liter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LITER_PER_100KILOMETERS](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LITER_PER_100KILOMETERS:android.icu.util.MeasureUnit) <br /> Constant for unit of consumption: liter-per-100-kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LITER_PER_KILOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LITER_PER_KILOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of consumption: liter-per-kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LUMEN](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LUMEN:android.icu.util.MeasureUnit) <br /> Constant for unit of light: lumen <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [LUX](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#LUX:android.icu.util.MeasureUnit) <br /> Constant for unit of light: lux <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGABIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGABIT:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: megabit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGABYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGABYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: megabyte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGAHERTZ](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGAHERTZ:android.icu.util.MeasureUnit) <br /> Constant for unit of frequency: megahertz <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGALITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGALITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: megaliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGAPIXEL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGAPIXEL:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: megapixel <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MEGAWATT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MEGAWATT:android.icu.util.MeasureUnit) <br /> Constant for unit of power: megawatt <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [METER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#METER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: meter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [METER_PER_SECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#METER_PER_SECOND:android.icu.util.MeasureUnit) <br /> Constant for unit of speed: meter-per-second <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [METER_PER_SECOND_SQUARED](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#METER_PER_SECOND_SQUARED:android.icu.util.MeasureUnit) <br /> Constant for unit of acceleration: meter-per-square-second <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [METRIC_TON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#METRIC_TON:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: metric-ton (renamed to tonne in CLDR 42 / ICU 72). Note: In ICU 74 this will be deprecated in favor of TONNE, which is currently draft but will become stable in ICU 74, and which uses the preferred naming. <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MICROGRAM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MICROGRAM:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: microgram <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MICROMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MICROMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: micrometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MICROSECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MICROSECOND:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: microsecond <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILE:android.icu.util.MeasureUnit) <br /> Constant for unit of length: mile <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILE_PER_GALLON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILE_PER_GALLON:android.icu.util.MeasureUnit) <br /> Constant for unit of consumption: mile-per-gallon <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILE_PER_GALLON_IMPERIAL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILE_PER_GALLON_IMPERIAL:android.icu.util.MeasureUnit) <br /> Constant for unit of consumption: mile-per-gallon-imperial <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILE_PER_HOUR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILE_PER_HOUR:android.icu.util.MeasureUnit) <br /> Constant for unit of speed: mile-per-hour <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILE_SCANDINAVIAN](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILE_SCANDINAVIAN:android.icu.util.MeasureUnit) <br /> Constant for unit of length: mile-scandinavian <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIAMPERE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIAMPERE:android.icu.util.MeasureUnit) <br /> Constant for unit of electric: milliampere <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIBAR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIBAR:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: millibar <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIGRAM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIGRAM:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: milligram <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIGRAM_OFGLUCOSE_PER_DECILITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIGRAM_OFGLUCOSE_PER_DECILITER:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: milligram-ofglucose-per-deciliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIGRAM_PER_DECILITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIGRAM_PER_DECILITER:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: milligram-per-deciliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLILITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLILITER:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: milliliter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: millimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIMETER_OF_MERCURY](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIMETER_OF_MERCURY:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: millimeter-ofhg <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIMOLE_PER_LITER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIMOLE_PER_LITER:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: millimole-per-liter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLISECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLISECOND:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: millisecond <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [MILLIWATT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MILLIWATT:android.icu.util.MeasureUnit) <br /> Constant for unit of power: milliwatt <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [MINUTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MINUTE:android.icu.util.TimeUnit) <br /> Constant for unit of duration: minute <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [MONTH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#MONTH:android.icu.util.TimeUnit) <br /> Constant for unit of duration: month <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [NANOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#NANOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: nanometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [NANOSECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#NANOSECOND:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: nanosecond <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [NAUTICAL_MILE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#NAUTICAL_MILE:android.icu.util.MeasureUnit) <br /> Constant for unit of length: nautical-mile <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [OHM](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#OHM:android.icu.util.MeasureUnit) <br /> Constant for unit of electric: ohm <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [OUNCE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#OUNCE:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: ounce <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [OUNCE_TROY](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#OUNCE_TROY:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: ounce-troy <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PARSEC](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PARSEC:android.icu.util.MeasureUnit) <br /> Constant for unit of length: parsec <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PART_PER_MILLION](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PART_PER_MILLION:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: permillion <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PERCENT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PERCENT:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: percent <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PERMILLE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PERMILLE:android.icu.util.MeasureUnit) <br /> Constant for unit of concentr: permille <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PETABYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PETABYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: petabyte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PICOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PICOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of length: picometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PINT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PINT:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: pint <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PINT_METRIC](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PINT_METRIC:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: pint-metric <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PIXEL](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PIXEL:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: pixel <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PIXEL_PER_CENTIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PIXEL_PER_CENTIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: pixel-per-centimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [PIXEL_PER_INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#PIXEL_PER_INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of graphics: pixel-per-inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [POINT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#POINT:android.icu.util.MeasureUnit) <br /> Constant for unit of length: point <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [POUND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#POUND:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: pound <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [POUND_PER_SQUARE_INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#POUND_PER_SQUARE_INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of pressure: pound-force-per-square-inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [QUART](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#QUART:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: quart <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [QUARTER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#QUARTER:android.icu.util.MeasureUnit) <br /> Constant for unit of duration: quarter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [RADIAN](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#RADIAN:android.icu.util.MeasureUnit) <br /> Constant for unit of angle: radian <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [REVOLUTION_ANGLE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#REVOLUTION_ANGLE:android.icu.util.MeasureUnit) <br /> Constant for unit of angle: revolution <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [SECOND](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SECOND:android.icu.util.TimeUnit) <br /> Constant for unit of duration: second <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_CENTIMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_CENTIMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-centimeter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_FOOT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_FOOT:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-foot <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_INCH](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_INCH:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-inch <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_KILOMETER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_KILOMETER:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-kilometer <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_METER](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_METER:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-meter <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_MILE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_MILE:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-mile <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [SQUARE_YARD](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#SQUARE_YARD:android.icu.util.MeasureUnit) <br /> Constant for unit of area: square-yard <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [STONE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#STONE:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: stone <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TABLESPOON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TABLESPOON:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: tablespoon <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TEASPOON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TEASPOON:android.icu.util.MeasureUnit) <br /> Constant for unit of volume: teaspoon <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TERABIT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TERABIT:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: terabit <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TERABYTE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TERABYTE:android.icu.util.MeasureUnit) <br /> Constant for unit of digital: terabyte <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TON](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TON:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: ton <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [TONNE](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#TONNE:android.icu.util.MeasureUnit) <br /> Constant for unit of mass: tonne <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [VOLT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#VOLT:android.icu.util.MeasureUnit) <br /> Constant for unit of electric: volt <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [WATT](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#WATT:android.icu.util.MeasureUnit) <br /> Constant for unit of power: watt <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [WEEK](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#WEEK:android.icu.util.TimeUnit) <br /> Constant for unit of duration: week <br /> | | [MeasureUnit](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit)! | [YARD](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#YARD:android.icu.util.MeasureUnit) <br /> Constant for unit of length: yard <br /> | | [TimeUnit](https://developer.android.com/reference/kotlin/android/icu/util/TimeUnit)! | [YEAR](https://developer.android.com/reference/kotlin/android/icu/util/MeasureUnit#YEAR:android.icu.util.TimeUnit) <br /> Constant for unit of duration: year <br /> | ||

## Constants

### FORMAL_SYMBOL_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FORMAL_SYMBOL_NAME: Int
```

Selector for getName() indicating the formal currency symbol.

The formal currency symbol is similar to the regular currency symbol, but it always takes the form used in formal settings such as banking; for example, "NT$" instead of "$" for TWD in zh-TW. 

 Value: 4

### LONG_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LONG_NAME: Int
```

Selector for getName() indicating the long name for a currency, such as "US Dollar" for USD. 

 Value: 1

### NARROW_SYMBOL_NAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NARROW_SYMBOL_NAME: Int
```

Selector for getName() indicating the narrow currency symbol.

The narrow currency symbol is similar to the regular currency symbol, but it always takes the shortest form; for example, "$" instead of "US$" for USD in en-CA. 

 Value: 3

### PLURAL_LONG_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLURAL_LONG_NAME: Int
```

Selector for getName() indicating the plural long name for a currency, such as "US dollar" for USD in "1 US dollar", and "US dollars" for USD in "2 US dollars". 

 Value: 2

### SYMBOL_NAME

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYMBOL_NAME: Int
```

Selector for getName() indicating a symbolic name for a currency, such as "$" for USD. 

 Value: 0

### VARIANT_SYMBOL_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VARIANT_SYMBOL_NAME: Int
```

Selector for getName() indicating the variant currency symbol.

The variant symbol for a currency is an alternative symbol that is not necessarily as widely used as the regular symbol. 

 Value: 5

## Protected constructors

### Currency

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Currency(theISOCode: String!)
```

Constructs a currency object for the given ISO 4217 3-letter code. This constructor assumes that the code is valid.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| `theISOCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The iso code used to construct the currency. |

## Public methods

### fromJavaCurrency

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fromJavaCurrency(currency: Currency!): Currency!
```

Returns a Currency object based on the currency represented by the given java.util.Currency.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------|
| `currency` | [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)!:The Java currency object to convert. |

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | An equivalent ICU currency object. |

### getAvailableCurrencies

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableCurrencies(): MutableSet<Currency!>!
```

Returns the set of available currencies. The returned set of currencies contains all of the available currencies, including obsolete ones. The result set can be modified without affecting the available currencies in the runtime.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)!>! | The set of available currencies. The returned set could be empty if there is no currency data available. |

### getAvailableCurrencyCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableCurrencyCodes(
    loc: ULocale!, 
    d: Date!
): Array<String!>!
```

Returns an array of Strings which contain the currency identifiers that are valid for the given locale on the given date. If there are no such identifiers, returns null. Returned identifiers are in preference order.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!:the locale for which to retrieve currency codes. |
| `d` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:the date for which to retrieve currency codes for the given locale. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The array of ISO currency codes. |

### getAvailableCurrencyCodes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableCurrencyCodes(
    loc: Locale!, 
    d: Date!
): Array<String!>!
```

Returns an array of Strings which contain the currency identifiers that are valid for the given [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) on the given date. If there are no such identifiers, returns null. Returned identifiers are in preference order.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) for which to retrieve currency codes. |
| `d` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:the date for which to retrieve currency codes for the given locale. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The array of ISO currency codes. |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableLocales(): Array<Locale!>!
```

Return an array of the locales for which a currency is defined.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | an array of the available locales |

### getAvailableULocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAvailableULocales(): Array<ULocale!>!
```

Return an array of the ulocales for which a currency is defined.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!>! | an array of the available ulocales |

### getCurrencyCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCurrencyCode(): String!
```

Returns the ISO 4217 3-letter code for this currency object. 

### getDefaultFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultFractionDigits(): Int
```

Returns the number of the number of fraction digits that should be displayed for this currency. This is equivalent to getDefaultFractionDigits(CurrencyUsage.STANDARD); Important: The number of fraction digits for a given currency is NOT guaranteed to be constant across versions of ICU or CLDR. For example, do NOT use this value as a mechanism for deciding the magnitude used to store currency values in a database. You should use this value for display purposes only.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative number of fraction digits to be displayed |

### getDefaultFractionDigits

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDefaultFractionDigits(Usage: Currency.CurrencyUsage!): Int
```

Returns the number of the number of fraction digits that should be displayed for this currency with Usage. Important: The number of fraction digits for a given currency is NOT guaranteed to be constant across versions of ICU or CLDR. For example, do NOT use this value as a mechanism for deciding the magnitude used to store currency values in a database. You should use this value for display purposes only.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Usage` | [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage)!:the usage of currency(Standard or Cash) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a non-negative number of fraction digits to be displayed |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(): String!
```

Returns the display name for this currency in the default locale. If the resource data for the default locale contains no entry for this currency, then the ISO 4217 code is returned.

Note: This method is a convenience equivalent for [java.util.Currency#getDisplayName()](https://developer.android.com/reference/kotlin/java/util/Currency.html#getDisplayName())and is equivalent to`getName(Locale.getDefault(), LONG_NAME, null)`.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name of this currency |

**See Also**

- [#getDisplayName(Locale)](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDisplayName(java.util.Locale))
- [#getName(Locale, int, boolean[])](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(java.util.Locale,%20kotlin.Int,%20kotlin.BooleanArray)) 

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayName(locale: Locale!): String!
```

Returns the display name for this currency in the given locale. If the resource data for the given locale contains no entry for this currency, then the ISO 4217 code is returned.

Note: This method is a convenience equivalent for [java.util.Currency#getDisplayName(java.util.Locale)](https://developer.android.com/reference/kotlin/java/util/Currency.html#getDisplayName(java.util.Locale))and is equivalent to`getName(locale, LONG_NAME, null)`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:locale in which to display currency |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The display name of this currency for the specified locale |

**See Also**

- [#getDisplayName(Locale)](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getDisplayName(java.util.Locale))
- [#getName(Locale, int, boolean[])](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(java.util.Locale,%20kotlin.Int,%20kotlin.BooleanArray)) 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: ULocale!): Currency!
```

Returns a currency object for the default currency in the given locale. 

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(theISOCode: String!): Currency!
```

Returns a currency object given an ISO 4217 3-letter code.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------|
| `theISOCode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the iso code |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | the currency for this iso code |

| Exceptions ||
|--------------------------------------|---------------------------------------------|
| `java.lang.NullPointerException` | if`theISOCode`is null. |
| `java.lang.IllegalArgumentException` | if`theISOCode`is not a 3-letter alpha code. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(locale: Locale!): Currency!
```

Returns a currency object for the default currency in the given locale.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale |

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/android/icu/util/Currency#)! | the currency object for this locale |

### getKeywordValuesForLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getKeywordValuesForLocale(
    key: String!, 
    locale: ULocale!, 
    commonlyUsed: Boolean
): Array<String!>!
```

Given a key and a locale, returns an array of values for the key for which data exists. If commonlyUsed is true, these are the values that typically are used with this locale, otherwise these are all values for which data exists. This is a common service API.

The only supported key is "currency", other values return an empty array.

Currency information is based on the region of the locale. If the locale does not indicate a region, [ULocale.addLikelySubtags(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#addLikelySubtags(android.icu.util.ULocale))is used to infer a region, except for the 'und' locale.

If commonlyUsed is true, only the currencies known to be in use as of the current date are returned. When there are more than one, these are returned in preference order (typically, this occurs when a country is transitioning to a new currency, and the newer currency is preferred), see [Unicode TR#35 Sec. C1](http://unicode.org/reports/tr35/#Supplemental_Currency_Data). If commonlyUsed is false, all currencies ever used in any locale are returned, in no particular order.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:key whose values to look up. the only recognized key is "currency" |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!:the locale |
| `commonlyUsed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, return only values that are currently used in the locale. Otherwise returns all values. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of values for the given key and the locale. If there is no data, the array will be empty. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(
    locale: ULocale!, 
    nameStyle: Int, 
    isChoiceFormat: BooleanArray!
): String!
```

Returns the display name for the given currency in the given locale. For example, the display name for the USD currency object in the en_US locale is "$".

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!:locale in which to display currency |
| `nameStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector for which kind of name to return. The nameStyle should be SYMBOL_NAME, NARROW_SYMBOL_NAME, or LONG_NAME. Otherwise, throw IllegalArgumentException. |
| `isChoiceFormat` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:isChoiceFormat\[0\] is always set to false, or isChoiceFormat can be null; display names are static strings; since ICU 4.4, ChoiceFormat patterns are no longer supported |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | display string for this currency. If the resource data contains no entry for this currency, then the ISO 4217 code is returned. <br /> |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the nameStyle is not SYMBOL_NAME or LONG_NAME. |

**See Also**

- [#getName(ULocale, int, String, boolean[])](https://developer.android.com/reference/kotlin/android/icu/util/Currency#getName(android.icu.util.ULocale,%20kotlin.Int,%20kotlin.String,%20kotlin.BooleanArray)) 

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(
    locale: ULocale!, 
    nameStyle: Int, 
    pluralCount: String!, 
    isChoiceFormat: BooleanArray!
): String!
```

Returns the display name for the given currency in the given locale. For example, the SYMBOL_NAME for the USD currency object in the en_US locale is "$". The PLURAL_LONG_NAME for the USD currency object when the currency amount is plural is "US dollars", such as in "3.00 US dollars"; while the PLURAL_LONG_NAME for the USD currency object when the currency amount is singular is "US dollar", such as in "1.00 US dollar".

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!:locale in which to display currency |
| `nameStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector for which kind of name to return |
| `pluralCount` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:plural count string for this locale |
| `isChoiceFormat` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:isChoiceFormat\[0\] is always set to false, or isChoiceFormat can be null; display names are static strings; since ICU 4.4, ChoiceFormat patterns are no longer supported |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | display string for this currency. If the resource data contains no entry for this currency, then the ISO 4217 code is returned. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the nameStyle is not SYMBOL_NAME, LONG_NAME, or PLURAL_LONG_NAME. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(
    locale: Locale!, 
    nameStyle: Int, 
    isChoiceFormat: BooleanArray!
): String!
```

Returns the display name for the given currency in the given locale. This is a convenient method for getName(ULocale, int, boolean\[\]);

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:locale in which to display currency |
| `nameStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector for which kind of name to return. The nameStyle should be SYMBOL_NAME, NARROW_SYMBOL_NAME, or LONG_NAME. Otherwise, throw IllegalArgumentException. |
| `isChoiceFormat` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:isChoiceFormat\[0\] is always set to false, or isChoiceFormat can be null; display names are static strings; since ICU 4.4, ChoiceFormat patterns are no longer supported |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | display string for this currency. If the resource data contains no entry for this currency, then the ISO 4217 code is returned. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getName(
    locale: Locale!, 
    nameStyle: Int, 
    pluralCount: String!, 
    isChoiceFormat: BooleanArray!
): String!
```

Returns the display name for the given currency in the given locale. This is a convenience overload of getName(ULocale, int, String, boolean\[\]);

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:locale in which to display currency |
| `nameStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):selector for which kind of name to return |
| `pluralCount` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:plural count string for this locale |
| `isChoiceFormat` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:isChoiceFormat\[0\] is always set to false, or isChoiceFormat can be null; display names are static strings; since ICU 4.4, ChoiceFormat patterns are no longer supported |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | display string for this currency. If the resource data contains no entry for this currency, then the ISO 4217 code is returned. |

### getNumericCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumericCode(): Int
```

Returns the ISO 4217 numeric code for this currency object.

Note: If the ISO 4217 numeric code is not assigned for the currency or the currency is unknown, this method returns 0.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The ISO 4217 numeric code of this currency. |

### getRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundingIncrement(): Double
```

Returns the rounding increment for this currency, or 0.0 if no rounding is done by this currency. This is equivalent to getRoundingIncrement(CurrencyUsage.STANDARD);

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the non-negative rounding increment, or 0.0 if none |

### getRoundingIncrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundingIncrement(Usage: Currency.CurrencyUsage!): Double
```

Returns the rounding increment for this currency, or 0.0 if no rounding is done by this currency with the Usage.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `Usage` | [Currency.CurrencyUsage](https://developer.android.com/reference/kotlin/android/icu/util/Currency.CurrencyUsage)!:the usage of currency(Standard or Cash) |

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the non-negative rounding increment, or 0.0 if none |

### getSymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSymbol(): String!
```

Convenience and compatibility override of getName that requests the symbol name for the default`DISPLAY`locale. 
**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getSymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSymbol(uloc: ULocale!): String!
```

Convenience and compatibility override of getName that requests the symbol name.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `uloc` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale)!:the ULocale for the symbol |

**See Also**

### getSymbol

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSymbol(loc: Locale!): String!
```

Convenience and compatibility override of getName that requests the symbol name.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the Locale for the symbol |

**See Also**

### isAvailable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isAvailable(
    code: String!, 
    from: Date!, 
    to: Date!
): Boolean
```

Queries if the given ISO 4217 3-letter code is available on the specified date range.

Note: For checking availability of a currency on a specific date, specify the date on both`from`and`to`. When both`from`and`to`are null, this method checks if the specified currency is available all time.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The ISO 4217 3-letter code. |
| `from` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:The lower bound of the date range, inclusive. When`from`is null, check the availability of the currency any date before`to` |
| `to` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:The upper bound of the date range, inclusive. When`to`is null, check the availability of the currency any date after`from` |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the given ISO 4217 3-letter code is supported on the specified date range. |

| Exceptions ||
|--------------------------------------|--------------------------|
| `java.lang.IllegalArgumentException` | when`to`is before`from`. |

### toJavaCurrency

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toJavaCurrency(): Currency!
```

Returns a java.util.Currency object based on the currency represented by this Currency.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------|
| [Currency](https://developer.android.com/reference/kotlin/java/util/Currency.html#)! | An equivalent Java currency object. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the ISO 4217 code for this currency.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
