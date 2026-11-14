Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Locale

```
class Locale : Cloneable, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) |

A object represents a specific geographical, political, or cultural region. An operation that requires a to perform its task is called *locale-sensitive* and uses the to tailor information for the user. For example, displaying a number is a locale-sensitive operation--- the number should be formatted according to the customs and conventions of the user's native country, region, or culture.

The `Locale` class implements IETF BCP 47 which is composed of [RFC 4647 "Matching of Language Tags"](https://tools.ietf.org/html/rfc4647) and [RFC 5646 "Tags for Identifying Languages"](https://tools.ietf.org/html/rfc5646) with support for the LDML (UTS#35, "Unicode Locale Data Markup Language") BCP 47-compatible extensions for locale data exchange.

A `Locale` object logically consists of the fields described below.

**language**
: ISO 639 alpha-2 or alpha-3 language code, or registered language subtags up to 8 alpha letters (for future enhancements). When a language has both an alpha-2 code and an alpha-3 code, the alpha-2 code must be used. You can find a full list of valid language codes in the IANA Language Subtag Registry (search for "Type: language"). The language field is case insensitive, but `Locale` always canonicalizes to lower case.
: Well-formed language values have the form `[a-zA-Z]{2,8}`. Note that this is not the full BCP47 language production, since it excludes extlang. They are not needed since modern three-letter language codes replace them.
: Example: "en" (English), "ja" (Japanese), "kok" (Konkani)

**script**
: ISO 15924 alpha-4 script code. You can find a full list of valid script codes in the IANA Language Subtag Registry (search for "Type: script"). The script field is case insensitive, but `Locale` always canonicalizes to title case (the first letter is upper case and the rest of the letters are lower case).
: Well-formed script values have the form `[a-zA-Z]{4}`
: Example: "Latn" (Latin), "Cyrl" (Cyrillic)

**country (region)**
: ISO 3166 alpha-2 country code or UN M.49 numeric-3 area code. You can find a full list of valid country and region codes in the IANA Language Subtag Registry (search for "Type: region"). The country (region) field is case insensitive, but `Locale` always canonicalizes to upper case.
: Well-formed country/region values have the form `[a-zA-Z]{2} | [0-9]{3}`
: Example: "US" (United States), "FR" (France), "029" (Caribbean)

**variant**
: Any arbitrary value used to indicate a variation of a `Locale`. Where there are two or more variant values each indicating its own semantics, these values should be ordered by importance, with most important first, separated by underscore('_'). The variant field is case sensitive.

: Note: IETF BCP 47 places syntactic restrictions on variant subtags. Also BCP 47 subtags are strictly used to indicate additional variations that define a language or its dialects that are not covered by any combinations of language, script and region subtags. You can find a full list of valid variant codes in the IANA Language Subtag Registry (search for "Type: variant"). However, the variant field in `Locale` has historically been used for any kind of variation, not just language variations. For example, some supported variants available in Java SE Runtime Environments indicate alternative cultural behaviors such as calendar type or number script. In BCP 47 this kind of information, which does not identify the language, is supported by extension subtags or private use subtags.

: Well-formed variant values have the form `SUBTAG (('_'|'-') SUBTAG)*` where `SUBTAG = [0-9][0-9a-zA-Z]{3} | [0-9a-zA-Z]{5,8}`. (Note: BCP 47 only uses hyphen ('-') as a delimiter, this is more lenient).
: Example: "polyton" (Polytonic Greek), "POSIX"

**extensions**
: A map from single character keys to string values, indicating extensions apart from language identification. The extensions in `Locale` implement the semantics and syntax of BCP 47 extension subtags and private use subtags. The extensions are case insensitive, but `Locale` canonicalizes all extension keys and values to lower case. Note that extensions cannot have empty values.
: Well-formed keys are single characters from the set `[0-9a-zA-Z]`. Well-formed values have the form `SUBTAG ('-' SUBTAG)*` where for the key 'x' `SUBTAG = [0-9a-zA-Z]{1,8}` and for other keys `SUBTAG = [0-9a-zA-Z]{2,8}` (that is, 'x' allows single-character subtags).
: Example: key="u"/value="ca-japanese" (Japanese Calendar), key="x"/value="java-1-7"
**Note:** Although BCP 47 requires field values to be registered in the IANA Language Subtag Registry, the `Locale` class does not provide any validation features. The `Builder` only checks if an individual field satisfies the syntactic requirement (is well-formed), but does not validate the value itself. See `https://developer.android.com/reference/kotlin/java/util/Locale.Builder` for details.

## Unicode locale/language extension

UTS#35, "Unicode Locale Data Markup Language" defines optional attributes and keywords to override or refine the default behavior associated with a locale. A keyword is represented by a pair of key and type. For example, "nu-thai" indicates that Thai local digits (value:"thai") should be used for formatting numbers (key:"nu").

The keywords are mapped to a BCP 47 extension value using the extension key 'u' (`https://developer.android.com/reference/kotlin/java/util/Locale#UNICODE_LOCALE_EXTENSION:kotlin.Char`). The above example, "nu-thai", becomes the extension "u-nu-thai".

