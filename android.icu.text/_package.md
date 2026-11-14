# android.icu.text

# android.icu.text

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [ReorderCodes](../android/icu/text/Collator.ReorderCodes.md) | Reordering codes for non-script groups that can be reordered under collation. |
| --- | --- |
| [FormattedValue](FormattedValue.md) | An abstract formatted value: a string with associated field attributes. |
| [Replaceable](Replaceable.md) | `Replaceable`is an interface representing a string of characters that supports the replacement of a range of itself with a new string of characters. |
| [SymbolTable](SymbolTable.md) | An interface that defines both lookup protocol and parsing of symbolic names. |
| --- | --- |
| [UnicodeMatcher](UnicodeMatcher.md) | `UnicodeMatcher`defines a protocol for objects that can match a range of characters in a Replaceable string. |

## Classes

| [AlphabeticIndex](AlphabeticIndex.md) | AlphabeticIndex supports the creation of a UI index appropriate for a given language. |
| --- | --- |
| [Bidi](Bidi.md) | <br /> ## Bidi algorithm for ICU This is an implementation of the Unicode Bidirectional Algorithm. <br /> |
| [BidiClassifier](BidiClassifier.md) | Overrides default Bidi class values with custom ones. |
| [BidiRun](BidiRun.md) | A BidiRun represents a sequence of characters at the same embedding level. |
| --- | --- |
| [BreakIterator](BreakIterator.md) | **\[icu enhancement\]** ICU's replacement for [java.text.BreakIterator](../java.text/BreakIterator.md). |
| [CaseMap](CaseMap.md) | Low-level case mapping options and methods. |
| [CollationElementIterator](CollationElementIterator.md) | `CollationElementIterator`is an iterator created by a RuleBasedCollator to walk through a string. |
| --- | --- |
| [CollationKey](CollationKey.md) | A`CollationKey`represents a`String`under the rules of a specific`Collator`object. |
| [Collator](Collator.md) | **\[icu enhancement\]** ICU's replacement for [java.text.Collator](../java.text/Collator.md). |
| [CompactDecimalFormat](CompactDecimalFormat.md) | Formats numbers in compact (abbreviated) notation, like "1. |
| --- | --- |
| [ConstrainedFieldPosition](ConstrainedFieldPosition.md) | Represents a span of a string containing a given field. |
| [CurrencyPluralInfo](CurrencyPluralInfo.md) | This class represents the information needed by DecimalFormat to format currency plural, such as "3. |
| [DateFormat](DateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormat](../java.text/DateFormat.md). |
| --- | --- |
| [DateFormatSymbols](DateFormatSymbols.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DateFormatSymbols](../java.text/DateFormatSymbols.md). |
| [DateIntervalFormat](DateIntervalFormat.md) | DateIntervalFormat is a class for formatting and parsing date intervals in a language-independent manner. |
| [DateIntervalInfo](DateIntervalInfo.md) | DateIntervalInfo is a public class for encapsulating localizable date time interval patterns. |
| --- | --- |
| [DateTimePatternGenerator](DateTimePatternGenerator.md) | This class provides flexible generation of date format patterns, like "yy-MM-dd". |
| [DecimalFormat](DecimalFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormat](../java.text/DecimalFormat.md). |
| [DecimalFormatSymbols](DecimalFormatSymbols.md) | **\[icu enhancement\]** ICU's replacement for [java.text.DecimalFormatSymbols](../java.text/DecimalFormatSymbols.md). |
| --- | --- |
| [DisplayOptions](DisplayOptions.md) | Represents all the display options that are supported by CLDR such as grammatical case, noun class, . |
| [Edits](Edits.md) | Records lengths of string edits but not replacement text. |
| [IDNA](IDNA.md) | Abstract base class for IDNA processing. |
| --- | --- |
| [ListFormatter](ListFormatter.md) | Immutable class for formatting a list, using data from CLDR (or supplied separately). |
| [LocaleDisplayNames](LocaleDisplayNames.md) | Returns display names of ULocales and components of ULocales. |
| [MeasureFormat](MeasureFormat.md) | A formatter for Measure objects. |
| --- | --- |
| [MessageFormat](MessageFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.MessageFormat](../java.text/MessageFormat.md). |
| [MessagePattern](MessagePattern.md) | Parses and represents ICU MessageFormat patterns. |
| [Normalizer](Normalizer.md) | Old Unicode normalization API. |
| --- | --- |
| [Normalizer2](Normalizer2.md) | Unicode normalization functionality for standard Unicode normalization or for using custom mapping tables. |
| [NumberFormat](NumberFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.NumberFormat](../java.text/NumberFormat.md). |
| [NumberingSystem](NumberingSystem.md) | `NumberingSystem`is the base class for all number systems. |
| --- | --- |
| [PluralFormat](PluralFormat.md) | `PluralFormat`supports the creation of internationalized messages with plural inflection. |
| [PluralRules](PluralRules.md) | Defines rules for mapping non-negative numeric values onto a small set of keywords. |
| [RelativeDateTimeFormatter](RelativeDateTimeFormatter.md) | Formats simple relative dates. |
| --- | --- |
| [RuleBasedCollator](RuleBasedCollator.md) | RuleBasedCollator is a concrete subclass of Collator. |
| [ScientificNumberFormatter](ScientificNumberFormatter.md) | A formatter that formats numbers in user-friendly scientific notation. |
| [SearchIterator](SearchIterator.md) | SearchIterator is an abstract base class that provides methods to search for a pattern within a text string. |
| --- | --- |
| [SelectFormat](SelectFormat.md) | `SelectFormat`supports the creation of internationalized messages by selecting phrases based on keywords. |
| [SimpleDateFormat](SimpleDateFormat.md) | **\[icu enhancement\]** ICU's replacement for [java.text.SimpleDateFormat](../java.text/SimpleDateFormat.md). |
| [StringSearch](StringSearch.md) | StringSearch is a [SearchIterator](SearchIterator.md) that provides language-sensitive text searching based on the comparison rules defined in a [RuleBasedCollator](RuleBasedCollator.md) object. |
| --- | --- |
| [TimeZoneFormat](TimeZoneFormat.md) | `TimeZoneFormat`supports time zone display name formatting and parsing. |
| [TimeZoneNames](TimeZoneNames.md) | `TimeZoneNames`is an abstract class representing the time zone display name data model defined by [UTS#35 Unicode Locale Data Markup Language (LDML)](http://www.unicode.org/reports/tr35/). |
| [Transliterator](Transliterator.md) | `Transliterator`is an abstract class that transliterates text from one format to another. |
| --- | --- |
| [UCharacterIterator](UCharacterIterator.md) | Abstract class that defines an API for iteration on text objects. |
| [UFormat](UFormat.md) | An abstract class that extends [java.text.Format](../java.text/Format.md) to provide additional ICU protocol, specifically, the getLocale() API. |
| [UnicodeFilter](UnicodeFilter.md) | `UnicodeFilter`defines a protocol for selecting a subset of the full range (U+0000 to U+FFFF) of Unicode characters. |
| --- | --- |
| [UnicodeSet](UnicodeSet.md) | A mutable set of Unicode characters and multicharacter strings. |
| [UnicodeSetIterator](UnicodeSetIterator.md) | UnicodeSetIterator iterates over the contents of a UnicodeSet. |
| [UnicodeSetSpanner](UnicodeSetSpanner.md) | A helper class used to count, replace, and trim CharSequences based on UnicodeSet matches. |
| --- | --- |

## Exceptions

| [StringPrepParseException](StringPrepParseException.md) | Exception that signals an error has occurred while parsing the input to StringPrep or IDNA. |
| --- | --- |

## Enums

| [DisplayContext](DisplayContext.md) | Display context settings. |
| --- | --- |
