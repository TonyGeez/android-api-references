# android.icu.text

# android.icu.text

Kotlin| [Java](../android/icu/text/_package.md)
| --- | --- |

## Interfaces

| [ReorderCodes](../android/icu/text/Collator.ReorderCodes.md) | Reordering codes for non-script groups that can be reordered under collation. |
| --- | --- |
| [FormattedValue](../android/icu/text/FormattedValue.md) | An abstract formatted value: a string with associated field attributes. |
| [Replaceable](../android/icu/text/Replaceable.md) | `Replaceable`is an interface representing a string of characters that supports the replacement of a range of itself with a new string of characters. |
| [SymbolTable](../android/icu/text/SymbolTable.md) | An interface that defines both lookup protocol and parsing of symbolic names. |
| --- | --- |
| [UnicodeMatcher](../android/icu/text/UnicodeMatcher.md) | `UnicodeMatcher`defines a protocol for objects that can match a range of characters in a Replaceable string. |

## Classes

| [AlphabeticIndex](../android/icu/text/AlphabeticIndex.md) | AlphabeticIndex supports the creation of a UI index appropriate for a given language. |
| --- | --- |
| [Bidi](../android/icu/text/Bidi.md) | <br /> ## Bidi algorithm for ICU This is an implementation of the Unicode Bidirectional Algorithm. <br /> |
| [BidiClassifier](../android/icu/text/BidiClassifier.md) | Overrides default Bidi class values with custom ones. |
| [BidiRun](../android/icu/text/BidiRun.md) | A BidiRun represents a sequence of characters at the same embedding level. |
| --- | --- |
| [BreakIterator](../android/icu/text/BreakIterator.md) | **\[icu enhancement\]** ICU's replacement for [java.text.BreakIterator](../java/text/BreakIterator.md). |
| [CaseMap](../android/icu/text/CaseMap.md) | Low-level case mapping options and methods. |
| [CollationElementIterator](../android/icu/text/CollationElementIterator.md) | `CollationElementIterator`is an iterator created by a RuleBasedCollator to walk through a string. |
| --- | --- |
| [CollationKey](../android/icu/text/CollationKey.md) | A`CollationKey`represents a`String`under the rules of a specific`Collator`object. |
| [Collator](../android/icu/text/Collator.md) | **\[icu enhancement\]** ICU's replacement for [java.text.Collator](../java/text/Collator.md). |
| [CompactDecimalFormat](../android/icu/text/CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. |
| --- | --- |
| [ConstrainedFieldPosition](../android/icu/text/ConstrainedFieldPosition.md) | Represents a span of a string containing a given field. |
| [CurrencyPluralInfo](../android/icu/text/CurrencyPluralInfo.md) | This class represents the information needed by DecimalFormat to format currency plural, such as "3. |
| [DateFormat](../android/icu/text/DateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](../java/text/DateFormat.md). |
| --- | --- |
| [DateFormatSymbols](../android/icu/text/DateFormatSymbols.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormatSymbols](../java/text/DateFormatSymbols.md). |
| [DateIntervalFormat](../android/icu/text/DateIntervalFormat.md) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. |
| [DateIntervalInfo](../android/icu/text/DateIntervalInfo.md) | DateIntervalInfo is a public class for encapsulating localizable date time interval patterns. |
| --- | --- |
| [DateTimePatternGenerator](../android/icu/text/DateTimePatternGenerator.md) | This class provides flexible generation of date format patterns, like "yy-MM-dd". |
| [DecimalFormat](../android/icu/text/DecimalFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](../java/text/DecimalFormat.md). |
| [DecimalFormatSymbols](../android/icu/text/DecimalFormatSymbols.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormatSymbols](../java/text/DecimalFormatSymbols.md). |
| --- | --- |
| [DisplayOptions](../android/icu/text/DisplayOptions.md) | Represents all the display options that are supported by CLDR such as grammatical case, noun class, . |
| [Edits](../android/icu/text/Edits.md) | Records lengths of string edits but not replacement text. |
| [IDNA](../android/icu/text/IDNA.md) | Abstract base class for IDNA processing. |
| --- | --- |
| [ListFormatter](../android/icu/text/ListFormatter.md) | Immutable class for formatting a list, using data from CLDR (or supplied separately). |
| [LocaleDisplayNames](../android/icu/text/LocaleDisplayNames.md) | Returns display names of ULocales and components of ULocales. |
| [MeasureFormat](../android/icu/text/MeasureFormat.md) | A formatter for Measure objects. |
| --- | --- |
| [MessageFormat](../android/icu/text/MessageFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](../java/text/MessageFormat.md). |
| [MessagePattern](../android/icu/text/MessagePattern.md) | Parses and represents ICU MessageFormat patterns. |
| [Normalizer](../android/icu/text/Normalizer.md) | Old Unicode normalization API. |
| --- | --- |
| [Normalizer2](../android/icu/text/Normalizer2.md) | Unicode normalization functionality for standard Unicode normalization or for using custom mapping tables. |
| [NumberFormat](../android/icu/text/NumberFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](../java/text/NumberFormat.md). |
| [NumberingSystem](../android/icu/text/NumberingSystem.md) | `NumberingSystem`is the base class for all number systems. |
| --- | --- |
| [PluralFormat](../android/icu/text/PluralFormat.md) | `PluralFormat`supports the creation of internationalized messages with plural inflection. |
| [PluralRules](../android/icu/text/PluralRules.md) | Defines rules for mapping non-negative numeric values onto a small set of keywords. |
| [RelativeDateTimeFormatter](../android/icu/text/RelativeDateTimeFormatter.md) | Formats simple relative dates. |
| --- | --- |
| [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) | RuleBasedCollator is a concrete subclass of Collator. |
| [ScientificNumberFormatter](../android/icu/text/ScientificNumberFormatter.md) | A formatter that formats numbers in user-friendly scientific notation. |
| [SearchIterator](../android/icu/text/SearchIterator.md) | SearchIterator is an abstract base class that provides methods to search for a pattern within a text string. |
| --- | --- |
| [SelectFormat](../android/icu/text/SelectFormat.md) | `SelectFormat`supports the creation of internationalized messages by selecting phrases based on keywords. |
| [SimpleDateFormat](../android/icu/text/SimpleDateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](../java/text/SimpleDateFormat.md). |
| [StringSearch](../android/icu/text/StringSearch.md) | StringSearch is a [SearchIterator](../android/icu/text/SearchIterator.md) that provides language-sensitive text searching based on the comparison rules defined in a [RuleBasedCollator](../android/icu/text/RuleBasedCollator.md) object. |
| --- | --- |
| [TimeZoneFormat](../android/icu/text/TimeZoneFormat.md) | `TimeZoneFormat`supports time zone display name formatting and parsing. |
| [TimeZoneNames](../android/icu/text/TimeZoneNames.md) | `TimeZoneNames`is an abstract class representing the time zone display name data model defined by [UTS#35 Unicode Locale Data Markup Language (LDML)](http://www.unicode.org/reports/tr35/). |
| [Transliterator](../android/icu/text/Transliterator.md) | `Transliterator`is an abstract class that transliterates text from one format to another. |
| --- | --- |
| [UCharacterIterator](../android/icu/text/UCharacterIterator.md) | Abstract class that defines an API for iteration on text objects. |
| [UFormat](../android/icu/text/UFormat.md) | An abstract class that extends [java.text.Format](../java/text/Format.md) to provide additional ICU protocol, specifically, the getLocale() API. |
| [UnicodeFilter](../android/icu/text/UnicodeFilter.md) | `UnicodeFilter`defines a protocol for selecting a subset of the full range (U+0000 to U+FFFF) of Unicode characters. |
| --- | --- |
| [UnicodeSet](../android/icu/text/UnicodeSet.md) | A mutable set of Unicode characters and multicharacter strings. |
| [UnicodeSetIterator](../android/icu/text/UnicodeSetIterator.md) | UnicodeSetIterator iterates over the contents of a UnicodeSet. |
| [UnicodeSetSpanner](../android/icu/text/UnicodeSetSpanner.md) | A helper class used to count, replace, and trim CharSequences based on UnicodeSet matches. |
| --- | --- |

## Exceptions

| [StringPrepParseException](../android/icu/text/StringPrepParseException.md) | Exception that signals an error has occurred while parsing the input to StringPrep or IDNA. |
| --- | --- |

## Enums

| [DisplayContext](../android/icu/text/DisplayContext.md) | Display context settings. |
| --- | --- |
