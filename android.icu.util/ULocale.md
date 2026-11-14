# ULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ULocale

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/ULocale "View this page in Java") 

```
class ULocale : Comparable<ULocale!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.icu.util.ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#) |

**\[icu enhancement\]** ICU's replacement for [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). Methods, fields, and other functionality specific to ICU are labeled '**\[icu\]** '. A class analogous to [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) that provides additional support for ICU protocol. In ICU 3.0 this class is enhanced to support RFC 3066 language identifiers.

Many classes and services in ICU follow a factory idiom, in which a factory method or object responds to a client request with an object. The request includes a locale (the*requested* locale), and the returned object is constructed using data for that locale. The system may lack data for the requested locale, in which case the locale fallback mechanism will be invoked until a populated locale is found (the*valid* locale). Furthermore, even when a populated locale is found (the*valid* locale), further fallback may be required to reach a locale containing the specific data required by the service (the*actual*locale).

ULocale performs**'normalization'** and**'canonicalization'**of locale ids. Normalization 'cleans up' ICU locale ids as follows:

- language, script, country, variant, and keywords are properly cased 
 (lower, title, upper, upper, and lower case respectively)
- hyphens used as separators are converted to underscores
- three-letter language and country ids are converted to two-letter equivalents where available
- surrounding spaces are removed from keywords and values
- if there are multiple keywords, they are put in sorted order

Canonicalization additionally performs the following:

<!-- -->

- POSIX ids are converted to ICU format IDs
- Legacy language tags (marked as "Type: grandfathered" in BCP 47) are converted to ICU standard form

All ULocale constructors automatically normalize the locale id. To handle POSIX ids,`canonicalize`can be called to convert the id to canonical form, or the`canonicalInstance`factory method can be called.

Note: The*actual* locale is returned correctly, but the*valid*locale is not, in most cases.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AvailableType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.AvailableType) Types for [ULocale.getAvailableLocalesByType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getAvailableLocalesByType(android.icu.util.ULocale.AvailableType)) |
| | [Builder](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder) `Builder`is used to build instances of`ULocale`from values configured by the setters. |
| | [Category](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) Enum for locale categories. |

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [PRIVATE_USE_EXTENSION](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#PRIVATE_USE_EXTENSION:kotlin.Char) The key for the private use locale extension ('x'). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [UNICODE_LOCALE_EXTENSION](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#UNICODE_LOCALE_EXTENSION:kotlin.Char) The key for Unicode locale extension ('u'). |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ULocale(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Constructs a ULocale from a RFC 3066 locale ID. |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ULocale(kotlin.String,%20kotlin.String))`(`a:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Convenience overload of ULocale(String, String, String) for compatibility with java. |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ULocale(kotlin.String,%20kotlin.String,%20kotlin.String))`(`a:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `b:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `c:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a ULocale from a localeID constructed from the three 'fields' a, b, and c. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [acceptLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#acceptLanguage(kotlin.Array,%20kotlin.Array,%20kotlin.BooleanArray))`(`acceptLanguageList:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!>!`, `availableLocales:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!>!`, `fallback:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` **\[icu\]**Based on a list of acceptable locales, determine an available locale for the user. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [acceptLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#acceptLanguage(kotlin.Array,%20kotlin.BooleanArray))`(`acceptLanguageList:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!>!`, `fallback:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` **\[icu\]**Based on an ordered array of acceptable locales, determine an available locale for the user. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [acceptLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#acceptLanguage(kotlin.String,%20kotlin.Array,%20kotlin.BooleanArray))`(`acceptLanguageList:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `availableLocales:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!>!`, `fallback:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` **\[icu\]**Based on a HTTP formatted list of acceptable locales, determine an available locale for the user. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [acceptLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#acceptLanguage(kotlin.String,%20kotlin.BooleanArray))`(`acceptLanguageList:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `fallback:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`)` **\[icu\]**Based on a HTTP formatted list of acceptable locales, determine an available locale for the user. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [addLikelySubtags](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#addLikelySubtags(android.icu.util.ULocale))`(`loc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Adds the likely subtags for a provided locale ID, per the algorithm described in the following CLDR technical report: http://www. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [canonicalize](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#canonicalize(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the canonical name according to CLDR for the specified locale ID. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#clone())`()` This is for compatibility with Locale-- in actuality, since ULocale is immutable, there is no reason to clone it, so this API returns 'this'. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#compareTo(android.icu.util.ULocale))`(`other:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Compares two ULocale for ordering. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [createCanonical](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#createCanonical(android.icu.util.ULocale))`(`locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Creates a ULocale from the locale by first canonicalizing the locale according to CLDR. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [createCanonical](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#createCanonical(kotlin.String))`(`nonCanonicalID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Creates a ULocale from the id by first canonicalizing the id according to CLDR. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns true if the other object is another ULocale with the same full name. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [forLanguageTag](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#forLanguageTag(kotlin.String))`(`languageTag:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a locale for the specified IETF BCP 47 language tag string. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [forLocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#forLocale(java.util.Locale))`(`loc:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`)` **\[icu\]** Returns a ULocale object for a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>! | [getAvailableLocales](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getAvailableLocales())`()` **\[icu\] Note:** Unlike the Locale API, this returns an array of`ULocale`, not`Locale`. |
| static [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>! | [getAvailableLocalesByType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getAvailableLocalesByType(android.icu.util.ULocale.AvailableType))`(`type:` ` [ULocale.AvailableType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.AvailableType)!`)` Returns a list of all installed locales according to the specified type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getBaseName())`()` **\[icu\]** Returns the (normalized) base name for this locale, like [getName()](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName()), but without keywords. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getBaseName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getBaseName(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** Returns the (normalized) base name for the specified locale, like [getName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName(kotlin.String)), but without keywords. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCharacterOrientation](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getCharacterOrientation())`()` **\[icu\]**Returns this locale's layout orientation for characters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getCountry())`()` Returns the country/region code for this locale, which will either be the empty string or an uppercase ISO 3166 2-letter code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getCountry(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the country/region code for this locale, which will either be the empty string or an uppercase ISO 3166 2-letter code. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [getDefault](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDefault())`()` Returns the current default ULocale. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [getDefault](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDefault(android.icu.util.ULocale.Category))`(`category:` ` [ULocale.Category](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category)!`)` Returns the current default ULocale for the specified category. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry())`()` Returns this locale's country localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Returns this locale's country localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a locale's country localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayCountry](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a locale's country localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeyword](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeyword(kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** Returns a keyword localized for display in the default`DISPLAY`locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeyword](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeyword(kotlin.String,%20android.icu.util.ULocale))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a keyword localized for display in the specified locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeyword](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeyword(kotlin.String,%20kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a keyword localized for display in the specified locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeywordValue(kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]** Returns a keyword value localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeywordValue(kotlin.String,%20android.icu.util.ULocale))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a keyword value localized for display in the specified locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeywordValue(kotlin.String,%20kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a keyword value localized for display in the specified locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayKeywordValue(kotlin.String,%20kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a keyword value localized for display in the specified locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage())`()` Returns this locale's language localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Returns this locale's language localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a locale's language localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a locale's language localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguageWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguageWithDialect())`()` **\[icu\]** Returns this locale's language localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguageWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguageWithDialect(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns this locale's language localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguageWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguageWithDialect(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a locale's language localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayLanguageWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguageWithDialect(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a locale's language localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayName())`()` Returns this locale name localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayName(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Returns this locale name localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayName(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns the locale ID localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayName(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the locale ID localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayNameWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayNameWithDialect())`()` **\[icu\]** Returns this locale name localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayNameWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayNameWithDialect(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns this locale name localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayNameWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayNameWithDialect(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns the locale ID localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayNameWithDialect](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayNameWithDialect(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the locale ID localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript())`()` Returns this locale's script localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Returns this locale's script localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a locale's script localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a locale's script localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant())`()` Returns this locale's variant localized for display in the default`DISPLAY`locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant(android.icu.util.ULocale))`(`displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` Returns this locale's variant localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant(kotlin.String,%20android.icu.util.ULocale))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]**Returns a locale's variant localized for display in the provided locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDisplayVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `displayLocaleID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a locale's variant localized for display in the provided locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getExtension](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getExtension(kotlin.Char))`(`key:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns the extension (or private use) value associated with the specified key, or null if there is no extension associated with the key. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)!\>! | [getExtensionKeys](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getExtensionKeys())`()` Returns the set of extension keys associated with this locale, or the empty set if it has no extensions. |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [getFallback](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getFallback())`()` **\[icu\]**Returns the fallback locale for this locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFallback](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getFallback(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the fallback locale for the specified locale, which might be the empty string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getISO3Country](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISO3Country())`()` Returns a three-letter abbreviation for this locale's country/region. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getISO3Country](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISO3Country(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a three-letter abbreviation for this locale's country/region. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getISO3Language](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISO3Language())`()` Returns a three-letter abbreviation for this locale's language. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getISO3Language](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISO3Language(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns a three-letter abbreviation for this locale's language. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getISOCountries](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISOCountries())`()` Returns a list of all 2-letter country codes defined in ISO 3166. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getISOLanguages](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getISOLanguages())`()` Returns a list of all unique language codes defined in ISO 639. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywordValue(kotlin.String))`(`keywordName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the value for a keyword in this locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywordValue(kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keywordName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the value for a keyword in the specified locale. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getKeywords](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywords())`()` **\[icu\]**Returns an iterator over keywords for this locale. |
| static [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getKeywords](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywords(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns an iterator over keywords for the specified locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getLanguage())`()` Returns the language code for this locale, which will either be the empty string or a lowercase ISO 639 code. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLanguage](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getLanguage(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the language code for the locale ID, which will either be the empty string or a lowercase ISO 639 code. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getLineOrientation](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getLineOrientation())`()` **\[icu\]**Returns this locale's layout orientation for lines. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName())`()` **\[icu\]**Returns the (normalized) full name for this locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the (normalized) full name for the specified locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getScript())`()` Returns the script code for this locale, which might be the empty string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getScript](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getScript(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the script code for the specified locale, which might be the empty string. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getUnicodeLocaleAttributes](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getUnicodeLocaleAttributes())`()` Returns the set of unicode locale attributes associated with this locale, or the empty set if it has no attributes. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getUnicodeLocaleKeys](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getUnicodeLocaleKeys())`()` Returns the set of Unicode locale keys defined by this locale, or the empty set if this locale has none. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getUnicodeLocaleType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getUnicodeLocaleType(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the Unicode locale type associated with the specified Unicode locale key for this locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getVariant())`()` Returns the variant code for this locale, which might be the empty string. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getVariant](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getVariant(kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Returns the variant code for the specified locale, which might be the empty string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#hashCode())`()` Returns the hashCode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRightToLeft](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#isRightToLeft())`()` **\[icu\]**Returns whether this locale's script is written right-to-left. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [minimizeSubtags](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#minimizeSubtags(android.icu.util.ULocale))`(`loc:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!`)` **\[icu\]** Minimizes the subtags for a provided locale ID, per the algorithm described in the following CLDR technical report:<http://www.unicode.org/reports/tr35/#Likely_Subtags>If the provided ULocale instance is already in the minimal form, or there is no data available for minimization, it will be returned. |
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [setKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#setKeywordValue(kotlin.String,%20kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Given a keyword and a value, return a new locale with an updated keyword and value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [setKeywordValue](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#setKeywordValue(kotlin.String,%20kotlin.String,%20kotlin.String))`(`localeID:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Given a locale id, a keyword, and a value, return a new locale id with an updated keyword and value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLanguageTag](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLanguageTag())`()` Returns a well-formed IETF BCP 47 language tag representing this locale. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLegacyKey](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLegacyKey(kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Converts the specified keyword (BCP 47 Unicode locale extension key, or legacy key) to the legacy key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toLegacyType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLegacyType(kotlin.String,%20kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Converts the specified keyword value (BCP 47 Unicode locale extension type, or legacy type or type alias) to the canonical legacy type. |
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | [toLocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLocale())`()` **\[icu\]** Converts this ULocale object to a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toString())`()` Returns a string representation of this object. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUnicodeLocaleKey](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toUnicodeLocaleKey(kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Converts the specified keyword (legacy key, or BCP 47 Unicode locale extension key) to the equivalent BCP 47 Unicode locale extension key. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toUnicodeLocaleType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toUnicodeLocaleType(kotlin.String,%20kotlin.String))`(`keyword:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **\[icu\]**Converts the specified keyword value (legacy type, or BCP 47 Unicode locale extension type) to the well-formed BCP 47 Unicode locale extension type for the specified keyword (category). |

| Properties ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [CANADA](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#CANADA:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [CANADA_FRENCH](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#CANADA_FRENCH:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [CHINA](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#CHINA:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [CHINESE](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#CHINESE:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [ENGLISH](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ENGLISH:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [FRANCE](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#FRANCE:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [FRENCH](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#FRENCH:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [GERMAN](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#GERMAN:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [GERMANY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#GERMANY:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [ITALIAN](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ITALIAN:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [ITALY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ITALY:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [JAPAN](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#JAPAN:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [JAPANESE](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#JAPANESE:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [KOREA](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#KOREA:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [KOREAN](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#KOREAN:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [PRC](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#PRC:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [ROOT](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ROOT:android.icu.util.ULocale) The root ULocale. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [SIMPLIFIED_CHINESE](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#SIMPLIFIED_CHINESE:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [TAIWAN](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#TAIWAN:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [TRADITIONAL_CHINESE](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#TRADITIONAL_CHINESE:android.icu.util.ULocale) Useful constant for language. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [UK](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#UK:android.icu.util.ULocale) Useful constant for country/region. |
| static [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | [US](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#US:android.icu.util.ULocale) Useful constant for country/region. |

## Constants

### PRIVATE_USE_EXTENSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIVATE_USE_EXTENSION: Char
```

The key for the private use locale extension ('x'). 

 Value: 'x'

**See Also**

- [#getExtension(char)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getExtension(kotlin.Char))
- [android.icu.util.ULocale.Builder#setExtension(char, String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder#setExtension(kotlin.Char,%20kotlin.String)) 

### UNICODE_LOCALE_EXTENSION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNICODE_LOCALE_EXTENSION: Char
```

The key for Unicode locale extension ('u'). 

 Value: 'u'

**See Also**

- [#getExtension(char)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getExtension(kotlin.Char))
- [android.icu.util.ULocale.Builder#setExtension(char, String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder#setExtension(kotlin.Char,%20kotlin.String))

## Public constructors

### ULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ULocale(localeID: String!)
```

**\[icu\]**Constructs a ULocale from a RFC 3066 locale ID. The locale ID consists of optional language, script, country, and variant fields in that order, separated by underscores, followed by an optional keyword list. The script, if present, is four characters long-- this distinguishes it from a country code, which is two characters long. Other fields are distinguished by position as indicated by the underscores. The start of the keyword list is indicated by '@', and consists of two or more keyword/value pairs separated by semicolons(';').

This constructor does not canonicalize the localeID. So, for example, "zh__pinyin" remains unchanged instead of converting to "zh@collation=pinyin". By default ICU only recognizes the latter as specifying pinyin collation. Use #createCanonical or [canonicalize](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#canonicalize(kotlin.String))if you need to canonicalize the localeID.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string representation of the locale, e.g: "en_US", "sy_Cyrl_YU", "zh__pinyin", "es_ES@currency=EUR;collation=traditional" |

### ULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ULocale(
    a: String!, 
    b: String!)
```

Convenience overload of ULocale(String, String, String) for compatibility with java.util.Locale. 
**See Also**

- [#ULocale(String, String, String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ULocale(kotlin.String,%20kotlin.String,%20kotlin.String)) 

### ULocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ULocale(
    a: String!, 
    b: String!, 
    c: String!)
```

Constructs a ULocale from a localeID constructed from the three 'fields' a, b, and c. These fields are concatenated using underscores to form a localeID of the form a_b_c, which is then handled like the localeID passed to`ULocale(String localeID)`.

Java locale strings consisting of language, country, and variant will be handled by this form, since the country code (being shorter than four letters long) will not be interpreted as a script code. If a script code is present, the final argument ('c') will be interpreted as the country code. It is recommended that this constructor only be used to ease porting, and that clients instead use the single-argument constructor when constructing a ULocale from a localeID.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------|
| `a` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:first component of the locale id |
| `b` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:second component of the locale id |
| `c` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:third component of the locale id |

**See Also**

- [#ULocale(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#ULocale(kotlin.String))

## Public methods

### acceptLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun acceptLanguage(
    acceptLanguageList: Array<ULocale!>!, 
    availableLocales: Array<ULocale!>!, 
    fallback: BooleanArray!
): ULocale!
```

**\[icu\]**Based on a list of acceptable locales, determine an available locale for the user. NullPointerException is thrown if acceptLanguageList or availableLocales is null. If fallback is non-null, it will contain true if a fallback locale (one not in the acceptLanguageList) was returned. The value on entry is ignored. ULocale will be one of the locales in availableLocales, or the ROOT ULocale if if a ROOT locale was used as a fallback (because nothing else in availableLocales matched). No ULocale array element should be null; behavior is undefined if this is the case.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acceptLanguageList` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>!:list of acceptable locales |
| `availableLocales` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>!:list of available locales. One of these will be returned. |
| `fallback` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:if non-null, a 1-element array containing a boolean to be set with the fallback status |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | one of the locales from the availableLocales list, or null if none match |

### acceptLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun acceptLanguage(
    acceptLanguageList: Array<ULocale!>!, 
    fallback: BooleanArray!
): ULocale!
```

**\[icu\]**Based on an ordered array of acceptable locales, determine an available locale for the user. NullPointerException is thrown if acceptLanguageList or availableLocales is null. If fallback is non-null, it will contain true if a fallback locale (one not in the acceptLanguageList) was returned. The value on entry is ignored. ULocale will be one of the locales in availableLocales, or the ROOT ULocale if if a ROOT locale was used as a fallback (because nothing else in availableLocales matched). No ULocale array element should be null; behavior is undefined if this is the case. This function will choose a locale from the ULocale.getAvailableLocales() list as available.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acceptLanguageList` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>!:ordered array of acceptable locales (preferred are listed first) |
| `fallback` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:if non-null, a 1-element array containing a boolean to be set with the fallback status |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | one of the locales from the ULocale.getAvailableLocales() list, or null if none match |

### acceptLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun acceptLanguage(
    acceptLanguageList: String!, 
    availableLocales: Array<ULocale!>!, 
    fallback: BooleanArray!
): ULocale!
```

**\[icu\]**Based on a HTTP formatted list of acceptable locales, determine an available locale for the user. NullPointerException is thrown if acceptLanguageList or availableLocales is null. If fallback is non-null, it will contain true if a fallback locale (one not in the acceptLanguageList) was returned. The value on entry is ignored. ULocale will be one of the locales in availableLocales, or the ROOT ULocale if if a ROOT locale was used as a fallback (because nothing else in availableLocales matched). No ULocale array element should be null; behavior is undefined if this is the case.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acceptLanguageList` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:list in HTTP "Accept-Language:" format of acceptable locales |
| `availableLocales` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!\>!:list of available locales. One of these will be returned. |
| `fallback` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:if non-null, a 1-element array containing a boolean to be set with the fallback status |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | one of the locales from the availableLocales list, or null if none match |

### acceptLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun acceptLanguage(
    acceptLanguageList: String!, 
    fallback: BooleanArray!
): ULocale!
```

**\[icu\]**Based on a HTTP formatted list of acceptable locales, determine an available locale for the user. NullPointerException is thrown if acceptLanguageList or availableLocales is null. If fallback is non-null, it will contain true if a fallback locale (one not in the acceptLanguageList) was returned. The value on entry is ignored. ULocale will be one of the locales in availableLocales, or the ROOT ULocale if if a ROOT locale was used as a fallback (because nothing else in availableLocales matched). No ULocale array element should be null; behavior is undefined if this is the case. This function will choose a locale from the ULocale.getAvailableLocales() list as available.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `acceptLanguageList` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:list in HTTP "Accept-Language:" format of acceptable locales |
| `fallback` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:if non-null, a 1-element array containing a boolean to be set with the fallback status |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | one of the locales from the ULocale.getAvailableLocales() list, or null if none match |

### addLikelySubtags

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun addLikelySubtags(loc: ULocale!): ULocale!
```

**\[icu\]**Adds the likely subtags for a provided locale ID, per the algorithm described in the following CLDR technical report: http://www.unicode.org/reports/tr35/#Likely_Subtags If the provided ULocale instance is already in the maximal form, or there is no data available available for maximization, it will be returned. For example, "sh" cannot be maximized, since there is no reasonable maximization. Otherwise, a new ULocale instance with the maximal form is returned. Examples: "en" maximizes to "en_Latn_US" "de" maximizes to "de_Latn_DE" "sr" maximizes to "sr_Cyrl_RS" "zh_Hani" maximizes to "zh_Hani_CN"

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `loc` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:The ULocale to maximize |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | The maximized ULocale instance. |

### canonicalize

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun canonicalize(localeID: String!): String!
```

**\[icu\]**Returns the canonical name according to CLDR for the specified locale ID. This is used to convert POSIX and other legacy IDs to standard ICU form.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale id |

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the canonicalized id |

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): Any!
```

This is for compatibility with Locale-- in actuality, since ULocale is immutable, there is no reason to clone it, so this API returns 'this'.

| Return ||
|-----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### compareTo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareTo(other: ULocale!): Int
```

Compares two ULocale for ordering.

**Note:**The order might change in future.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `o` | the object to be compared. |
| `other` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the ULocale to be compared. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a negative integer, zero, or a positive integer as this ULocale is less than, equal to, or greater than the specified ULocale. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`other`is null. |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### createCanonical

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createCanonical(locale: ULocale!): ULocale!
```

Creates a ULocale from the locale by first canonicalizing the locale according to CLDR.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the ULocale to canonicalize |

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | the ULocale created from the canonical version of the ULocale. |

### createCanonical

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createCanonical(nonCanonicalID: String!): ULocale!
```

**\[icu\]**Creates a ULocale from the id by first canonicalizing the id according to CLDR.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------|
| `nonCanonicalID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale id to canonicalize |

| Return ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | the locale created from the canonical version of the ID. |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Returns true if the other object is another ULocale with the same full name. Note that since names are not canonicalized, two ULocales that function identically might not compare equal.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this Locale is equal to the specified object. |

### forLanguageTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forLanguageTag(languageTag: String!): ULocale!
```

Returns a locale for the specified IETF BCP 47 language tag string.

If the specified language tag contains any ill-formed subtags, the first such subtag and all following subtags are ignored. Compare to [ULocale.Builder.setLanguageTag](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder#setLanguageTag(kotlin.String))which throws an exception in this case.

The following**conversions**are performed:

- The language code "und" is mapped to language "".
- The portion of a private use subtag prefixed by "lvariant", if any, is removed and appended to the variant field in the result locale (without case normalization). If it is then empty, the private use subtag is discarded: 

  ```kotlin
  ULocale loc;
        loc = ULocale.forLanguageTag("en-US-x-lvariant-icu4j);
        loc.getVariant(); // returns "ICU4J"
        loc.getExtension('x'); // returns null
   
        loc = Locale.forLanguageTag("de-icu4j-x-URP-lvariant-Abc-Def");
        loc.getVariant(); // returns "ICU4J_ABC_DEF"
        loc.getExtension('x'); // returns "urp"
    
  ```
- When the languageTag argument contains an extlang subtag, the first such subtag is used as the language, and the primary language subtag and other extlang subtags are ignored: 

  ```kotlin
  ULocale.forLanguageTag("ar-aao").getLanguage(); // returns "aao"
        ULocale.forLanguageTag("en-abc-def-us").toString(); // returns "abc_US"
    
  ```
- Case is normalized. Language is normalized to lower case, script to title case, country to upper case, variant to upper case, and extensions to lower case.

This implements the 'Language-Tag' production of BCP 47, and so supports legacy language tags (marked as "Type: grandfathered" in BCP 47) (regular and irregular) as well as private use language tags.

Stand-alone private use tags are represented as empty language and extension 'x-whatever', and legacy tags are converted to their canonical replacements where they exist.

Note that a few legacy tags have no modern replacement; these will be converted using the fallback described in the first paragraph, so some information might be lost.

**Note** : there is no guarantee that`toLanguageTag`and`forLanguageTag`will round-trip.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------|
| `languageTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the language tag |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | The locale that best represents the language tag. |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if`languageTag`is`null` |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLanguageTag()>
- [android.icu.util.ULocale.Builder#setLanguageTag(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Builder#setLanguageTag(kotlin.String)) 

### forLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun forLocale(loc: Locale!): ULocale!
```

**\[icu\]** Returns a ULocale object for a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#). The ULocale is canonicalized.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `loc` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) |

### getAvailableLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableLocales(): Array<ULocale!>!
```

**\[icu\] Note:** Unlike the Locale API, this returns an array of`ULocale`, not`Locale`.

Returns a list of all installed locales. This is equivalent to calling [getAvailableLocalesByType](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getAvailableLocalesByType(android.icu.util.ULocale.AvailableType))with AvailableType.DEFAULT. 

### getAvailableLocalesByType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getAvailableLocalesByType(type: ULocale.AvailableType!): MutableCollection<ULocale!>!
```

Returns a list of all installed locales according to the specified type. 

### getBaseName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBaseName(): String!
```

**\[icu\]** Returns the (normalized) base name for this locale, like [getName()](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName()), but without keywords.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the base name as a String. |

### getBaseName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getBaseName(localeID: String!): String!
```

**\[icu\]** Returns the (normalized) base name for the specified locale, like [getName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getName(kotlin.String)), but without keywords.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale ID as a string |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the base name as a String. |

### getCharacterOrientation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharacterOrientation(): String!
```

**\[icu\]**Returns this locale's layout orientation for characters. The possible values are "left-to-right", "right-to-left", "top-to-bottom" or "bottom-to-top".

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The locale's layout orientation for characters. |

### getCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCountry(): String!
```

Returns the country/region code for this locale, which will either be the empty string or an uppercase ISO 3166 2-letter code. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry()>
- [#getDisplayCountry(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry(android.icu.util.ULocale)) 

### getCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCountry(localeID: String!): String!
```

**\[icu\]**Returns the country/region code for this locale, which will either be the empty string or an uppercase ISO 3166 2-letter code.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The locale identification string. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry()>
- [#getDisplayCountry(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayCountry(android.icu.util.ULocale)) 

### getDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(): ULocale!
```

Returns the current default ULocale.

The default ULocale is synchronized to the default Java Locale. This method checks the current default Java Locale and returns an equivalent ULocale.

| Return ||
|--------------------------------------------------------------------------------------|----------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | the default ULocale. |

### getDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefault(category: ULocale.Category!): ULocale!
```

Returns the current default ULocale for the specified category.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `category` | [ULocale.Category](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category)!:the category |

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | the default ULocale for the specified category. |

### getDisplayCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayCountry(): String!
```

Returns this locale's country localized for display in the default`DISPLAY`locale.**Warning:** this is for the region part of a valid locale ID; it cannot just be the region code (like "FR"). To get the display name for a region alone, or for other options, use [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.html#) instead.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized country name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayCountry(displayLocale: ULocale!): String!
```

Returns this locale's country localized for display in the provided locale.**Warning:** this is for the region part of a valid locale ID; it cannot just be the region code (like "FR"). To get the display name for a region alone, or for other options, use [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.html#) instead.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized country name. |

### getDisplayCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayCountry(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]** Returns a locale's country localized for display in the provided locale.**Warning:** this is for the region part of a valid locale ID; it cannot just be the region code (like "FR"). To get the display name for a region alone, or for other options, use [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.html#) instead. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose country will be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized country name. |

### getDisplayCountry

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayCountry(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]** Returns a locale's country localized for display in the provided locale.**Warning:** this is for the region part of a valid locale ID; it cannot just be the region code (like "FR"). To get the display name for a region alone, or for other options, use [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames.html#) instead. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose country will be displayed |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized country name. |

### getDisplayKeyword

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayKeyword(keyword: String!): String!
```

**\[icu\]** Returns a keyword localized for display in the default`DISPLAY`locale.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized keyword name. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywords()>
- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayKeyword

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayKeyword(
    keyword: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a keyword localized for display in the specified locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the keyword. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized keyword name. |

**See Also**

- [#getKeywords(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywords(kotlin.String)) 

### getDisplayKeyword

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayKeyword(
    keyword: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a keyword localized for display in the specified locale.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to be displayed. |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the keyword. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized keyword name. |

**See Also**

- [#getKeywords(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getKeywords(kotlin.String)) 

### getDisplayKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayKeywordValue(keyword: String!): String!
```

**\[icu\]** Returns a keyword value localized for display in the default`DISPLAY`locale.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword whose value is to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized value name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayKeywordValue(
    keyword: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a keyword value localized for display in the specified locale.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword whose value is to be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the value. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized value name. |

### getDisplayKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayKeywordValue(
    localeID: String!, 
    keyword: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a keyword value localized for display in the specified locale. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose keyword value is to be displayed. |
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword whose value is to be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the id of the locale in which to display the value. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized value name. |

### getDisplayKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayKeywordValue(
    localeID: String!, 
    keyword: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a keyword value localized for display in the specified locale. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose keyword value is to be displayed. |
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword whose value is to be displayed. |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the value. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized value name. |

### getDisplayLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLanguage(): String!
```

Returns this locale's language localized for display in the default`DISPLAY`locale.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLanguage(displayLocale: ULocale!): String!
```

Returns this locale's language localized for display in the provided locale.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayLanguage(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a locale's language localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose language will be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayLanguage(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a locale's language localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose language will be displayed |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayLanguageWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLanguageWithDialect(): String!
```

**\[icu\]** Returns this locale's language localized for display in the default`DISPLAY`locale. If a dialect name is present in the data, then it is returned.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayLanguageWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayLanguageWithDialect(displayLocale: ULocale!): String!
```

**\[icu\]**Returns this locale's language localized for display in the provided locale. If a dialect name is present in the data, then it is returned.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayLanguageWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayLanguageWithDialect(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a locale's language localized for display in the provided locale. If a dialect name is present in the data, then it is returned. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose language will be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayLanguageWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayLanguageWithDialect(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a locale's language localized for display in the provided locale. If a dialect name is present in the data, then it is returned. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose language will be displayed |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized language name. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(): String!
```

Returns this locale name localized for display in the default`DISPLAY`locale.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayName(displayLocale: ULocale!): String!
```

Returns this locale name localized for display in the provided locale.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayName(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns the locale ID localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale whose name is to be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayName(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns the locale ID localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale whose name is to be displayed. |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayNameWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayNameWithDialect(): String!
```

**\[icu\]** Returns this locale name localized for display in the default`DISPLAY`locale. If a dialect name is present in the locale data, then it is returned.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayNameWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayNameWithDialect(displayLocale: ULocale!): String!
```

**\[icu\]**Returns this locale name localized for display in the provided locale. If a dialect name is present in the locale data, then it is returned.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayNameWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayNameWithDialect(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns the locale ID localized for display in the provided locale. If a dialect name is present in the locale data, then it is returned. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale whose name is to be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayNameWithDialect

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayNameWithDialect(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns the locale ID localized for display in the provided locale. If a dialect name is present in the locale data, then it is returned. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale whose name is to be displayed. |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the locale name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized locale name. |

### getDisplayScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayScript(): String!
```

Returns this locale's script localized for display in the default`DISPLAY`locale.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized script name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayScript(displayLocale: ULocale!): String!
```

Returns this locale's script localized for display in the provided locale.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized script name. |

### getDisplayScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayScript(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a locale's script localized for display in the provided locale.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose script will be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized script name. |

### getDisplayScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayScript(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a locale's script localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose script will be displayed |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized script name. |

### getDisplayVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayVariant(): String!
```

Returns this locale's variant localized for display in the default`DISPLAY`locale.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized variant name. |

**See Also**

- [android.icu.util.ULocale.Category#DISPLAY](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category) 

### getDisplayVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayVariant(displayLocale: ULocale!): String!
```

Returns this locale's variant localized for display in the provided locale.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized variant name. |

### getDisplayVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayVariant(
    localeID: String!, 
    displayLocale: ULocale!
): String!
```

**\[icu\]**Returns a locale's variant localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose variant will be displayed. |
| `displayLocale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized variant name. |

### getDisplayVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDisplayVariant(
    localeID: String!, 
    displayLocaleID: String!
): String!
```

**\[icu\]**Returns a locale's variant localized for display in the provided locale. This is a cover for the ICU4C API.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale whose variant will be displayed |
| `displayLocaleID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the id of the locale in which to display the name. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the localized variant name. |

### getExtension

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtension(key: Char): String!
```

Returns the extension (or private use) value associated with the specified key, or null if there is no extension associated with the key. To be well-formed, the key must be one of`[0-9A-Za-z]`. Keys are case-insensitive, so for example 'z' and 'Z' represent the same extension.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `key` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the extension key |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The extension, or null if this locale defines no extension for the specified key. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if key is not well-formed |

**See Also**

- [#PRIVATE_USE_EXTENSION](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#PRIVATE_USE_EXTENSION:kotlin.Char)
- [#UNICODE_LOCALE_EXTENSION](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#UNICODE_LOCALE_EXTENSION:kotlin.Char) 

### getExtensionKeys

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtensionKeys(): MutableSet<Char!>!
```

Returns the set of extension keys associated with this locale, or the empty set if it has no extensions. The returned set is unmodifiable. The keys will all be lower-case.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)!>! | the set of extension keys, or the empty set if this locale has no extensions |

### getFallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFallback(): ULocale!
```

**\[icu\]**Returns the fallback locale for this locale. If this locale is root, returns null. 

### getFallback

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getFallback(localeID: String!): String!
```

**\[icu\]**Returns the fallback locale for the specified locale, which might be the empty string. 

### getISO3Country

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getISO3Country(): String!
```

Returns a three-letter abbreviation for this locale's country/region. If the locale doesn't specify a country, returns the empty string. Otherwise, returns an uppercase ISO 3166 3-letter country code.

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | Throws MissingResourceException if the three-letter country abbreviation is not available for this locale. |

### getISO3Country

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getISO3Country(localeID: String!): String!
```

**\[icu\]**Returns a three-letter abbreviation for this locale's country/region. If the locale doesn't specify a country, returns the empty string. Otherwise, returns an uppercase ISO 3166 3-letter country code.

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | Throws MissingResourceException if the three-letter country abbreviation is not available for this locale. |

### getISO3Language

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getISO3Language(): String!
```

Returns a three-letter abbreviation for this locale's language. If the locale doesn't specify a language, returns the empty string. Otherwise, returns a lowercase ISO 639-2/T language code. The ISO 639-2 language codes can be found on-line at [`ftp://dkuug.dk/i18n/iso-639-2.txt`](ftp://dkuug.dk/i18n/iso-639-2.txt)

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | Throws MissingResourceException if the three-letter language abbreviation is not available for this locale. |

### getISO3Language

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getISO3Language(localeID: String!): String!
```

**\[icu\]** Returns a three-letter abbreviation for this locale's language. If the locale doesn't specify a language, returns the empty string. Otherwise, returns a lowercase ISO 639-2/T language code. The ISO 639-2 language codes can be found on-line at [`ftp://dkuug.dk/i18n/iso-639-2.txt`](ftp://dkuug.dk/i18n/iso-639-2.txt)

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.util.MissingResourceException` | Throws MissingResourceException if the three-letter language abbreviation is not available for this locale. |

### getISOCountries

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getISOCountries(): Array<String!>!
```

Returns a list of all 2-letter country codes defined in ISO 3166. Can be used to create Locales. 

### getISOLanguages

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getISOLanguages(): Array<String!>!
```

Returns a list of all unique language codes defined in ISO 639. They can be 2 or 3 letter codes, as defined by [BCP 47, section 2.2.1](https://www.ietf.org/rfc/bcp/bcp47.html#section-2.2.1). Can be used to create Locales. \[NOTE: ISO 639 is not a stable standard-- some languages' codes have changed. The list this function returns includes both the new and the old codes for the languages whose codes have changed.\] 

### getKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeywordValue(keywordName: String!): String!
```

**\[icu\]**Returns the value for a keyword in this locale. If the keyword is not defined, returns null.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `keywordName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:name of the keyword whose value is desired. Case insensitive. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the value of the keyword, or null. |

### getKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getKeywordValue(
    localeID: String!, 
    keywordName: String!
): String!
```

**\[icu\]**Returns the value for a keyword in the specified locale. If the keyword is not defined, returns null. The locale name does not need to be normalized.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `keywordName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:name of the keyword whose value is desired. Case insensitive. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String the value of the keyword as a string |

### getKeywords

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeywords(): MutableIterator<String!>!
```

**\[icu\]**Returns an iterator over keywords for this locale. If there are no keywords, returns null.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | iterator over keywords, or null if there are no keywords. |

### getKeywords

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getKeywords(localeID: String!): MutableIterator<String!>!
```

**\[icu\]**Returns an iterator over keywords for the specified locale. If there are no keywords, returns null.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an iterator over the keywords in the specified locale, or null if there are no keywords. |

### getLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLanguage(): String!
```

Returns the language code for this locale, which will either be the empty string or a lowercase ISO 639 code. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage()>
- [#getDisplayLanguage(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage(android.icu.util.ULocale)) 

### getLanguage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLanguage(localeID: String!): String!
```

Returns the language code for the locale ID, which will either be the empty string or a lowercase ISO 639 code. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage()>
- [#getDisplayLanguage(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayLanguage(android.icu.util.ULocale)) 

### getLineOrientation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineOrientation(): String!
```

**\[icu\]**Returns this locale's layout orientation for lines. The possible values are "left-to-right", "right-to-left", "top-to-bottom" or "bottom-to-top".

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The locale's layout orientation for lines. |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

**\[icu\]**Returns the (normalized) full name for this locale.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String the full name of the localeID |

### getName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getName(localeID: String!): String!
```

**\[icu\]**Returns the (normalized) full name for the specified locale.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the localeID as a string |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String the full name of the localeID |

### getScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScript(): String!
```

Returns the script code for this locale, which might be the empty string. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript()>
- [#getDisplayScript(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript(android.icu.util.ULocale)) 

### getScript

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getScript(localeID: String!): String!
```

**\[icu\]**Returns the script code for the specified locale, which might be the empty string. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript()>
- [#getDisplayScript(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayScript(android.icu.util.ULocale)) 

### getUnicodeLocaleAttributes

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnicodeLocaleAttributes(): MutableSet<String!>!
```

Returns the set of unicode locale attributes associated with this locale, or the empty set if it has no attributes. The returned set is unmodifiable.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The set of attributes. |

### getUnicodeLocaleKeys

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnicodeLocaleKeys(): MutableSet<String!>!
```

Returns the set of Unicode locale keys defined by this locale, or the empty set if this locale has none. The returned set is immutable. Keys are all lower case.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The set of Unicode locale keys, or the empty set if this locale has no Unicode locale keywords. |

### getUnicodeLocaleType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getUnicodeLocaleType(key: String!): String!
```

Returns the Unicode locale type associated with the specified Unicode locale key for this locale. Returns the empty string for keys that are defined with no type. Returns null if the key is not defined. Keys are case-insensitive. The key must be two alphanumeric characters (\[0-9a-zA-Z\]), or an IllegalArgumentException is thrown.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Unicode locale key |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The Unicode locale type associated with the key, or null if the locale does not define the key. |

| Exceptions ||
|--------------------------------------|-------------------------------|
| `java.lang.IllegalArgumentException` | if the key is not well-formed |
| `java.lang.NullPointerException` | if`key`is null |

### getVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVariant(): String!
```

Returns the variant code for this locale, which might be the empty string. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant()>
- [#getDisplayVariant(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant(android.icu.util.ULocale)) 

### getVariant

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getVariant(localeID: String!): String!
```

**\[icu\]**Returns the variant code for the specified locale, which might be the empty string. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant()>
- [#getDisplayVariant(ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getDisplayVariant(android.icu.util.ULocale)) 

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hashCode.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isRightToLeft

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRightToLeft(): Boolean
```

**\[icu\]** Returns whether this locale's script is written right-to-left. If there is no script subtag, then the likely script is used, see [addLikelySubtags(android.icu.util.ULocale)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#addLikelySubtags(android.icu.util.ULocale)). If no likely script is known, then false is returned.

A script is right-to-left according to the CLDR script metadata which corresponds to whether the script's letters have Bidi_Class=R or AL.

Returns true for "ar" and "en-Hebr", false for "zh" and "fa-Cyrl".

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the locale's script is written right-to-left |

### minimizeSubtags

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun minimizeSubtags(loc: ULocale!): ULocale!
```

**\[icu\]** Minimizes the subtags for a provided locale ID, per the algorithm described in the following CLDR technical report:<http://www.unicode.org/reports/tr35/#Likely_Subtags>If the provided ULocale instance is already in the minimal form, or there is no data available for minimization, it will be returned. Since the minimization algorithm relies on proper maximization, see the comments for addLikelySubtags for reasons why there might not be any data. Examples: 

```kotlin
"en_Latn_US" minimizes to "en"
 
  "de_Latn_US" minimizes to "de"
 
  "sr_Cyrl_RS" minimizes to "sr"
 
  "zh_Hant_TW" minimizes to "zh_TW" (The region is preferred to the
  script, and minimizing to "zh" would imply "zh_Hans_CN".) 
```

<br />

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `loc` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)!:The ULocale to minimize |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | The minimized ULocale instance. |

### setKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setKeywordValue(
    keyword: String!, 
    value: String!
): ULocale!
```

**\[icu\]**Given a keyword and a value, return a new locale with an updated keyword and value. If the keyword is null, this removes all keywords from the locale id. Otherwise, if the value is null, this removes the value for this keyword from the locale id. Otherwise, this adds/replaces the value for this keyword in the locale id. The keyword and value must not be empty.

Related: [getBaseName()](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getBaseName())returns the locale ID string with all keywords removed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to add/remove, or null to remove all keywords. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value to add/set, or null to remove this particular keyword. |

| Return ||
|--------------------------------------------------------------------------------------|--------------------|
| [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#)! | the updated locale |

### setKeywordValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setKeywordValue(
    localeID: String!, 
    keyword: String!, 
    value: String!
): String!
```

Given a locale id, a keyword, and a value, return a new locale id with an updated keyword and value. If the keyword is null, this removes all keywords from the locale id. Otherwise, if the value is null, this removes the value for this keyword from the locale id. Otherwise, this adds/replaces the value for this keyword in the locale id. The keyword and value must not be empty.

Related: [getBaseName(java.lang.String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#getBaseName(kotlin.String))returns the locale ID string with all keywords removed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `localeID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale id to modify |
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the keyword to add/remove, or null to remove all keywords. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the value to add/set, or null to remove this particular keyword. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the updated locale id |

### toLanguageTag

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLanguageTag(): String!
```

Returns a well-formed IETF BCP 47 language tag representing this locale.

If this`ULocale`has a language, script, country, or variant that does not satisfy the IETF BCP 47 language tag syntax requirements, this method handles these fields as described below:

**Language:**If language is empty, or not well-formed (for example "a" or "e2"), it will be emitted as "und" (Undetermined).

**Script:**If script is not well-formed (for example "12" or "Latin"), it will be omitted.

**Country:**If country is not well-formed (for example "12" or "USA"), it will be omitted.

**Variant:** If variant**is**well-formed, each sub-segment (delimited by '-' or '_') is emitted as a subtag. Otherwise:

- if all sub-segments match`[0-9a-zA-Z]{1,8}`(for example "WIN" or "Oracle_JDK_Standard_Edition"), the first ill-formed sub-segment and all following will be appended to the private use subtag. The first appended subtag will be "lvariant", followed by the sub-segments in order, separated by hyphen. For example, "x-lvariant-WIN", "Oracle-x-lvariant-JDK-Standard-Edition".
- if any sub-segment does not match`[0-9a-zA-Z]{1,8}`, the variant will be truncated and the problematic sub-segment and all following sub-segments will be omitted. If the remainder is non-empty, it will be emitted as a private use subtag as above (even if the remainder turns out to be well-formed). For example, "Solaris_isjustthecoolestthing" is emitted as "x-lvariant-Solaris", not as "solaris".

**Note:**Although the language tag created by this method is well-formed (satisfies the syntax requirements defined by the IETF BCP 47 specification), it is not necessarily a valid BCP 47 language tag. For example, 

```kotlin
new Locale("xx", "YY").toLanguageTag();
```
will return "xx-YY", but the language subtag "xx" and the region subtag "YY" are invalid because they are not registered in the IANA Language Subtag Registry.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a BCP47 language tag representing the locale |

**See Also**

- [#forLanguageTag(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#forLanguageTag(kotlin.String)) 

### toLegacyKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLegacyKey(keyword: String!): String!
```

**\[icu\]**Converts the specified keyword (BCP 47 Unicode locale extension key, or legacy key) to the legacy key. For example, legacy key "collation" is returned for the input BCP 47 Unicode locale extension key "co".

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the input locale keyword (either BCP 47 Unicode locale extension key or legacy key). |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the well-formed legacy key, or null if the specified keyword cannot be mapped to a well-formed legacy key. |

**See Also**

- [#toUnicodeLocaleKey(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toUnicodeLocaleKey(kotlin.String)) 

### toLegacyType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toLegacyType(
    keyword: String!, 
    value: String!
): String!
```

**\[icu\]**Converts the specified keyword value (BCP 47 Unicode locale extension type, or legacy type or type alias) to the canonical legacy type. For example, the legacy type "phonebook" is returned for the input BCP 47 Unicode locale extension type "phonebk" with the keyword "collation" (or "co").

When the specified keyword is not recognized, but the specified value satisfies the syntax of legacy key, or when the specified keyword allows 'variable' type and the specified value satisfies the syntax, the lower-case version of the input value will be returned. For example,`toLegacyType("Foo", "Bar")`returns "bar",`toLegacyType("vt", "00A4")`returns "00a4".

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale keyword (either legacy keyword such as "collation" or BCP 47 Unicode locale extension key such as "co"). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale keyword value (either BCP 47 Unicode locale extension type such as "phonebk" or legacy keyword value such as "phonebook"). |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the well-formed legacy type, or null if the specified keyword value cannot be mapped to a well-formed legacy type. |

**See Also**

- [#toUnicodeLocaleType(String, String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toUnicodeLocaleType(kotlin.String,%20kotlin.String)) 

### toLocale

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toLocale(): Locale!
```

**\[icu\]** Converts this ULocale object to a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)! | a [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) that either exactly represents this object or is the closest approximation. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### toUnicodeLocaleKey

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnicodeLocaleKey(keyword: String!): String!
```

**\[icu\]**Converts the specified keyword (legacy key, or BCP 47 Unicode locale extension key) to the equivalent BCP 47 Unicode locale extension key. For example, BCP 47 Unicode locale extension key "co" is returned for the input keyword "collation".

When the specified keyword is unknown, but satisfies the BCP syntax, then the lower-case version of the input keyword will be returned. For example,`toUnicodeLocaleKey("ZZ")`returns "zz".

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the input locale keyword (either legacy key such as "collation" or BCP 47 Unicode locale extension key such as "co"). |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the well-formed BCP 47 Unicode locale extension key, or null if the specified locale keyword cannot be mapped to a well-formed BCP 47 Unicode locale extension key. |

**See Also**

- [#toLegacyKey(String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLegacyKey(kotlin.String)) 

### toUnicodeLocaleType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toUnicodeLocaleType(
    keyword: String!, 
    value: String!
): String!
```

**\[icu\]**Converts the specified keyword value (legacy type, or BCP 47 Unicode locale extension type) to the well-formed BCP 47 Unicode locale extension type for the specified keyword (category). For example, BCP 47 Unicode locale extension type "phonebk" is returned for the input keyword value "phonebook", with the keyword "collation" (or "co").

When the specified keyword is not recognized, but the specified value satisfies the syntax of the BCP 47 Unicode locale extension type, or when the specified keyword allows 'variable' type and the specified value satisfies the syntax, the lower-case version of the input value will be returned. For example,`toUnicodeLocaleType("Foo", "Bar")`returns "bar",`toUnicodeLocaleType("variableTop", "00A4")`returns "00a4".

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyword` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale keyword (either legacy key such as "collation" or BCP 47 Unicode locale extension key such as "co"). |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the locale keyword value (either legacy type such as "phonebook" or BCP 47 Unicode locale extension type such as "phonebk"). |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the well-formed BCP47 Unicode locale extension type, or null if the locale keyword value cannot be mapped to a well-formed BCP 47 Unicode locale extension type. |

**See Also**

- [#toLegacyType(String, String)](https://developer.android.com/reference/kotlin/android/icu/util/ULocale#toLegacyType(kotlin.String,%20kotlin.String))

## Properties

### CANADA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANADA: ULocale!
```

Useful constant for country/region. 

### CANADA_FRENCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANADA_FRENCH: ULocale!
```

Useful constant for country/region. 

### CHINA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHINA: ULocale!
```

Useful constant for country/region. 

### CHINESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHINESE: ULocale!
```

Useful constant for language. 

### ENGLISH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENGLISH: ULocale!
```

Useful constant for language. 

### FRANCE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRANCE: ULocale!
```

Useful constant for country/region. 

### FRENCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FRENCH: ULocale!
```

Useful constant for language. 

### GERMAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GERMAN: ULocale!
```

Useful constant for language. 

### GERMANY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GERMANY: ULocale!
```

Useful constant for country/region. 

### ITALIAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ITALIAN: ULocale!
```

Useful constant for language. 

### ITALY

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ITALY: ULocale!
```

Useful constant for country/region. 

### JAPAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JAPAN: ULocale!
```

Useful constant for country/region. 

### JAPANESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JAPANESE: ULocale!
```

Useful constant for language. 

### KOREA

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KOREA: ULocale!
```

Useful constant for country/region. 

### KOREAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val KOREAN: ULocale!
```

Useful constant for language. 

### PRC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRC: ULocale!
```

Useful constant for country/region. 

### ROOT

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ROOT: ULocale!
```

The root ULocale. 

### SIMPLIFIED_CHINESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIMPLIFIED_CHINESE: ULocale!
```

Useful constant for language. 

### TAIWAN

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TAIWAN: ULocale!
```

Useful constant for country/region. 

### TRADITIONAL_CHINESE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRADITIONAL_CHINESE: ULocale!
```

Useful constant for language. 

### UK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UK: ULocale!
```

Useful constant for country/region. 

### US

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val US: ULocale!
```

Useful constant for country/region.
