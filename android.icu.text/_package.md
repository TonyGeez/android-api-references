# android.icu.text

# android.icu.text

Kotlin| [Java](https://developer.android.com/reference/android/icu/text/package-summary "View this page in Java")

## Interfaces

| [ReorderCodes](https://developer.android.com/reference/kotlin/android/icu/text/Collator.ReorderCodes) | Reordering codes for non-script groups that can be reordered under collation. |
| [FormattedValue](https://developer.android.com/reference/kotlin/android/icu/text/FormattedValue) | An abstract formatted value: a string with associated field attributes. |
| [Replaceable](https://developer.android.com/reference/kotlin/android/icu/text/Replaceable) | `Replaceable`is an interface representing a string of characters that supports the replacement of a range of itself with a new string of characters. |
| [SymbolTable](https://developer.android.com/reference/kotlin/android/icu/text/SymbolTable) | An interface that defines both lookup protocol and parsing of symbolic names. |
| [UnicodeMatcher](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeMatcher) | `UnicodeMatcher`defines a protocol for objects that can match a range of characters in a Replaceable string. |

## Classes

| [AlphabeticIndex](https://developer.android.com/reference/kotlin/android/icu/text/AlphabeticIndex) | AlphabeticIndex supports the creation of a UI index appropriate for a given language. |
| [Bidi](https://developer.android.com/reference/kotlin/android/icu/text/Bidi) | <br /> ## Bidi algorithm for ICU This is an implementation of the Unicode Bidirectional Algorithm. <br /> |
| [BidiClassifier](https://developer.android.com/reference/kotlin/android/icu/text/BidiClassifier) | Overrides default Bidi class values with custom ones. |
| [BidiRun](https://developer.android.com/reference/kotlin/android/icu/text/BidiRun) | A BidiRun represents a sequence of characters at the same embedding level. |
| [BreakIterator](https://developer.android.com/reference/kotlin/android/icu/text/BreakIterator) | **\[icu enhancement\]** ICU's replacement for [java.text.BreakIterator](https://developer.android.com/reference/kotlin/java/text/BreakIterator.html#). |
| [CaseMap](https://developer.android.com/reference/kotlin/android/icu/text/CaseMap) | Low-level case mapping options and methods. |
| [CollationElementIterator](https://developer.android.com/reference/kotlin/android/icu/text/CollationElementIterator) | `CollationElementIterator`is an iterator created by a RuleBasedCollator to walk through a string. |
| [CollationKey](https://developer.android.com/reference/kotlin/android/icu/text/CollationKey) | A`CollationKey`represents a`String`under the rules of a specific`Collator`object. |
| [Collator](https://developer.android.com/reference/kotlin/android/icu/text/Collator) | **\[icu enhancement\]** ICU's replacement for [java.text.Collator](https://developer.android.com/reference/kotlin/java/text/Collator.html#). |
| [CompactDecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/CompactDecimalFormat) | Formats numbers in compact (abbreviated) notation, like "1. |
| [ConstrainedFieldPosition](https://developer.android.com/reference/kotlin/android/icu/text/ConstrainedFieldPosition) | Represents a span of a string containing a given field. |
| [CurrencyPluralInfo](https://developer.android.com/reference/kotlin/android/icu/text/CurrencyPluralInfo) | This class represents the information needed by DecimalFormat to format currency plural, such as "3. |
| [DateFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](https://developer.android.com/reference/kotlin/java/text/DateFormat.html#). |
| [DateFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DateFormatSymbols) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DateFormatSymbols.html#). |
| [DateIntervalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalFormat) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. |
| [DateIntervalInfo](https://developer.android.com/reference/kotlin/android/icu/text/DateIntervalInfo) | DateIntervalInfo is a public class for encapsulating localizable date time interval patterns. |
| [DateTimePatternGenerator](https://developer.android.com/reference/kotlin/android/icu/text/DateTimePatternGenerator) | This class provides flexible generation of date format patterns, like "yy-MM-dd". |
| [DecimalFormat](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](https://developer.android.com/reference/kotlin/java/text/DecimalFormat.html#). |
| [DecimalFormatSymbols](https://developer.android.com/reference/kotlin/android/icu/text/DecimalFormatSymbols) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormatSymbols](https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols.html#). |
| [DisplayOptions](https://developer.android.com/reference/kotlin/android/icu/text/DisplayOptions) | Represents all the display options that are supported by CLDR such as grammatical case, noun class, . |
| [Edits](https://developer.android.com/reference/kotlin/android/icu/text/Edits) | Records lengths of string edits but not replacement text. |
| [IDNA](https://developer.android.com/reference/kotlin/android/icu/text/IDNA) | Abstract base class for IDNA processing. |
| [ListFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ListFormatter) | Immutable class for formatting a list, using data from CLDR (or supplied separately). |
| [LocaleDisplayNames](https://developer.android.com/reference/kotlin/android/icu/text/LocaleDisplayNames) | Returns display names of ULocales and components of ULocales. |
| [MeasureFormat](https://developer.android.com/reference/kotlin/android/icu/text/MeasureFormat) | A formatter for Measure objects. |
| [MessageFormat](https://developer.android.com/reference/kotlin/android/icu/text/MessageFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](https://developer.android.com/reference/kotlin/java/text/MessageFormat.html#). |
| [MessagePattern](https://developer.android.com/reference/kotlin/android/icu/text/MessagePattern) | Parses and represents ICU MessageFormat patterns. |
| [Normalizer](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer) | Old Unicode normalization API. |
| [Normalizer2](https://developer.android.com/reference/kotlin/android/icu/text/Normalizer2) | Unicode normalization functionality for standard Unicode normalization or for using custom mapping tables. |
| [NumberFormat](https://developer.android.com/reference/kotlin/android/icu/text/NumberFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](https://developer.android.com/reference/kotlin/java/text/NumberFormat.html#). |
| [NumberingSystem](https://developer.android.com/reference/kotlin/android/icu/text/NumberingSystem) | `NumberingSystem`is the base class for all number systems. |
| [PluralFormat](https://developer.android.com/reference/kotlin/android/icu/text/PluralFormat) | `PluralFormat`supports the creation of internationalized messages with plural inflection. |
| [PluralRules](https://developer.android.com/reference/kotlin/android/icu/text/PluralRules) | Defines rules for mapping non-negative numeric values onto a small set of keywords. |
| [RelativeDateTimeFormatter](https://developer.android.com/reference/kotlin/android/icu/text/RelativeDateTimeFormatter) | Formats simple relative dates. |
| [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator) | RuleBasedCollator is a concrete subclass of Collator. |
| [ScientificNumberFormatter](https://developer.android.com/reference/kotlin/android/icu/text/ScientificNumberFormatter) | A formatter that formats numbers in user-friendly scientific notation. |
| [SearchIterator](https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator) | SearchIterator is an abstract base class that provides methods to search for a pattern within a text string. |
| [SelectFormat](https://developer.android.com/reference/kotlin/android/icu/text/SelectFormat) | `SelectFormat`supports the creation of internationalized messages by selecting phrases based on keywords. |
| [SimpleDateFormat](https://developer.android.com/reference/kotlin/android/icu/text/SimpleDateFormat) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](https://developer.android.com/reference/kotlin/java/text/SimpleDateFormat.html#). |
| [StringSearch](https://developer.android.com/reference/kotlin/android/icu/text/StringSearch) | StringSearch is a [SearchIterator](https://developer.android.com/reference/kotlin/android/icu/text/SearchIterator) that provides language-sensitive text searching based on the comparison rules defined in a [RuleBasedCollator](https://developer.android.com/reference/kotlin/android/icu/text/RuleBasedCollator) object. |
| [TimeZoneFormat](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneFormat) | `TimeZoneFormat`supports time zone display name formatting and parsing. |
| [TimeZoneNames](https://developer.android.com/reference/kotlin/android/icu/text/TimeZoneNames) | `TimeZoneNames`is an abstract class representing the time zone display name data model defined by [UTS#35 Unicode Locale Data Markup Language (LDML)](http://www.unicode.org/reports/tr35/). |
| [Transliterator](https://developer.android.com/reference/kotlin/android/icu/text/Transliterator) | `Transliterator`is an abstract class that transliterates text from one format to another. |
| [UCharacterIterator](https://developer.android.com/reference/kotlin/android/icu/text/UCharacterIterator) | Abstract class that defines an API for iteration on text objects. |
| [UFormat](https://developer.android.com/reference/kotlin/android/icu/text/UFormat) | An abstract class that extends [java.text.Format](https://developer.android.com/reference/kotlin/java/text/Format.html#) to provide additional ICU protocol, specifically, the getLocale() API. |
| [UnicodeFilter](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeFilter) | `UnicodeFilter`defines a protocol for selecting a subset of the full range (U+0000 to U+FFFF) of Unicode characters. |
| [UnicodeSet](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet) | A mutable set of Unicode characters and multicharacter strings. |
| [UnicodeSetIterator](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetIterator) | UnicodeSetIterator iterates over the contents of a UnicodeSet. |
| [UnicodeSetSpanner](https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSetSpanner) | A helper class used to count, replace, and trim CharSequences based on UnicodeSet matches. |

## Exceptions

| [StringPrepParseException](https://developer.android.com/reference/kotlin/android/icu/text/StringPrepParseException) | Exception that signals an error has occurred while parsing the input to StringPrep or IDNA. |

## Enums

| [DisplayContext](https://developer.android.com/reference/kotlin/android/icu/text/DisplayContext) | Display context settings. |
