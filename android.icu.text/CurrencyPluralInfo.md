Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CurrencyPluralInfo

Kotlin | [Java](CurrencyPluralInfo.md)
| --- | --- |

```
open class CurrencyPluralInfo : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.CurrencyPluralInfo](CurrencyPluralInfo.md) |

This class represents the information needed by DecimalFormat to format currency plural, such as "3.00 US dollars" or "1.00 US dollar". DecimalFormat creates for itself an instance of CurrencyPluralInfo from its locale data. If you need to change any of these symbols, you can get the CurrencyPluralInfo object from your DecimalFormat and modify it. Following are the information needed for currency plural format and parse: locale information, plural rule of the locale, currency plural pattern of the locale.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#CurrencyPluralInfo()()` Create a CurrencyPluralInfo object for the default `FORMAT` locale. |
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#CurrencyPluralInfo(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Create a CurrencyPluralInfo object for the given locale. |
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#CurrencyPluralInfo(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Create a CurrencyPluralInfo object for the given locale. |

| Public methods ||
|---|---|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#clone()()` Standard override |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Override equals |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getCurrencyPluralPattern(kotlin.String)(pluralCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Given a plural count, gets currency plural pattern of this locale, used for currency plural format |
| --- | --- |
| open static [CurrencyPluralInfo](CurrencyPluralInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getInstance()()` Gets a CurrencyPluralInfo instance for the default locale. |
| open static [CurrencyPluralInfo](CurrencyPluralInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getInstance(android.icu.util.ULocale)(locale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Gets a CurrencyPluralInfo instance for the given locale. |
| open static [CurrencyPluralInfo](CurrencyPluralInfo.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getInstance(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Gets a CurrencyPluralInfo instance for the given locale. |
| --- | --- |
| open [ULocale](../android.icu.util/ULocale.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getLocale()()` Get locale |
| open [PluralRules](PluralRules.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#getPluralRules()()` Gets plural rules of this locale, used for currency plural format |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#hashCode()()` Override hashCode |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#setCurrencyPluralPattern(kotlin.String,%20kotlin.String)(pluralCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, pattern: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set currency plural patterns. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#setLocale(android.icu.util.ULocale)(loc: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Set locale. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#setPluralRules(kotlin.String)(ruleDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set plural rules. |
| --- | --- |

## Public constructors

### CurrencyPluralInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CurrencyPluralInfo()
```

Create a CurrencyPluralInfo object for the default `FORMAT` locale.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### CurrencyPluralInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CurrencyPluralInfo(locale: ULocale!)
```

Create a CurrencyPluralInfo object for the given locale.

| Parameters ||
|---|---|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the locale |

### CurrencyPluralInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CurrencyPluralInfo(locale: Locale!)
```

Create a CurrencyPluralInfo object for the given locale.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the locale |

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Standard override

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Override equals

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCurrencyPluralPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrencyPluralPattern(pluralCount: String!): String!
```

Given a plural count, gets currency plural pattern of this locale, used for currency plural format

| Parameters ||
|---|---|
| `pluralCount` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: currency plural count |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a currency plural pattern based on plural count |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): CurrencyPluralInfo!
```

Gets a CurrencyPluralInfo instance for the default locale.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#!` | A CurrencyPluralInfo instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: ULocale!): CurrencyPluralInfo!
```

Gets a CurrencyPluralInfo instance for the given locale.

| Parameters ||
|---|---|
| `locale` | [ULocale](../android.icu.util/ULocale.md)!: the locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#!` | A CurrencyPluralInfo instance. |

### getInstance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: Locale!): CurrencyPluralInfo!
```

Gets a CurrencyPluralInfo instance for the given locale.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: the locale. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo#!` | A CurrencyPluralInfo instance. |

### getLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocale(): ULocale!
```

Get locale

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!` | locale |

### getPluralRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPluralRules(): PluralRules!
```

Gets plural rules of this locale, used for currency plural format

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/PluralRules!` | plural rule |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Override hashCode

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### setCurrencyPluralPattern

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCurrencyPluralPattern(
    pluralCount: String!, 
    pattern: String!
): Unit
```

Set currency plural patterns. These are initially set in the constructor based on the locale, and usually do not need to be changed. The decimal digits part of the pattern cannot be specified via this method. All plural forms will use the same decimal pattern as set in the constructor of DecimalFormat. For example, you can't set "0.0" for plural "few" but "0.00" for plural "many".

| Parameters ||
|---|---|
| `pluralCount` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the plural count for which the currency pattern will be overridden. |
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the new currency plural pattern |

### setLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLocale(loc: ULocale!): Unit
```

Set locale. This also sets both the plural rules and the currency plural patterns to be the defaults for the locale.

| Parameters ||
|---|---|
| `loc` | [ULocale](../android.icu.util/ULocale.md)!: the new locale to set |

### setPluralRules

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPluralRules(ruleDescription: String!): Unit
```

Set plural rules. These are initially set in the constructor based on the locale, and usually do not need to be changed.

| Parameters ||
|---|---|
| `ruleDescription` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: new plural rule description |
