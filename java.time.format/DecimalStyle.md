# DecimalStyle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DecimalStyle

```
class DecimalStyle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.time.format.DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#) |

Localized decimal style used in date and time formatting.

A significant part of dealing with dates and times is the localization. This class acts as a central point for accessing the information.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Checks if this DecimalStyle is equal to another DecimalStyle. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#getAvailableLocales())`()` Lists all the locales that are supported. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDecimalSeparator](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#getDecimalSeparator())`()` Gets the character that represents the decimal point. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getNegativeSign](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#getNegativeSign())`()` Gets the character that represents the negative sign. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getPositiveSign](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#getPositiveSign())`()` Gets the character that represents the positive sign. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getZeroDigit](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#getZeroDigit())`()` Gets the character that represents zero. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#hashCode())`()` A hash code for this DecimalStyle. |
| static [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [of](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#of(java.util.Locale))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` Obtains the DecimalStyle for the specified locale. |
| static [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [ofDefaultLocale](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#ofDefaultLocale())`()` Obtains the DecimalStyle for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#toString())`()` Returns a string describing this DecimalStyle. |
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [withDecimalSeparator](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#withDecimalSeparator(kotlin.Char))`(`decimalSeparator:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns a copy of the info with a new character that represents the decimal point. |
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [withNegativeSign](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#withNegativeSign(kotlin.Char))`(`negativeSign:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns a copy of the info with a new character that represents the negative sign. |
| --- | --- |
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [withPositiveSign](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#withPositiveSign(kotlin.Char))`(`positiveSign:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns a copy of the info with a new character that represents the positive sign. |
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [withZeroDigit](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#withZeroDigit(kotlin.Char))`(`zeroDigit:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns a copy of the info with a new character that represents zero. |

| Properties ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | [STANDARD](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#STANDARD:java.time.format.DecimalStyle) The standard set of non-localized decimal style symbols. |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Checks if this DecimalStyle is equal to another DecimalStyle.

| Parameters ||
|-------|-----------------------------------------|
| `obj` | the object to check, null returns false |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is equal to the other date |

### getAvailableLocales

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableLocales(): MutableSet<Locale!>!
```

Lists all the locales that are supported.

The locale 'en_US' will always be present.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!>! | a Set of Locales for which localization is supported |

### getDecimalSeparator

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDecimalSeparator(): Char
```

Gets the character that represents the decimal point.

The character used to represent a decimal point may vary by culture. This method specifies the character to use.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character for the decimal point |

### getNegativeSign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNegativeSign(): Char
```

Gets the character that represents the negative sign.

The character used to represent a negative number may vary by culture. This method specifies the character to use.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character for the negative sign |

### getPositiveSign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPositiveSign(): Char
```

Gets the character that represents the positive sign.

The character used to represent a positive number may vary by culture. This method specifies the character to use.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character for the positive sign |

### getZeroDigit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getZeroDigit(): Char
```

Gets the character that represents zero.

The character used to represent digits may vary by culture. This method specifies the zero character to use, which implies the characters for one to nine.

| Return ||
|------------------------------------------------------------------------------|------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the character for zero |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

A hash code for this DecimalStyle.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a suitable hash code |

### of

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun of(locale: Locale!): DecimalStyle!
```

Obtains the DecimalStyle for the specified locale.

This method provides access to locale sensitive decimal style symbols. If the locale contains "nu" (Numbering System) [Unicode extensions](https://developer.android.com/reference/kotlin/java/util/Locale.html#def_locale_extension), returned instance will reflect the values specified with those extensions.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:the locale, not null |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | the decimal style, not null |

### ofDefaultLocale

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofDefaultLocale(): DecimalStyle!
```

Obtains the DecimalStyle for the default [FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) locale.

This method provides access to locale sensitive decimal style symbols.

This is equivalent to calling [of(Locale.getDefault(Locale.Category.FORMAT))](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#of(java.util.Locale)).

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | the decimal style, not null |

**See Also**

- [java.util.Locale.Category#FORMAT](https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#) 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this DecimalStyle.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string description, not null |

### withDecimalSeparator

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withDecimalSeparator(decimalSeparator: Char): DecimalStyle!
```

Returns a copy of the info with a new character that represents the decimal point.

The character used to represent a decimal point may vary by culture. This method specifies the character to use.

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------|
| `decimalSeparator` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character for the decimal point |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | a copy with a new character that represents the decimal point, not null |

### withNegativeSign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withNegativeSign(negativeSign: Char): DecimalStyle!
```

Returns a copy of the info with a new character that represents the negative sign.

The character used to represent a negative number may vary by culture. This method specifies the character to use.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `negativeSign` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character for the negative sign |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | a copy with a new character that represents the negative sign, not null |

### withPositiveSign

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withPositiveSign(positiveSign: Char): DecimalStyle!
```

Returns a copy of the info with a new character that represents the positive sign.

The character used to represent a positive number may vary by culture. This method specifies the character to use.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------|
| `positiveSign` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character for the positive sign |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | a copy with a new character that represents the positive sign, not null |

### withZeroDigit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun withZeroDigit(zeroDigit: Char): DecimalStyle!
```

Returns a copy of the info with a new character that represents zero.

The character used to represent digits may vary by culture. This method specifies the zero character to use, which implies the characters for one to nine.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------|
| `zeroDigit` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the character for zero |

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [DecimalStyle](https://developer.android.com/reference/kotlin/java/time/format/DecimalStyle#)! | a copy with a new character that represents zero, not null |

## Properties

### STANDARD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STANDARD: DecimalStyle!
```

The standard set of non-localized decimal style symbols.

This uses standard ASCII characters for zero, positive, negative and a dot for the decimal point.