Thus, when a `Locale` object contains Unicode locale attributes and keywords, `getExtension(UNICODE_LOCALE_EXTENSION)` will return a String representing this information, for example, "nu-thai". The `Locale` class also provides `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleAttributes()`, `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleKeys()`, and `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleType(kotlin.String)` which allow you to access Unicode locale attributes and key/type pairs directly. When represented as a string, the Unicode Locale Extension lists attributes alphabetically, followed by key/type sequences with keys listed alphabetically (the order of subtags comprising a key's type is fixed when the type is defined)

A well-formed locale key has the form `[0-9a-zA-Z]{2}`. A well-formed locale type has the form `"" | [0-9a-zA-Z]{3,8} ('-' [0-9a-zA-Z]{3,8})*` (it can be empty, or a series of subtags 3-8 alphanums in length). A well-formed locale attribute has the form `[0-9a-zA-Z]{3,8}` (it is a single subtag with the same form as a locale type subtag).

The Unicode locale extension specifies optional behavior in locale-sensitive services. Although the LDML specification defines various keys and values, actual locale-sensitive service implementations in a Java Runtime Environment might not support any particular Unicode locale attributes or key/type pairs.

### Obtaining a Locale

There are several ways to obtain a `Locale` object.

#### Builder

Using `https://developer.android.com/reference/kotlin/java/util/Locale.Builder` you can construct a `Locale` object that conforms to BCP 47 syntax.

#### Factory Methods

The method `https://developer.android.com/reference/kotlin/java/util/Locale#forLanguageTag(kotlin.String)` obtains a `Locale` object for a well-formed BCP 47 language tag. The method `https://developer.android.com/reference/kotlin/java/util/Locale#of(kotlin.String,%20kotlin.String,%20kotlin.String)` and its overloads obtain a `Locale` object from given `language`, `country`, and/or `variant` defined above.

#### Locale Constants

The `Locale` class provides a number of convenient constants that you can use to obtain `Locale` objects for commonly used locales. For example, `Locale.US` is the `Locale` object for the United States.

### Locale Matching

If an application or a system is internationalized and provides localized resources for multiple locales, it sometimes needs to find one or more locales (or language tags) which meet each user's specific preferences. Note that a term "language tag" is used interchangeably with "locale" in this locale matching documentation.

In order to do matching a user's preferred locales to a set of language tags, [RFC 4647 Matching of Language Tags](https://tools.ietf.org/html/rfc4647) defines two mechanisms: filtering and lookup. *Filtering* is used to get all matching locales, whereas *lookup* is to choose the best matching locale. Matching is done case-insensitively. These matching mechanisms are described in the following sections.

A user's preference is called a *Language Priority List* and is expressed as a list of language ranges. There are syntactically two types of language ranges: basic and extended. See `https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange` for details.

#### Filtering

The filtering operation returns all matching language tags. It is defined in RFC 4647 as follows: "In filtering, each language range represents the least specific language tag (that is, the language tag with fewest number of subtags) that is an acceptable match. All of the language tags in the matching set of tags will have an equal or greater number of subtags than the language range. Every non-wildcard subtag in the language range will appear in every one of the matching language tags."

There are two types of filtering: filtering for basic language ranges (called "basic filtering") and filtering for extended language ranges (called "extended filtering"). They may return different results by what kind of language ranges are included in the given Language Priority List. `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode` is a parameter to specify how filtering should be done.

#### Lookup

The lookup operation returns the best matching language tags. It is defined in RFC 4647 as follows: "By contrast with filtering, each language range represents the most specific tag that is an acceptable match. The first matching tag found, according to the user's priority, is considered the closest match and is the item returned."

For example, if a Language Priority List consists of two language ranges, `"zh-Hant-TW"` and `"en-US"`, in prioritized order, lookup method progressively searches the language tags below in order to find the best matching language tag.

```kotlin
1. zh-Hant-TW
     2. zh-Hant
     3. zh
     4. en-US
     5. en
  
```
If there is a language tag which matches completely to a language range above, the language tag is returned.

`"*"` is the special language range, and it is ignored in lookup.

If multiple language tags match as a result of the subtag `'*'` included in a language range, the first matching language tag returned by an `https://developer.android.com/reference/kotlin/java/util/Iterator` over a `https://developer.android.com/reference/kotlin/java/util/Collection` of language tags is treated as the best matching one.

### Use of Locale

Once you've obtained a `Locale` you can query it for information about itself. Use `getCountry` to get the country (or region) code and `getLanguage` to get the language code. You can use `getDisplayCountry` to get the name of the country suitable for displaying to the user. Similarly, you can use `getDisplayLanguage` to get the name of the language suitable for displaying to the user. Interestingly, the `getDisplayXXX` methods are themselves locale-sensitive and have two versions: one that uses the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale and one that uses the locale specified as an argument.

The Java Platform provides a number of classes that perform locale-sensitive operations. For example, the `NumberFormat` class formats numbers, currency, and percentages in a locale-sensitive manner. Classes such as `NumberFormat` have several convenience methods for creating a default object of that type. For example, the `NumberFormat` class provides these three convenience methods for creating a default `NumberFormat` object: {@snippet lang=java : \* NumberFormat.getInstance(); \* NumberFormat.getCurrencyInstance(); \* NumberFormat.getPercentInstance(); \* } Each of these methods has two variants; one with an explicit locale and one without; the latter uses the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale: {@snippet lang=java : \* NumberFormat.getInstance(myLocale); \* NumberFormat.getCurrencyInstance(myLocale); \* NumberFormat.getPercentInstance(myLocale); \* } A `Locale` is the mechanism for identifying the kind of object (`NumberFormat`) that you would like to get. The locale is **just** a mechanism for identifying objects, **not** a container for the objects themselves.

### Compatibility

In order to maintain compatibility, Locale's constructors retain their behavior prior to the Java Runtime Environment version 1.7. The same is largely true for the `toString` method. Thus Locale objects can continue to be used as they were. In particular, clients who parse the output of toString into language, country, and variant fields can continue to do so (although this is strongly discouraged), although the variant field will have additional information in it if script or extensions are present.

In addition, BCP 47 imposes syntax restrictions that are not imposed by Locale's constructors. This means that conversions between some Locales and BCP 47 language tags cannot be made without losing information. Thus `toLanguageTag` cannot represent the state of locales whose language, country, or variant do not conform to BCP 47.

Because of these issues, it is recommended that clients migrate away from constructing non-conforming locales and use the `forLanguageTag` and `Locale.Builder` APIs instead. Clients desiring a string representation of the complete locale can then always rely on `toLanguageTag` for this purpose.

#### Special cases

For compatibility reasons, two non-conforming locales are treated as special cases. These are **`ja_JP_JP`** and **`th_TH_TH`**. These are ill-formed in BCP 47 since the variants are too short. To ease migration to BCP 47, these are treated specially during construction. These two cases (and only these) cause a constructor to generate an extension, all other values behave exactly as they did prior to Java 7.

Java has used `ja_JP_JP` to represent Japanese as used in Japan together with the Japanese Imperial calendar. This is now representable using a Unicode locale extension, by specifying the Unicode locale key `ca` (for "calendar") and type `japanese`. When the Locale constructor is called with the arguments "ja", "JP", "JP", the extension "u-ca-japanese" is automatically added.

Java has used `th_TH_TH` to represent Thai as used in Thailand together with Thai digits. This is also now representable using a Unicode locale extension, by specifying the Unicode locale key `nu` (for "number") and value `thai`. When the Locale constructor is called with the arguments "th", "TH", "TH", the extension "u-nu-thai" is automatically added.

#### Serialization

During serialization, writeObject writes all fields to the output stream, including extensions.

During deserialization, readResolve adds extensions as described in #, only for the two cases th_TH_TH and ja_JP_JP.

#### Legacy language codes

Locale's constructor has always converted three language codes to their earlier, obsoleted forms: `he` maps to `iw`, `yi` maps to `ji`, and `id` maps to `in`. For apps targeting and running on Android V and later, this is no longer the case. Each language maps to its new form; `iw` maps to `he`, `ji` maps to `yi`, and `in` maps to `id`.

The APIs added in 1.7 map between the old and new language codes, maintaining the mapped codes internal to Locale (so that `getLanguage` and `toString` reflect the mapped code, which depends on the `java.locale.useOldISOCodes` system property), but using the new codes in the BCP 47 language tag APIs (so that `toLanguageTag` reflects the new one). This preserves the equivalence between Locales no matter which code or API is used to construct them. Java's default resource bundle lookup mechanism also implements this mapping, so that resources can be named using either convention, see `https://developer.android.com/reference/kotlin/java/util/ResourceBundle.Control`.

#### Three-letter language/country(region) codes

The Locale constructors have always specified that the language and the country param be two characters in length, although in practice they have accepted any length. The specification has now been relaxed to allow language codes of two to eight characters and country (region) codes of two to three characters, and in particular, three-letter language codes and three-digit region codes as specified in the IANA Language Subtag Registry. For compatibility, the implementation still does not impose a length constraint.

#### Locale data

Note that locale data comes solely from ICU. User-supplied locale service providers (using the `java.text.spi` or `java.util.spi` mechanisms) are not supported.

Here are the versions of ICU (and the corresponding CLDR and Unicode versions) used in various Android releases:

| Android 1.5 (Cupcake)/Android 1.6 (Donut)/Android 2.0 (Eclair) | ICU 3.8 | [CLDR 1.5](http://cldr.unicode.org/index/downloads/cldr-1-5) | [Unicode 5.0](http://www.unicode.org/versions/Unicode5.0.0/) |
| Android 2.2 (Froyo) | ICU 4.2 | [CLDR 1.7](http://cldr.unicode.org/index/downloads/cldr-1-7) | [Unicode 5.1](http://www.unicode.org/versions/Unicode5.1.0/) |
| Android 2.3 (Gingerbread)/Android 3.0 (Honeycomb) | ICU 4.4 | [CLDR 1.8](http://cldr.unicode.org/index/downloads/cldr-1-8) | [Unicode 5.2](http://www.unicode.org/versions/Unicode5.2.0/) |
| Android 4.0 (Ice Cream Sandwich) | [ICU 4.6](http://site.icu-project.org/download/46) | [CLDR 1.9](http://cldr.unicode.org/index/downloads/cldr-1-9) | [Unicode 6.0](http://www.unicode.org/versions/Unicode6.0.0/) |
| Android 4.1 (Jelly Bean) | [ICU 4.8](http://site.icu-project.org/download/48) | [CLDR 2.0](http://cldr.unicode.org/index/downloads/cldr-2-0) | [Unicode 6.0](http://www.unicode.org/versions/Unicode6.0.0/) |
| Android 4.3 (Jelly Bean MR2) | [ICU 50](http://site.icu-project.org/download/50) | [CLDR 22.1](http://cldr.unicode.org/index/downloads/cldr-22-1) | [Unicode 6.2](http://www.unicode.org/versions/Unicode6.2.0/) |
| Android 4.4 (KitKat) | [ICU 51](http://site.icu-project.org/download/51) | [CLDR 23](http://cldr.unicode.org/index/downloads/cldr-23) | [Unicode 6.2](http://www.unicode.org/versions/Unicode6.2.0/) |
| Android 5.0 (Lollipop) | [ICU 53](http://site.icu-project.org/download/53) | [CLDR 25](http://cldr.unicode.org/index/downloads/cldr-25) | [Unicode 6.3](http://www.unicode.org/versions/Unicode6.3.0/) |
| Android 6.0 (Marshmallow) | [ICU 55.1](http://site.icu-project.org/download/55) | [CLDR 27.0.1](http://cldr.unicode.org/index/downloads/cldr-27) | [Unicode 7.0](http://www.unicode.org/versions/Unicode7.0.0/) |
| Android 7.0 (Nougat) | [ICU 56.1](http://site.icu-project.org/download/56) | [CLDR 28](http://cldr.unicode.org/index/downloads/cldr-28) | [Unicode 8.0](http://www.unicode.org/versions/Unicode8.0.0/) |
| Android 8.0 (Oreo) | [ICU 58.2](http://site.icu-project.org/download/58) | [CLDR 30.0.3](http://cldr.unicode.org/index/downloads/cldr-30) | [Unicode 9.0](http://www.unicode.org/versions/Unicode9.0.0/) |
| Android 9.0 (Pie) | [ICU 60.2](http://site.icu-project.org/download/60) | [CLDR 32.0.1](http://cldr.unicode.org/index/downloads/cldr-32) | [Unicode 10.0](http://www.unicode.org/versions/Unicode10.0.0/) |
| Android 10.0 (Q) | [ICU 63.2](http://site.icu-project.org/download/63) | [CLDR 34](http://cldr.unicode.org/index/downloads/cldr-34) | [Unicode 11.0](http://www.unicode.org/versions/Unicode11.0.0/) |

#### Be wary of the default locale

Note that there are many convenience methods that automatically use the default locale, but using them may lead to subtle bugs.

The default locale is appropriate for tasks that involve presenting data to the user. In this case, you want to use the user's date/time formats, number formats, rules for conversion to lowercase, and so on. In this case, it's safe to use the convenience methods.

The default locale is *not* appropriate for machine-readable output. The best choice there is usually `Locale.US` -- this locale is guaranteed to be available on all devices, and the fact that it has no surprising special cases and is frequently used (especially for computer-computer communication) means that it tends to be the most efficient choice too.

A common mistake is to implicitly use the default locale when producing output meant to be machine-readable. This tends to work on the developer's test devices (especially because so many developers use en_US), but fails when run on a device whose user is in a more complex locale.

For example, if you're formatting integers some locales will use non-ASCII decimal digits. As another example, if you're formatting floating-point numbers some locales will use `','` as the decimal point and `'.'` for digit grouping. That's correct for human-readable output, but likely to cause problems if presented to another computer (`https://developer.android.com/reference/kotlin/java/lang/Double.html#parseDouble(kotlin.String)` can't parse such a number, for example). You should also be wary of the java.lang.String#toLowerCase and java.lang.String#toUpperCase overloads that don't take a `Locale`: in Turkey, for example, the characters `'i'` and `'I'` won't be converted to `'I'` and `'i'`. This is the correct behavior for Turkish text (such as user input), but inappropriate for, say, HTTP headers.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/java/util/Locale.Builder` `Builder` is used to build instances of `Locale` from values configured by the setters. |
| | `https://developer.android.com/reference/kotlin/java/util/Locale.Category` Enum for locale categories. |
| | `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode` This enum provides constants to select a filtering mode for locale matching. |
| | `https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode` Enum for specifying the type defined in ISO 3166. |
| | `https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange` This class expresses a *Language Range* defined in [RFC 4647 Matching of Language Tags](https://tools.ietf.org/html/rfc4647). |

| Constants ||
|---|---|
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#PRIVATE_USE_EXTENSION:kotlin.Char` The key for the private use extension ('x'). |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#UNICODE_LOCALE_EXTENSION:kotlin.Char` The key for Unicode locale extension ('u'). |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#Locale(kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Construct a locale from a language code. |
| `https://developer.android.com/reference/kotlin/java/util/Locale#Locale(kotlin.String,%20kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, country: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Construct a locale from language and country. |
| `https://developer.android.com/reference/kotlin/java/util/Locale#Locale(kotlin.String,%20kotlin.String,%20kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, country: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, variant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Construct a locale from language, country and variant. |

| Public methods ||
|---|---|
| static [Stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#availableLocales()()` {@return a stream of installed locales} At a minimum, the returned stream must contain a `Locale` instance equal to `https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale`. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#clone()()` Overrides Cloneable. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns true if this Locale is equal to another object. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#filter(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, locales: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>)` Returns a list of matching `Locale` instances using the filtering mechanism defined in RFC 4647. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#filter(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection,%20java.util.Locale.FilteringMode)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, locales: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>, mode: https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode)` Returns a list of matching `Locale` instances using the filtering mechanism defined in RFC 4647. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#filterTags(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, tags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Returns a list of matching languages tags using the basic filtering mechanism defined in RFC 4647. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#filterTags(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection,%20java.util.Locale.FilteringMode)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, tags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>, mode: https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode)` Returns a list of matching languages tags using the basic filtering mechanism defined in RFC 4647. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#forLanguageTag(kotlin.String)(languageTag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns a locale for the specified IETF BCP 47 language tag string. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getAvailableLocales()()` Returns an array of all installed locales. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getCountry()()` Returns the country/region code for this locale, which should either be the empty string, an uppercase ISO 3166 2-letter code, or a UN M. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDefault()()` Gets the current value of the default locale for this instance of the Java Virtual Machine. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDefault(java.util.Locale.Category)(category: https://developer.android.com/reference/kotlin/java/util/Locale.Category)` Gets the current value of the default locale for the specified Category for this instance of the Java Virtual Machine. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayCountry()()` Returns a name for the locale's country that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayCountry(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Returns the name of this locale's country, localized to `locale`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayLanguage()()` Returns a name for the locale's language that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayLanguage(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Returns the name of this locale's language, localized to `locale`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayName()()` Returns a name for the locale that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayName(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Returns this locale's language name, country name, and variant, localized to `locale`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayScript()()` Returns a name for the locale's script that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayScript(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Returns a name for the locale's script that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayVariant()()` Returns a name for the locale's variant code that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getDisplayVariant(java.util.Locale)(inLocale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Returns a name for the locale's variant code that is appropriate for display to the user. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/util/Locale#getExtension(kotlin.Char)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the extension (or private use) value associated with the specified key, or null if there is no extension associated with the key. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getExtensionKeys()()` Returns the set of extension keys associated with this locale, or the empty set if it has no extensions. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getISO3Country()()` {@return a three-letter abbreviation of this locale's country} If the country matches an ISO 3166-1 alpha-2 code, the corresponding ISO 3166-1 alpha-3 uppercase code is returned. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getISO3Language()()` {@return a three-letter abbreviation of this locale's language} If the language matches an ISO 639-1 two-letter code, the corresponding ISO 639-2/T three-letter lowercase code is returned. |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getISOCountries()()` Returns a list of all 2-letter country codes defined in ISO 3166. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getISOCountries(java.util.Locale.IsoCountryCode)(type: https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode)` {@return a {@code Set} of ISO3166 country codes for the specified type} |
| static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getISOLanguages()()` Returns a list of all 2-letter language codes and some of 3-letter codes defined in ISO 639. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getLanguage()()` Returns the language code of this Locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getScript()()` Returns the script for this locale, which should either be the empty string or an ISO 15924 4-letter script code. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleAttributes()()` Returns the set of unicode locale attributes associated with this locale, or the empty set if it has no attributes. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleKeys()()` Returns the set of Unicode locale keys defined by this locale, or the empty set if this locale has none. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/util/Locale#getUnicodeLocaleType(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the Unicode locale type associated with the specified Unicode locale key for this locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#getVariant()()` Returns the variant code for this locale. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#hasExtensions()()` Returns `true` if this `Locale` has any #. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#hashCode()()` Override hashCode. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)? | `https://developer.android.com/reference/kotlin/java/util/Locale#lookup(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, locales: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>)` Returns a `Locale` instance for the best-matching language tag using the lookup mechanism defined in RFC 4647. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/java/util/Locale#lookupTag(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection)(priorityList: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange!>, tags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>)` Returns the best-matching language tag using the lookup mechanism defined in RFC 4647. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#of(kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Obtains a locale from a language code. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#of(kotlin.String,%20kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, country: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Obtains a locale from language and country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#of(kotlin.String,%20kotlin.String,%20kotlin.String)(language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, country: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, variant: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Obtains a locale from language, country and variant. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#setDefault(java.util.Locale)(newLocale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Sets the default locale for this instance of the Java Virtual Machine. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#setDefault(java.util.Locale.Category,%20java.util.Locale)(category: https://developer.android.com/reference/kotlin/java/util/Locale.Category, newLocale: https://developer.android.com/reference/kotlin/java/util/Locale#)` Sets the default locale for the specified Category for this instance of the Java Virtual Machine. |
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#stripExtensions()()` Returns a copy of this `Locale` with no #. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#toLanguageTag()()` Returns a well-formed IETF BCP 47 language tag representing this locale. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/Locale#toString()()` Returns a string representation of this `Locale` object, consisting of language, country, variant, script, and extensions as below: language + "_" + country + "_" + (variant + "_#" | "#") + script + "_" + extensions Language is always lower case, country is always upper case, script is always title case, and extensions are always lower case. |

| Properties ||
|---|---|
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#CANADA:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#CANADA_FRENCH:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#CHINA:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#CHINESE:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#ENGLISH:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#FRANCE:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#FRENCH:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#GERMAN:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#GERMANY:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#ITALIAN:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#ITALY:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#JAPAN:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#JAPANESE:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#KOREA:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#KOREAN:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#PRC:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#ROOT:java.util.Locale` Useful constant for the root locale. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#SIMPLIFIED_CHINESE:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#TAIWAN:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#TRADITIONAL_CHINESE:java.util.Locale` Useful constant for language. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#UK:java.util.Locale` Useful constant for country. |
| static [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#) | `https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale` Useful constant for country. |

## Constants

### PRIVATE_USE_EXTENSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRIVATE_USE_EXTENSION: Char
```

The key for the private use extension ('x').

 Value: 'x'

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#getExtension(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/util/Locale.Builder#setExtension(kotlin.Char,%20kotlin.String)`

### UNICODE_LOCALE_EXTENSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICODE_LOCALE_EXTENSION: Char
```

The key for Unicode locale extension ('u').

 Value: 'u'

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#getExtension(kotlin.Char)`
- `https://developer.android.com/reference/kotlin/java/util/Locale.Builder#setExtension(kotlin.Char,%20kotlin.String)`

## Public constructors

### Locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Locale(language: String)
```

**Deprecated:** *Locale constructors have been deprecated. See # for other options.*

Construct a locale from a language code. This constructor normalizes the language value to lowercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): An ISO 639 alpha-2 or alpha-3 language code, or a language subtag up to 8 characters in length. See the `Locale` class description about valid language values. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if argument is null. |

### Locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Locale(
    language: String, 
    country: String)
```

**Deprecated:** *Locale constructors have been deprecated. See # for other options.*

Construct a locale from language and country. This constructor normalizes the language value to lowercase and the country value to uppercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): An ISO 639 alpha-2 or alpha-3 language code, or a language subtag up to 8 characters in length. See the `Locale` class description about valid language values. |
| `country` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): An ISO 3166 alpha-2 country code or a UN M.49 numeric-3 area code. See the `Locale` class description about valid country values. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if either argument is null. |

### Locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Locale(
    language: String, 
    country: String, 
    variant: String)
```

**Deprecated:** *Locale constructors have been deprecated. See # for other options.*

Construct a locale from language, country and variant. This constructor normalizes the language value to lowercase and the country value to uppercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): An ISO 639 alpha-2 or alpha-3 language code, or a language subtag up to 8 characters in length. See the `Locale` class description about valid language values. |
| `country` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): An ISO 3166 alpha-2 country code or a UN M.49 numeric-3 area code. See the `Locale` class description about valid country values. |
| `variant` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Any arbitrary value used to indicate a variation of a `Locale`. See the `Locale` class description for the details. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if any argument is null. |

## Public methods

### availableLocales

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun availableLocales(): Stream<Locale!>
```

{@return a stream of installed locales} At a minimum, the returned stream must contain a `Locale` instance equal to `https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale`.

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clone(): Any
```

Overrides Cloneable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Returns true if this Locale is equal to another object. A Locale is deemed equal to another Locale with identical language, script, country, variant and extensions, and unequal to all other objects.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this Locale is equal to the specified object. |

### filter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun filter(
    priorityList: MutableList<Locale.LanguageRange!>, 
    locales: MutableCollection<Locale!>
): MutableList<Locale!>
```

Returns a list of matching `Locale` instances using the filtering mechanism defined in RFC 4647. This is equivalent to `https://developer.android.com/reference/kotlin/java/util/Locale#filter(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection,%20java.util.Locale.FilteringMode)` when `mode` is `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode`. This filter operation on the given `locales` ensures that only unique matching locale(s) are returned.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `locales` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\>: `Locale` instances used for matching |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>` | a list of `Locale` instances for matching language tags sorted in descending order based on priority or weight, or an empty list if nothing matches. The list is modifiable. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `priorityList` or `locales` is `null` |

### filter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun filter(
    priorityList: MutableList<Locale.LanguageRange!>, 
    locales: MutableCollection<Locale!>, 
    mode: Locale.FilteringMode
): MutableList<Locale!>
```

Returns a list of matching `Locale` instances using the filtering mechanism defined in RFC 4647. This filter operation on the given `locales` ensures that only unique matching locale(s) are returned.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `locales` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\>: `Locale` instances used for matching |
| `mode` | [Locale.FilteringMode](https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode): filtering mode |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>` | a list of `Locale` instances for matching language tags sorted in descending order based on priority or weight, or an empty list if nothing matches. The list is modifiable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one or more extended language ranges are included in the given list when `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode` is specified |
| `java.lang.NullPointerException` | if `priorityList` or `locales` is `null` |

### filterTags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun filterTags(
    priorityList: MutableList<Locale.LanguageRange!>, 
    tags: MutableCollection<String!>
): MutableList<String!>
```

Returns a list of matching languages tags using the basic filtering mechanism defined in RFC 4647. This is equivalent to `https://developer.android.com/reference/kotlin/java/util/Locale#filterTags(kotlin.collections.MutableList,%20kotlin.collections.MutableCollection,%20java.util.Locale.FilteringMode)` when `mode` is `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode`. This filter operation on the given `tags` ensures that only unique matching tag(s) are returned with preserved case. In case of duplicate matching tags with the case difference, the first matching tag with preserved case is returned. For example, "de-ch" is returned out of the duplicate matching tags "de-ch" and "de-CH", if "de-ch" is checked first for matching in the given `tags`. Note that if the given `tags` is an unordered `Collection`, the returned matching tag out of duplicate tags is subject to change, depending on the implementation of the `Collection`.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `tags` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: language tags |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | a list of matching language tags sorted in descending order based on priority or weight, or an empty list if nothing matches. The list is modifiable. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `priorityList` or `tags` is `null` |

### filterTags

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun filterTags(
    priorityList: MutableList<Locale.LanguageRange!>, 
    tags: MutableCollection<String!>, 
    mode: Locale.FilteringMode
): MutableList<String!>
```

Returns a list of matching languages tags using the basic filtering mechanism defined in RFC 4647. This filter operation on the given `tags` ensures that only unique matching tag(s) are returned with preserved case. In case of duplicate matching tags with the case difference, the first matching tag with preserved case is returned. For example, "de-ch" is returned out of the duplicate matching tags "de-ch" and "de-CH", if "de-ch" is checked first for matching in the given `tags`. Note that if the given `tags` is an unordered `Collection`, the returned matching tag out of duplicate tags is subject to change, depending on the implementation of the `Collection`.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `tags` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: language tags |
| `mode` | [Locale.FilteringMode](https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode): filtering mode |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | a list of matching language tags sorted in descending order based on priority or weight, or an empty list if nothing matches. The list is modifiable. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if one or more extended language ranges are included in the given list when `https://developer.android.com/reference/kotlin/java/util/Locale.FilteringMode` is specified |
| `java.lang.NullPointerException` | if `priorityList` or `tags` is `null` |

### forLanguageTag

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun forLanguageTag(languageTag: String): Locale
```

Returns a locale for the specified IETF BCP 47 language tag string.

If the specified language tag contains any ill-formed subtags, the first such subtag and all following subtags are ignored. Compare to `https://developer.android.com/reference/kotlin/java/util/Locale.Builder#setLanguageTag(kotlin.String)` which throws an exception in this case.

The following **conversions** are performed:

- The language code "und" is mapped to language "".
- The language codes "iw", "ji", and "in" are mapped to "he", "yi", and "id" respectively. (This is the same canonicalization that's done in Locale's constructors.) See # for more information.
- The portion of a private use subtag prefixed by "lvariant", if any, is removed and appended to the variant field in the result locale (without case normalization). If it is then empty, the private use subtag is discarded: {@snippet lang=java : \* Locale loc; \* loc = Locale.forLanguageTag("en-US-x-lvariant-POSIX"); \* loc.getVariant(); // returns "POSIX" \* loc.getExtension('x'); // returns null \* \* loc = Locale.forLanguageTag("de-POSIX-x-URP-lvariant-Abc-Def"); \* loc.getVariant(); // returns "POSIX_Abc_Def" \* loc.getExtension('x'); // returns "urp" \* }
- When the languageTag argument contains an extlang subtag, the first such subtag is used as the language, and the primary language subtag and other extlang subtags are ignored: {@snippet lang=java : \* Locale.forLanguageTag("ar-aao").getLanguage(); // returns "aao" \* Locale.forLanguageTag("en-abc-def-us").toString(); // returns "abc_US" \* }
- Case is normalized except for variant tags, which are left unchanged. Language is normalized to lower case, script to title case, country to upper case, and extensions to lower case.
- If, after processing, the locale would exactly match either ja_JP_JP or th_TH_TH with no extensions, the appropriate extensions are added as though the constructor had been called: {@snippet lang=java : \* Locale.forLanguageTag("ja-JP-x-lvariant-JP").toLanguageTag(); \* // returns "ja-JP-u-ca-japanese-x-lvariant-JP" \* Locale.forLanguageTag("th-TH-x-lvariant-TH").toLanguageTag(); \* // returns "th-TH-u-nu-thai-x-lvariant-TH" \* }

This implements the 'Language-Tag' production of BCP47, and so supports legacy (regular and irregular, referred to as "Type: grandfathered" in BCP47) as well as private use language tags. Stand alone private use tags are represented as empty language and extension 'x-whatever', and legacy tags are converted to their canonical replacements where they exist.

Legacy tags with canonical replacements are as follows:

| legacy tag | modern replacement |
| art-lojban | jbo |
| i-ami | ami |
| i-bnn | bnn |
| i-hak | hak |
| i-klingon | tlh |
| i-lux | lb |
| i-navajo | nv |
| i-pwn | pwn |
| i-tao | tao |
| i-tay | tay |
| i-tsu | tsu |
| no-bok | nb |
| no-nyn | nn |
| sgn-BE-FR | sfb |
| sgn-BE-NL | vgt |
| sgn-CH-DE | sgg |
| zh-guoyu | cmn |
| zh-hakka | hak |
| zh-min-nan | nan |
| zh-xiang | hsn |
|---|---|

Legacy tags with no modern replacement will be converted as follows:

| legacy tag | converts to |
| cel-gaulish | xtg-x-cel-gaulish |
| en-GB-oed | en-GB-x-oed |
| i-default | en-x-i-default |
| i-enochian | und-x-i-enochian |
| i-mingo | see-x-i-mingo |
| zh-min | nan-x-zh-min |
|---|---|

For a list of all legacy tags, see the IANA Language Subtag Registry (search for "Type: grandfathered").

**Note** : there is no guarantee that `toLanguageTag` and `forLanguageTag` will round-trip.

| Parameters ||
|---|---|
| `languageTag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the language tag |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | The locale that best represents the language tag. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `languageTag` is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#toLanguageTag()`
- `https://developer.android.com/reference/kotlin/java/util/Locale.Builder#setLanguageTag(kotlin.String)`

### getAvailableLocales

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableLocales(): Array<Locale!>
```

Returns an array of all installed locales.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/Locale#!>` | An array of installed locales. At a minimum, the returned array must contain a `Locale` instance equal to `https://developer.android.com/reference/kotlin/java/util/Locale#US:java.util.Locale`. |

### getCountry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCountry(): String
```

Returns the country/region code for this locale, which should either be the empty string, an uppercase ISO 3166 2-letter code, or a UN M.49 3-digit code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The country/region code, or the empty string if none is defined. |

**See Also**

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefault(): Locale
```

Gets the current value of the default locale for this instance of the Java Virtual Machine.

The Java Virtual Machine sets the default locale during startup based on the host environment. It is used by many locale-sensitive methods if no locale is explicitly specified. It can be changed using the `https://developer.android.com/reference/kotlin/java/util/Locale#setDefault(java.util.Locale)` method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | the default locale for this instance of the Java Virtual Machine |

### getDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefault(category: Locale.Category): Locale
```

Gets the current value of the default locale for the specified Category for this instance of the Java Virtual Machine.

The Java Virtual Machine sets the default locale during startup based on the host environment. It is used by many locale-sensitive methods if no locale is explicitly specified. It can be changed using the setDefault(Locale.Category, Locale) method.

| Parameters ||
|---|---|
| `category` | [Locale.Category](https://developer.android.com/reference/kotlin/java/util/Locale.Category): the specified category to get the default locale |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | the default locale for the specified Category for this instance of the Java Virtual Machine |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if category is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#setDefault(java.util.Locale.Category,%20java.util.Locale)`

### getDisplayCountry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayCountry(): String
```

Returns a name for the locale's country that is appropriate for display to the user. If possible, the name returned will be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale. For example, if the locale is fr_FR and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale is en_US, getDisplayCountry() will return "France"; if the locale is en_US and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale is fr_FR, getDisplayCountry() will return "Etats-Unis". If the name returned cannot be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale, (say, we don't have a Japanese name for Croatia), this function falls back on the English name, and uses the ISO code as a last-resort value. If the locale doesn't specify a country, this function returns the empty string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the country appropriate to the locale. |

### getDisplayCountry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayCountry(locale: Locale): String
```

Returns the name of this locale's country, localized to `locale`. Returns the empty string if this locale does not correspond to a specific country.

### getDisplayLanguage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayLanguage(): String
```

Returns a name for the locale's language that is appropriate for display to the user. If possible, the name returned will be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale. For example, if the locale is fr_FR and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale is en_US, getDisplayLanguage() will return "French"; if the locale is en_US and the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale is fr_FR, getDisplayLanguage() will return "anglais". If the name returned cannot be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale, (say, we don't have a Japanese name for Croatian), this function falls back on the English name, and uses the ISO code as a last-resort value. If the locale doesn't specify a language, this function returns the empty string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the display language. |

### getDisplayLanguage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayLanguage(locale: Locale): String
```

Returns the name of this locale's language, localized to `locale`. If the language name is unknown, the language code is returned.

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(): String
```

Returns a name for the locale that is appropriate for display to the user. This will be the values returned by getDisplayLanguage(), getDisplayScript(), getDisplayCountry(), getDisplayVariant() and optional # assembled into a single string. The non-empty values are used in order, with the second and subsequent names in parentheses. For example: language (script, country, variant(, extension)\*) 
language (country(, extension)\*) 
language (variant(, extension)\*) 
script (country(, extension)\*) 
country (extension)\* 
depending on which fields are specified in the locale. The field separator in the above parentheses, denoted as a comma character, may be localized depending on the locale. If the language, script, country, and variant fields are all empty, this function returns the empty string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the locale appropriate to display. |

### getDisplayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayName(locale: Locale): String
```

Returns this locale's language name, country name, and variant, localized to `locale`. The exact output form depends on whether this locale corresponds to a specific language, script, country and variant.

For example:

- `new Locale("en").getDisplayName(Locale.US)` -\> `English`
- `new Locale("en", "US").getDisplayName(Locale.US)` -\> `English (United States)`
- `new Locale("en", "US", "POSIX").getDisplayName(Locale.US)` -\> `English (United States,Computer)`
- `Locale.forLanguageTag("zh-Hant-CN").getDisplayName(Locale.US)` -\> `Chinese (Traditional Han,China)`
- `new Locale("en").getDisplayName(Locale.FRANCE)` -\> `anglais`
- `new Locale("en", "US").getDisplayName(Locale.FRANCE)` -\> `anglais (États-Unis)`
- `new Locale("en", "US", "POSIX").getDisplayName(Locale.FRANCE)` -\> `anglais (États-Unis,informatique)`.

### getDisplayScript

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayScript(): String
```

Returns a name for the locale's script that is appropriate for display to the user. If possible, the name will be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale. Returns the empty string if this locale doesn't specify a script code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the display name of the script code for the current default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale |

### getDisplayScript

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayScript(inLocale: Locale): String
```

Returns a name for the locale's script that is appropriate for display to the user. If possible, the name will be localized for the given locale. Returns the empty string if this locale doesn't specify a script code.

| Parameters ||
|---|---|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#): The locale for which to retrieve the display script. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the display name of the script code for the current default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `inLocale` is `null` |

### getDisplayVariant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayVariant(): String
```

Returns a name for the locale's variant code that is appropriate for display to the user. If possible, the name will be localized for the default `https://developer.android.com/reference/kotlin/java/util/Locale.Category` locale. If the locale doesn't specify a variant code, this function returns the empty string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the display variant code appropriate to the locale. |

### getDisplayVariant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDisplayVariant(inLocale: Locale): String
```

Returns a name for the locale's variant code that is appropriate for display to the user. If possible, the name will be localized for inLocale. If the locale doesn't specify a variant code, this function returns the empty string.

| Parameters ||
|---|---|
| `inLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#): The locale for which to retrieve the display variant code. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the display variant code appropriate to the given locale. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `inLocale` is `null` |

### getExtension

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtension(key: Char): String?
```

Returns the extension (or private use) value associated with the specified key, or null if there is no extension associated with the key. To be well-formed, the key must be one of `[0-9A-Za-z]`. Keys are case-insensitive, so for example 'z' and 'Z' represent the same extension.

| Parameters ||
|---|---|
| `key` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the extension key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The extension, or null if this locale defines no extension for the specified key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if key is not well-formed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#PRIVATE_USE_EXTENSION:kotlin.Char`
- `https://developer.android.com/reference/kotlin/java/util/Locale#UNICODE_LOCALE_EXTENSION:kotlin.Char`

### getExtensionKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtensionKeys(): MutableSet<Char!>
```

Returns the set of extension keys associated with this locale, or the empty set if it has no extensions. The returned set is unmodifiable. The keys will all be lower-case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html!>` | The set of extension keys, or the empty set if this locale has no extensions. |

### getISO3Country

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getISO3Country(): String
```

{@return a three-letter abbreviation of this locale's country} If the country matches an ISO 3166-1 alpha-2 code, the corresponding ISO 3166-1 alpha-3 uppercase code is returned. If the locale doesn't specify a country, this will be the empty string.

The ISO 3166-1 codes can be found on-line.

| Exceptions ||
|---|---|
| `java.util.MissingResourceException` | Throws MissingResourceException if the three-letter country abbreviation is not available for this locale. |

### getISO3Language

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getISO3Language(): String
```

{@return a three-letter abbreviation of this locale's language} If the language matches an ISO 639-1 two-letter code, the corresponding ISO 639-2/T three-letter lowercase code is returned. The ISO 639-2 language codes can be found on-line, see "Codes for the Representation of Names of Languages Part 2: Alpha-3 Code". If the locale specifies a three-letter language, the language is returned as is. If the locale does not specify a language the empty string is returned.

| Exceptions ||
|---|---|
| `java.util.MissingResourceException` | Throws MissingResourceException if three-letter language abbreviation is not available for this locale. |

### getISOCountries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getISOCountries(): Array<String!>
```

Returns a list of all 2-letter country codes defined in ISO 3166. Can be used to obtain Locales. This method is equivalent to `https://developer.android.com/reference/kotlin/java/util/Locale#getISOCountries(java.util.Locale.IsoCountryCode)` with `type` `https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode`.

**Note:** The `Locale` class also supports other codes for country (region), such as 3-letter numeric UN M.49 area codes. Therefore, the list returned by this method does not contain ALL valid codes that can be used to obtain Locales.

Note that this method does not return obsolete 2-letter country codes. ISO3166-3 codes which designate country codes for those obsolete codes, can be retrieved from `https://developer.android.com/reference/kotlin/java/util/Locale#getISOCountries(java.util.Locale.IsoCountryCode)` with `type` `https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | An array of ISO 3166 two-letter country codes. |

### getISOCountries

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getISOCountries(type: Locale.IsoCountryCode): MutableSet<String!>
```

{@return a {@code Set} of ISO3166 country codes for the specified type}

| Parameters ||
|---|---|
| `type` | [Locale.IsoCountryCode](https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode): `https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode` specified ISO code type. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if type is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale.IsoCountryCode`

### getISOLanguages

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getISOLanguages(): Array<String!>
```

Returns a list of all 2-letter language codes and some of 3-letter codes defined in ISO 639. Can be used to obtain Locales.

**Note:**

- ISO 639 is not a stable standard--- some languages' codes have changed. The list this function returns includes both the new and the old codes for the languages whose codes have changed.
- The `Locale` class also supports language codes up to 8 characters in length. Therefore, the list returned by this method does not contain ALL valid codes that can be used to obtain Locales.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | An array of ISO 639 language codes. |

### getLanguage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLanguage(): String
```

Returns the language code of this Locale.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The language code, or the empty string if none is defined. |

**See Also**

### getScript

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScript(): String
```

Returns the script for this locale, which should either be the empty string or an ISO 15924 4-letter script code. The first letter is uppercase and the rest are lowercase, for example, 'Latn', 'Cyrl'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The script code, or the empty string if none is defined. |

**See Also**

### getUnicodeLocaleAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUnicodeLocaleAttributes(): MutableSet<String!>
```

Returns the set of unicode locale attributes associated with this locale, or the empty set if it has no attributes. The returned set is unmodifiable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The set of attributes. |

### getUnicodeLocaleKeys

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUnicodeLocaleKeys(): MutableSet<String!>
```

Returns the set of Unicode locale keys defined by this locale, or the empty set if this locale has none. The returned set is immutable. Keys are all lower case.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The set of Unicode locale keys, or the empty set if this locale has no Unicode locale keywords. |

### getUnicodeLocaleType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUnicodeLocaleType(key: String): String?
```

Returns the Unicode locale type associated with the specified Unicode locale key for this locale. Returns the empty string for keys that are defined with no type. Returns null if the key is not defined. Keys are case-insensitive. The key must be two alphanumeric characters (\[0-9a-zA-Z\]), or an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the Unicode locale key |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The Unicode locale type associated with the key, or null if the locale does not define the key. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the key is not well-formed |
| `java.lang.NullPointerException` | if `key` is null |

### getVariant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVariant(): String
```

Returns the variant code for this locale.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The variant code, or the empty string if none is defined. |

**See Also**

### hasExtensions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasExtensions(): Boolean
```

Returns `true` if this `Locale` has any #.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `Locale` has any extensions |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Override hashCode. Since Locales are often used in hashtables, caches the value for speed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### lookup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lookup(
    priorityList: MutableList<Locale.LanguageRange!>, 
    locales: MutableCollection<Locale!>
): Locale?
```

Returns a `Locale` instance for the best-matching language tag using the lookup mechanism defined in RFC 4647.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `locales` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#)!\>: `Locale` instances used for matching |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#?` | the best matching `Locale` instance chosen based on priority or weight, or `null` if nothing matches. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `priorityList` or `locales` is `null` |

### lookupTag

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun lookupTag(
    priorityList: MutableList<Locale.LanguageRange!>, 
    tags: MutableCollection<String!>
): String?
```

Returns the best-matching language tag using the lookup mechanism defined in RFC 4647. This lookup operation on the given `tags` ensures that the first matching tag with preserved case is returned.

| Parameters ||
|---|---|
| `priorityList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Locale.LanguageRange](https://developer.android.com/reference/kotlin/java/util/Locale.LanguageRange)!\>: user's Language Priority List in which each language tag is sorted in descending order based on priority or weight |
| `tags` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>: language tags used for matching |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the best matching language tag chosen based on priority or weight, or `null` if nothing matches. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `priorityList` or `tags` is `null` |

### of

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(language: String): Locale
```

Obtains a locale from a language code. This method normalizes the language value to lowercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A language code. See the `Locale` class description of # values. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | A `Locale` object |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if argument is null. |

### of

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    language: String, 
    country: String
): Locale
```

Obtains a locale from language and country. This method normalizes the language value to lowercase and the country value to uppercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A language code. See the `Locale` class description of # values. |
| `country` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A country code. See the `Locale` class description of # values. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | A `Locale` object |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if either argument is null. |

### of

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun of(
    language: String, 
    country: String, 
    variant: String
): Locale
```

Obtains a locale from language, country and variant. This method normalizes the language value to lowercase and the country value to uppercase.

| Parameters ||
|---|---|
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A language code. See the `Locale` class description of # values. |
| `country` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A country code. See the `Locale` class description of # values. |
| `variant` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Any arbitrary value used to indicate a variation of a `Locale`. See the `Locale` class description of # values. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | A `Locale` object |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | thrown if any argument is null. |

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setDefault(newLocale: Locale): Unit
```

Sets the default locale for this instance of the Java Virtual Machine. This does not affect the host locale.

If there is a security manager, its `checkPermission` method is called with a `PropertyPermission("user.language", "write")` permission before the default locale is changed.

The Java Virtual Machine sets the default locale during startup based on the host environment. It is used by many locale-sensitive methods if no locale is explicitly specified.

Since changing the default locale may affect many different areas of functionality, this method should only be used if the caller is prepared to reinitialize locale-sensitive code running within the same Java Virtual Machine.

By setting the default locale with this method, all of the default locales for each Category are also set to the specified default locale.

| Parameters ||
|---|---|
| `newLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#): the new default locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if `newLocale` is null |
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method doesn't allow the operation. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/PropertyPermission`

### setDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setDefault(
    category: Locale.Category, 
    newLocale: Locale
): Unit
```

Sets the default locale for the specified Category for this instance of the Java Virtual Machine. This does not affect the host locale.

If there is a security manager, its checkPermission method is called with a PropertyPermission("user.language", "write") permission before the default locale is changed.

The Java Virtual Machine sets the default locale during startup based on the host environment. It is used by many locale-sensitive methods if no locale is explicitly specified.

Since changing the default locale may affect many different areas of functionality, this method should only be used if the caller is prepared to reinitialize locale-sensitive code running within the same Java Virtual Machine.

| Parameters ||
|---|---|
| `category` | [Locale.Category](https://developer.android.com/reference/kotlin/java/util/Locale.Category): the specified category to set the default locale |
| `newLocale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale#): the new default locale |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if category and/or newLocale is null |
| `java.lang.SecurityException` | if a security manager exists and its checkPermission method doesn't allow the operation. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkPermission(java.security.Permission)`
- `https://developer.android.com/reference/kotlin/java/util/PropertyPermission`
- `https://developer.android.com/reference/kotlin/java/util/Locale#getDefault(java.util.Locale.Category)`

### stripExtensions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stripExtensions(): Locale
```

Returns a copy of this `Locale` with no #. If this `Locale` has no extensions, this `Locale` is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale#` | a copy of this `Locale` with no extensions, or `this` if `this` has no extensions |

### toLanguageTag

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLanguageTag(): String
```

Returns a well-formed IETF BCP 47 language tag representing this locale.

If this `Locale` has a language, country, or variant that does not satisfy the IETF BCP 47 language tag syntax requirements, this method handles these fields as described below:

**Language:** If language is empty, or not # (for example "a" or "e2"), it will be emitted as "und" (Undetermined).

**Country:** If country is not # (for example "12" or "USA"), it will be omitted.

**Variant:** If variant **is** #, each sub-segment (delimited by '-' or '_') is emitted as a subtag. Otherwise:

- if all sub-segments match `[0-9a-zA-Z]{1,8}` (for example "WIN" or "Oracle_JDK_Standard_Edition"), the first ill-formed sub-segment and all following will be appended to the private use subtag. The first appended subtag will be "lvariant", followed by the sub-segments in order, separated by hyphen. For example, "x-lvariant-WIN", "Oracle-x-lvariant-JDK-Standard-Edition".
- if any sub-segment does not match `[0-9a-zA-Z]{1,8}`, the variant will be truncated and the problematic sub-segment and all following sub-segments will be omitted. If the remainder is non-empty, it will be emitted as a private use subtag as above (even if the remainder turns out to be well-formed). For example, "Solaris_isjustthecoolestthing" is emitted as "x-lvariant-Solaris", not as "solaris".

**Special Conversions:** Java supports some old locale representations, including deprecated ISO language codes, for compatibility. This method performs the following conversions:

- Deprecated ISO language codes "iw", "ji", and "in" are converted to "he", "yi", and "id", respectively.
- A locale with language "no", country "NO", and variant "NY", representing Norwegian Nynorsk (Norway), is converted to a language tag "nn-NO".

**Note:** Although the language tag obtained by this method is well-formed (satisfies the syntax requirements defined by the IETF BCP 47 specification), it is not necessarily a valid BCP 47 language tag. For example, {@snippet lang=java : \* Locale.forLanguageTag("xx-YY").toLanguageTag(); \* } will return "xx-YY", but the language subtag "xx" and the region subtag "YY" are invalid because they are not registered in the IANA Language Subtag Registry.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a BCP47 language tag representing the locale |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#forLanguageTag(kotlin.String)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of this `Locale` object, consisting of language, country, variant, script, and extensions as below: language + "_" + country + "_" + (variant + "_#" | "#") + script + "_" + extensions Language is always lower case, country is always upper case, script is always title case, and extensions are always lower case. Extensions and private use subtags will be in canonical order as explained in `https://developer.android.com/reference/kotlin/java/util/Locale#toLanguageTag()`.

When the locale has neither script nor extensions, the result is the same as in Java 6 and prior.

If both the language and country fields are missing, this function will return the empty string, even if the variant, script, or extensions field is present (you can't have a locale with just a variant, the variant must accompany a well-formed language or country code).

If script or extensions are present and variant is missing, no underscore is added before the "#".

This behavior is designed to support debugging and to be compatible with previous uses of `toString` that expected language, country, and variant fields only. To represent a Locale as a String for interchange purposes, use `https://developer.android.com/reference/kotlin/java/util/Locale#toLanguageTag()`.

Examples:

- `en`
- `de_DE`
- `_GB`
- `en_US_WIN`
- `de__POSIX`
- `zh_CN_#Hans`
- `zh_TW_#Hant_x-java`
- `th_TH_TH_#u-nu-thai`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of the Locale, for debugging. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Locale#toLanguageTag()`

## Properties

### CANADA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANADA: Locale
```

Useful constant for country.

### CANADA_FRENCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANADA_FRENCH: Locale
```

Useful constant for country.

### CHINA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHINA: Locale
```

Useful constant for country.

### CHINESE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHINESE: Locale
```

Useful constant for language.

### ENGLISH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENGLISH: Locale
```

Useful constant for language.

### FRANCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRANCE: Locale
```

Useful constant for country.

### FRENCH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FRENCH: Locale
```

Useful constant for language.

### GERMAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GERMAN: Locale
```

Useful constant for language.

### GERMANY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GERMANY: Locale
```

Useful constant for country.

### ITALIAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ITALIAN: Locale
```

Useful constant for language.

### ITALY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ITALY: Locale
```

Useful constant for country.

### JAPAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JAPAN: Locale
```

Useful constant for country.

### JAPANESE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val JAPANESE: Locale
```

Useful constant for language.

### KOREA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KOREA: Locale
```

Useful constant for country.

### KOREAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KOREAN: Locale
```

Useful constant for language.

### PRC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PRC: Locale
```

Useful constant for country.

### ROOT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ROOT: Locale
```

Useful constant for the root locale. The root locale is the locale whose language, country, and variant are empty ("") strings. This is regarded as the base locale of all locales, and is used as the language/country neutral locale for the locale sensitive operations.

### SIMPLIFIED_CHINESE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIMPLIFIED_CHINESE: Locale
```

Useful constant for language.

### TAIWAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TAIWAN: Locale
```

Useful constant for country.

### TRADITIONAL_CHINESE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRADITIONAL_CHINESE: Locale
```

Useful constant for language.

### UK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UK: Locale
```

Useful constant for country.

### US

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val US: Locale
```

Useful constant for country.
