Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Transliterator

```
abstract class Transliterator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.icu.text.Transliterator](../android/icu/text/Transliterator.md) |

`Transliterator` is an abstract class that transliterates text from one format to another. The most common kind of transliterator is a script, or alphabet, transliterator. For example, a Russian to Latin transliterator changes Russian text written in Cyrillic characters to phonetically equivalent Latin characters. It does not *translate* Russian to English! Transliteration, unlike translation, operates on characters, without reference to the meanings of words and sentences.

Although script conversion is its most common use, a transliterator can actually perform a more general class of tasks. In fact, `Transliterator` defines a very general API which specifies only that a segment of the input text is replaced by new text. The particulars of this conversion are determined entirely by subclasses of `Transliterator`.

**Transliterators are stateless**

`Transliterator` objects are *stateless* ; they retain no information between calls to `transliterate()`. As a result, threads may share transliterators without synchronizing them. This might seem to limit the complexity of the transliteration operation. In practice, subclasses perform complex transliterations by delaying the replacement of text until it is known that no other replacements are possible. In other words, although the `Transliterator` objects are stateless, the source text itself embodies all the needed information, and delayed operation allows arbitrary complexity.

**Batch transliteration**

The simplest way to perform transliteration is all at once, on a string of existing text. This is referred to as *batch* transliteration. For example, given a string `input` and a transliterator `t`, the call
`String result = t.transliterate(input); ` will transliterate it and return the result. Other methods allow the client to specify a substring to be transliterated and to use `https://developer.android.com/reference/kotlin/android/icu/text/Replaceable` objects instead of strings, in order to preserve out-of-band information (such as text styles).

**Keyboard transliteration**

Somewhat more involved is *keyboard*, or incremental transliteration. This is the transliteration of text that is arriving from some source (typically the user's keyboard) one character at a time, or in some other piecemeal fashion.

In keyboard transliteration, a `Replaceable` buffer stores the text. As text is inserted, as much as possible is transliterated on the fly. This means a GUI that displays the contents of the buffer may show text being modified as each new character arrives.

Consider the simple rule-based Transliterator:
` th>{theta}
t>{tau} ` When the user types 't', nothing will happen, since the transliterator is waiting to see if the next character is 'h'. To remedy this, we introduce the notion of a cursor, marked by a '|' in the output string: ` t>|{tau}
| --- | --- | --- |
{tau}h>{theta} ` Now when the user types 't', tau appears, and if the next character is 'h', the tau changes to a theta. This is accomplished by maintaining a cursor position (independent of the insertion point, and invisible in the GUI) across calls to `transliterate()`. Typically, the cursor will be coincident with the insertion point, but in a case like the one above, it will precede the insertion point.

Keyboard transliteration methods maintain a set of three indices that are updated with each call to `transliterate()`, including the cursor, start, and limit. These indices are changed by the method, and they are passed in and out via a Position object. The `start` index marks the beginning of the substring that the transliterator will look at. It is advanced as text becomes committed (but it is not the committed index; that's the `cursor`). The `cursor` index, described above, marks the point at which the transliterator last stopped, either because it reached the end, or because it required more characters to disambiguate between possible inputs. The `cursor` can also be explicitly set by rules. Any characters before the `cursor` index are frozen; future keyboard transliteration calls within this input sequence will not change them. New text is inserted at the `limit` index, which marks the end of the substring that the transliterator looks at.

Because keyboard transliteration assumes that more characters are to arrive, it is conservative in its operation. It only transliterates when it can do so unambiguously. Otherwise it waits for more characters to arrive. When the client code knows that no more characters are forthcoming, perhaps because the user has performed some input termination operation, then it should call `finishTransliteration()` to complete any pending transliterations.

**Inverses**

Pairs of transliterators may be inverses of one another. For example, if transliterator **A** transliterates characters by incrementing their Unicode value (so "abc" -\> "def"), and transliterator **B** decrements character values, then **A** is an inverse of **B** and vice versa. If we compose **A** with **B** in a compound transliterator, the result is the identity transliterator, that is, a transliterator that does not change its input text. The `Transliterator` method `getInverse()` returns a transliterator's inverse, if one exists, or `null` otherwise. However, the result of `getInverse()` usually will *not* be a true mathematical inverse. This is because true inverse transliterators are difficult to formulate. For example, consider two transliterators: **AB** , which transliterates the character 'A' to 'B', and **BA**, which transliterates 'B' to 'A'. It might seem that these are exact inverses, since
"A" x **AB** -\> "B" 
"B" x **BA** -\> "A" where 'x' represents transliteration. However, "ABCD" x **AB** -\> "BBCD" 
"BBCD" x **BA** -\> "AACD" so **AB** composed with **BA** is not the identity. Nonetheless, **BA** may be usefully considered to be **AB** 's inverse, and it is on this basis that **AB** `.getInverse()` could legitimately return **BA** .

**Filtering**

Each transliterator has a filter, which restricts changes to those characters selected by the filter. The filter affects just the characters that are changed -- the characters outside of the filter are still part of the context for the filter. For example, in the following even though 'x' is filtered out, and doesn't convert to y, it does affect the conversion of 'a'.

```kotlin
String rules = "x > y; x{a} > b; ";
  Transliterator tempTrans = Transliterator.createFromRules("temp", rules, Transliterator.FORWARD);
  tempTrans.setFilter(new UnicodeSet("[a]"));
  String tempResult = tempTrans.transform("xa");
  // results in "xb"
 
```

**IDs and display names**

A transliterator is designated by a short identifier string or *ID* . IDs follow the format *source-destination* , where *source* describes the entity being replaced, and *destination* describes the entity replacing *source*. The entities may be the names of scripts, particular sequences of characters, or whatever else it is that the transliterator converts to or from. For example, a transliterator from Russian to Latin might be named "Russian-Latin". A transliterator from keyboard escape sequences to Latin-1 characters might be named "KeyboardEscape-Latin1". By convention, system entity names are in English, with the initial letters of words capitalized; user entity names may follow any format so long as they do not contain dashes.

In addition to programmatic IDs, transliterator objects have display names for presentation in user interfaces, returned by #getDisplayName.

**Composed transliterators**

In addition to built-in system transliterators like "Latin-Greek", there are also built-in *composed* transliterators. These are implemented by composing two or more component transliterators. For example, if we have scripts "A", "B", "C", and "D", and we want to transliterate between all pairs of them, then we need to write 12 transliterators: "A-B", "A-C", "A-D", "B-A",..., "D-A", "D-B", "D-C". If it is possible to convert all scripts to an intermediate script "M", then instead of writing 12 rule sets, we only need to write 8: "A\~M", "B\~M", "C\~M", "D\~M", "M\~A", "M\~B", "M\~C", "M\~D". (This might not seem like a big win, but it's really 2*n* vs. *n* 2 - *n* , so as *n* gets larger the gain becomes significant. With 9 scripts, it's 18 vs. 72 rule sets, a big difference.) Note the use of "\~" rather than "-" for the script separator here; this indicates that the given transliterator is intended to be composed with others, rather than be used as is.

Composed transliterators can be instantiated as usual. For example, the system transliterator "Devanagari-Gujarati" is a composed transliterator built internally as "Devanagari\~InterIndic;InterIndic\~Gujarati". When this transliterator is instantiated, it appears externally to be a standard transliterator (e.g., getID() returns "Devanagari-Gujarati").

**Rule syntax**

A set of rules determines how to perform translations. Rules within a rule set are separated by semicolons (';'). To include a literal semicolon, prefix it with a backslash ('\\'). Unicode Pattern_White_Space is ignored. If the first non-blank character on a line is '#', the entire line is ignored as a comment.

Each set of rules consists of two groups, one forward, and one reverse. This is a convention that is not enforced; rules for one direction may be omitted, with the result that translations in that direction will not modify the source text. In addition, bidirectional forward-reverse rules may be specified for symmetrical transformations.

Note: Another description of the Transliterator rule syntax is available in [section Transform Rules Syntax of UTS #35: Unicode LDML](https://www.unicode.org/reports/tr35/tr35-general.html#Transform_Rules_Syntax). The rules are shown there using arrow symbols ← and → and ↔. ICU supports both those and the equivalent ASCII symbols \< and \> and \<\>.

Rule statements take one of the following forms:

`$alefmadda=\\u0622;`
: **Variable definition.** The name on the left is assigned the text on the right. In this example, after this statement, instances of the left hand name, "`$alefmadda`", will be replaced by the Unicode character U+0622. Variable names must begin with a letter and consist only of letters, digits, and underscores. Case is significant. Duplicate names cause an exception to be thrown, that is, variables cannot be redefined. The right hand side may contain well-formed text of any length, including no text at all ("`$empty=;`"). The right hand side may contain embedded `UnicodeSet` patterns, for example, "`$softvowel=[eiyEIY]`".

`ai>$alefmadda;`
: **Forward translation rule.** This rule states that the string on the left will be changed to the string on the right when performing forward transliteration.

`ai<$alefmadda;`
: **Reverse translation rule.** This rule states that the string on the right will be changed to the string on the left when performing reverse transliteration.

`ai<>$alefmadda;`
: **Bidirectional translation rule.** This rule states that the string on the right will be changed to the string on the left when performing forward transliteration, and vice versa when performing reverse transliteration.

Translation rules consist of a *match pattern* and an *output string* . The match pattern consists of literal characters, optionally preceded by context, and optionally followed by context. Context characters, like literal pattern characters, must be matched in the text being transliterated. However, unlike literal pattern characters, they are not replaced by the output text. For example, the pattern "`abc{def}`" indicates the characters "`def`" must be preceded by "`abc`" for a successful match. If there is a successful match, "`def`" will be replaced, but not "`abc`". The final '`}`' is optional, so "`abc{def`" is equivalent to "`abc{def}`". Another example is "`{123}456`" (or "`123}456`") in which the literal pattern "`123`" must be followed by "`456`".

The output string of a forward or reverse rule consists of characters to replace the literal pattern characters. If the output string contains the character '`|`', this is taken to indicate the location of the *cursor* after replacement. The cursor is the point in the text at which the next replacement, if any, will be applied. The cursor is usually placed within the replacement text; however, it can actually be placed into the precending or following context by using the special character '@'. Examples:
| --- | --- |

```kotlin
a {foo} z > | @ bar; # foo -> bar, move cursor before a
      {foo} xyz > bar @@|; # foo -> bar, cursor between y and z
  
```

**UnicodeSet**

`UnicodeSet` patterns may appear anywhere that makes sense. They may appear in variable definitions. Contrariwise, `UnicodeSet` patterns may themselves contain variable references, such as "`$a=[a-z];$not_a=[^$a]`", or "`$range=a-z;$ll=[$range]`".

`UnicodeSet` patterns may also be embedded directly into rule strings. Thus, the following two rules are equivalent:

```kotlin
$vowel=[aeiou]; $vowel>'*'; # One way to do this
      [aeiou]>'*'; # Another way
  
```

See `https://developer.android.com/reference/kotlin/android/icu/text/UnicodeSet` for more documentation and examples.

**Segments**

Segments of the input string can be matched and copied to the output string. This makes certain sets of rules simpler and more general, and makes reordering possible. For example:

```kotlin
([a-z]) > $1 $1; # double lowercase letters
      ([:Lu:]) ([:Ll:]) > $2 $1; # reverse order of Lu-Ll pairs
  
```

The segment of the input string to be copied is delimited by "`(`" and "`)`". Up to nine segments may be defined. Segments may not overlap. In the output string, "`$1`" through "`$9`" represent the input string segments, in left-to-right order of definition.

**Anchors**

Patterns can be anchored to the beginning or the end of the text. This is done with the special characters '`^`' and '`$`'. For example:

```kotlin
^ a   > 'BEG_A';   # match 'a' at start of text
      a   > 'A'; # match other instances of 'a'
      z $ > 'END_Z';   # match 'z' at end of text
      z   > 'Z';       # match other instances of 'z'
  
```

It is also possible to match the beginning or the end of the text using a `UnicodeSet`. This is done by including a virtual anchor character '`$`' at the end of the set pattern. Although this is usually the match character for the end anchor, the set will match either the beginning or the end of the text, depending on its placement. For example:

```kotlin
$x = [a-z$];   # match 'a' through 'z' OR anchor
    $x 1    > 2;   # match '1' after a-z or at the start
       3 $x > 4;   # match '3' before a-z or at the end
  
```

**Example**

The following example rules illustrate many of the features of the rule language.

| Rule 1. | `abc{def}>x|y` |
| --- | --- | --- |
| Rule 2. | `xyz>r` |
| Rule 3. | `yz>q` |

Applying these rules to the string "`adefabcdefz`" yields the following results:

| `|adefabcdefz` | Initial state, no rules match. Advance cursor. |
| --- | --- | --- |
| `a|defabcdefz` | Still no match. Rule 1 does not match because the preceding context is not present. |
| `ad|efabcdefz` | Still no match. Keep advancing until there is a match... |
| `ade|fabcdefz` | ... |
| --- | --- | --- |
| `adef|abcdefz` | ... |
| `adefa|bcdefz` | ... |
| `adefab|cdefz` | ... |
| --- | --- | --- |
| `adefabc|defz` | Rule 1 matches; replace "`def`" with "`xy`" and back up the cursor to before the '`y`'. |
| `adefabcx|yz` | Although "`xyz`" is present, rule 2 does not match because the cursor is before the '`y`', not before the '`x`'. Rule 3 does match. Replace "`yz`" with "`q`". |
| `adefabcxq|` | The cursor is at the end; transliteration is complete. |
| --- | --- | --- |

The order of rules is significant. If multiple rules may match at some point, the first matching rule is applied.

Forward and reverse rules may have an empty output string. Otherwise, an empty left or right hand side of any statement is a syntax error.

Single quotes are used to quote any character other than a digit or letter. To specify a single quote itself, inside or outside of quotes, use two single quotes in a row. For example, the rule "`'>'>o''clock`" changes the string "`>`" to the string "`o'clock`".

**Notes**

While a Transliterator is being built from rules, it checks that the rules are added in proper order. For example, if the rule "a\>x" is followed by the rule "ab\>y", then the second rule will throw an exception. The reason is that the second rule can never be triggered, since the first rule always matches anything it matches. In other words, the first rule *masks* the second rule.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position` Position structure for incremental transliteration. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#FORWARD:kotlin.Int` Direction constant indicating the forward direction in a transliterator, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#REVERSE:kotlin.Int` Direction constant indicating the reverse direction in a transliterator, e. |

| Public methods ||
|---|---|
| static [Transliterator](../android/icu/text/Transliterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#createFromRules(kotlin.String,%20kotlin.String,%20kotlin.Int)(ID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, rules: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a `Transliterator` object constructed from the given rule string. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#filteredTransliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.Boolean)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, index: https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position!, incremental: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Transliterate a substring of text, as specified by index, taking filters into account. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#finishTransliteration(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, index: https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position!)` Finishes any pending transliterations that were waiting for more characters. |
| --- | --- |
| static [Enumeration](../java/util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableIDs()()` Returns an enumeration over the programmatic names of registered `Transliterator` objects. |
| static [Enumeration](../java/util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableSources()()` Returns an enumeration over the source names of registered transliterators. |
| static [Enumeration](../java/util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableTargets(kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns an enumeration over the target names of registered transliterators having a given source name. |
| --- | --- |
| static [Enumeration](../java/util/Enumeration.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableVariants(kotlin.String,%20kotlin.String)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns an enumeration over the variant names of registered transliterators having a given source name and target name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getDisplayName(kotlin.String)(ID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a name for this transliterator that is appropriate for display to the user in the default `DISPLAY` locale. |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getDisplayName(kotlin.String,%20android.icu.util.ULocale)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, inLocale: https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#!)` Returns a name for this transliterator that is appropriate for display to the user in the given locale. |
| --- | --- |
| open static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getDisplayName(kotlin.String,%20java.util.Locale)(id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, inLocale: https://developer.android.com/reference/kotlin/java/util/Locale.html#!)` Returns a name for this transliterator that is appropriate for display to the user in the given locale. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Transliterator](../android/icu/text/Transliterator.md)!\>! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getElements()()` Return the elements that make up this transliterator. |
| [UnicodeFilter](../android/icu/text/UnicodeFilter.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getFilter()()` Returns the filter used by this transliterator, or `null` if this transliterator uses no filter. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getID()()` Returns a programmatic identifier for this transliterator. |
| static [Transliterator](../android/icu/text/Transliterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getInstance(kotlin.String)(ID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns a `Transliterator` object given its ID. |
| open static [Transliterator](../android/icu/text/Transliterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getInstance(kotlin.String,%20kotlin.Int)(ID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a `Transliterator` object given its ID. |
| --- | --- |
| [Transliterator](../android/icu/text/Transliterator.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getInverse()()` Returns this transliterator's inverse. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getMaximumContextLength()()` Returns the length of the longest context required by this transliterator. |
| [UnicodeSet](../android/icu/text/UnicodeSet.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getSourceSet()()` Returns the set of all characters that may be modified in the input text by this Transliterator. |
| --- | --- |
| open [UnicodeSet](../android/icu/text/UnicodeSet.md)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getTargetSet()()` Returns the set of all characters that may be generated as replacement text by this transliterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#setFilter(android.icu.text.UnicodeFilter)(filter: https://developer.android.com/reference/kotlin/android/icu/text/UnicodeFilter!)` Changes the filter used by this transliterator. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#toRules(kotlin.Boolean)(escapeUnprintable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns a rule string for this transliterator. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!)` Transliterates an entire string in place. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, index: https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position!)` Transliterates the portion of the text buffer that can be transliterated unambiguosly. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.Int)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, index: https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position!, insertion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Transliterates the portion of the text buffer that can be transliterated unambiguosly after a new character has been inserted, typically as a result of a keyboard event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.String)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, index: https://developer.android.com/reference/kotlin/android/icu/text/Transliterator.Position!, insertion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Transliterates the portion of the text buffer that can be transliterated unambiguosly after new text has been inserted, typically as a result of a keyboard event. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20kotlin.Int,%20kotlin.Int)(text: https://developer.android.com/reference/kotlin/android/icu/text/Replaceable!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Transliterates a segment of a string, with optional filtering. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(kotlin.String)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Transliterate an entire string and returns the result. |
| --- | --- |

## Constants

### FORWARD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FORWARD: Int
```

Direction constant indicating the forward direction in a transliterator, e.g., the forward rules of a rule-based Transliterator. An "A-B" transliterator transliterates A to B when operating in the forward direction, and B to A when operating in the reverse direction.

 Value: 0

### REVERSE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REVERSE: Int
```

Direction constant indicating the reverse direction in a transliterator, e.g., the reverse rules of a rule-based Transliterator. An "A-B" transliterator transliterates A to B when operating in the forward direction, and B to A when operating in the reverse direction.

 Value: 1

## Public methods

### createFromRules

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createFromRules(
    ID: String!, 
    rules: String!, 
    dir: Int
): Transliterator!
```

Returns a `Transliterator` object constructed from the given rule string. This will be a rule-based Transliterator, if the rule string contains only rules, or a compound Transliterator, if it contains ID blocks, or a null Transliterator, if it contains ID blocks which parse as empty for the given direction.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the id for the transliterator. |
| `rules` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: rules, separated by ';' |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either FORWARD or REVERSE. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#!` | a newly created Transliterator |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if there is a problem with the ID or the rules |

### filteredTransliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun filteredTransliterate(
    text: Replaceable!, 
    index: Transliterator.Position!, 
    incremental: Boolean
): Unit
```

Transliterate a substring of text, as specified by index, taking filters into account. This method is for subclasses that need to delegate to another transliterator.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the text to be transliterated |
| `index` | [Transliterator.Position](../android/icu/text/Transliterator.Position.md)!: the position indices |
| `incremental` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, then assume more characters may be inserted at index.limit, and postpone processing to accommodate future incoming characters |
| --- | --- |

### finishTransliteration

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun finishTransliteration(
    text: Replaceable!, 
    index: Transliterator.Position!
): Unit
```

Finishes any pending transliterations that were waiting for more characters. Clients should call this method as the last call after a sequence of one or more calls to `transliterate()`.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the buffer holding transliterated and untransliterated text. |
| `index` | [Transliterator.Position](../android/icu/text/Transliterator.Position.md)!: the array of indices previously passed to #transliterate |

### getAvailableIDs

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableIDs(): Enumeration<String!>!
```

Returns an enumeration over the programmatic names of registered `Transliterator` objects. This includes both system transliterators and user transliterators registered using `registerClass()`. The enumerated names may be passed to `getInstance()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | An `Enumeration` over `String` objects |

**See Also**

### getAvailableSources

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableSources(): Enumeration<String!>!
```

Returns an enumeration over the source names of registered transliterators. Source names may be passed to getAvailableTargets() to obtain available targets for each source.

### getAvailableTargets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableTargets(source: String!): Enumeration<String!>!
```

Returns an enumeration over the target names of registered transliterators having a given source name. Target names may be passed to getAvailableVariants() to obtain available variants for each source and target pair.

### getAvailableVariants

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getAvailableVariants(
    source: String!, 
    target: String!
): Enumeration<String!>!
```

Returns an enumeration over the variant names of registered transliterators having a given source name and target name.

### getDisplayName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDisplayName(ID: String!): String!
```

Returns a name for this transliterator that is appropriate for display to the user in the default `DISPLAY` locale. See `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getDisplayName(kotlin.String,%20java.util.Locale)` for details.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/util/ULocale.Category.html#`

### getDisplayName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(
    id: String!, 
    inLocale: ULocale!
): String!
```

Returns a name for this transliterator that is appropriate for display to the user in the given locale. This name is taken from the locale resource data in the standard manner of the `java.text` package.

If no localized names exist in the system resource bundles, a name is synthesized using a localized `MessageFormat` pattern from the resource data. The arguments to this pattern are an integer followed by one or two strings. The integer is the number of strings, either 1 or 2. The strings are formed by splitting the ID for this transliterator at the first '-'. If there is no '-', then the entire ID forms the only string.

| Parameters ||
|---|---|
| `inLocale` | [ULocale](../android/icu/util/ULocale.md)!: the ULocale in which the display name should be localized. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/text/MessageFormat.html#`

### getDisplayName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDisplayName(
    id: String!, 
    inLocale: Locale!
): String!
```

Returns a name for this transliterator that is appropriate for display to the user in the given locale. This name is taken from the locale resource data in the standard manner of the `java.text` package.

If no localized names exist in the system resource bundles, a name is synthesized using a localized `MessageFormat` pattern from the resource data. The arguments to this pattern are an integer followed by one or two strings. The integer is the number of strings, either 1 or 2. The strings are formed by splitting the ID for this transliterator at the first '-'. If there is no '-', then the entire ID forms the only string.

| Parameters ||
|---|---|
| `inLocale` | [Locale](../java/util/Locale.md)!: the Locale in which the display name should be localized. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/text/MessageFormat.html#`

### getElements

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getElements(): Array<Transliterator!>!
```

Return the elements that make up this transliterator. For example, if the transliterator "NFD;Jamo-Latin;Latin-Greek" were created, the return value of this method would be an array of the three transliterator objects that make up that transliterator: \[NFD, Jamo-Latin, Latin-Greek\].

If this transliterator is not composed of other transliterators, then this method will return an array of length one containing a reference to this transliterator.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#!>!` | an array of one or more transliterators that make up this transliterator |

### getFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFilter(): UnicodeFilter!
```

Returns the filter used by this transliterator, or `null` if this transliterator uses no filter.

### getID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getID(): String!
```

Returns a programmatic identifier for this transliterator. If this identifier is passed to `getInstance()`, it will return this object, if it has been registered.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableIDs()`

### getInstance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getInstance(ID: String!): Transliterator!
```

Returns a `Transliterator` object given its ID. The ID must be a system transliterator ID.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a valid ID, as enumerated by `getAvailableIDs()` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#!` | A `Transliterator` object with the given ID |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given ID is invalid. |

### getInstance

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(
    ID: String!, 
    dir: Int
): Transliterator!
```

Returns a `Transliterator` object given its ID. The ID must be a system transliterator ID.

| Parameters ||
|---|---|
| `ID` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a valid ID, as enumerated by `getAvailableIDs()` |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): either FORWARD or REVERSE. If REVERSE then the inverse of the given ID is instantiated. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#!` | A `Transliterator` object with the given ID |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given ID is invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getAvailableIDs()`
- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getID()`

### getInverse

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInverse(): Transliterator!
```

Returns this transliterator's inverse. See the class documentation for details. This implementation simply inverts the two entities in the ID and attempts to retrieve the resulting transliterator. That is, if `getID()` returns "A-B", then this method will return the result of `getInstance("B-A")`, or `null` if that call fails.

Subclasses with knowledge of their inverse may wish to override this method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#!` | a transliterator that is an inverse, not necessarily exact, of this transliterator, or `null` if no such transliterator is registered. |

### getMaximumContextLength

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaximumContextLength(): Int
```

Returns the length of the longest context required by this transliterator. This is *preceding* context. The default value is zero, but subclasses can change this by calling `setMaximumContextLength()`. For example, if a transliterator translates "ddd" (where d is any digit) to "555" when preceded by "(ddd)", then the preceding context length is 5, the length of "(ddd)".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The maximum number of preceding context characters this transliterator needs to examine |

### getSourceSet

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSourceSet(): UnicodeSet!
```

Returns the set of all characters that may be modified in the input text by this Transliterator. This incorporates this object's current filter; if the filter is changed, the return value of this function will change. The default implementation returns an empty set. The return result is approximate in any case and is intended for use by tests, tools, or utilities.
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getTargetSet()`

### getTargetSet

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetSet(): UnicodeSet!
```

Returns the set of all characters that may be generated as replacement text by this transliterator. The default implementation returns the empty set. Some subclasses may override this method to return a more precise result. The return result is approximate in any case and is intended for use by tests, tools, or utilities requiring such meta-information.

Warning. You might expect an empty filter to always produce an empty target. However, consider the following:

```kotlin
[Pp]{}[\u03A3\u03C2\u03C3\u03F7\u03F8\u03FA\u03FB] > \';
  
```
With a filter of \[\], you still get some elements in the target set, because this rule will still match. It could be recast to the following if it were important.

```kotlin
[Pp]{([\u03A3\u03C2\u03C3\u03F7\u03F8\u03FA\u03FB])} > \' | $1;
  
```
**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#getTargetSet()`

### setFilter

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFilter(filter: UnicodeFilter!): Unit
```

Changes the filter used by this transliterator. If the filter is set to `null` then no filtering will occur.

Callers must take care if a transliterator is in use by multiple threads. The filter should not be changed by one thread while another thread may be transliterating.

### toRules

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toRules(escapeUnprintable: Boolean): String!
```

Returns a rule string for this transliterator.

| Parameters ||
|---|---|
| `escapeUnprintable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true, then unprintable characters will be converted to escape form backslash-'u' or backslash-'U'. |

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(text: Replaceable!): Unit
```

Transliterates an entire string in place. Convenience method.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the string to be transliterated |

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(
    text: Replaceable!, 
    index: Transliterator.Position!
): Unit
```

Transliterates the portion of the text buffer that can be transliterated unambiguosly. This is a convenience method; see `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.String)` for details.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the buffer holding transliterated and untransliterated text |
| `index` | [Transliterator.Position](../android/icu/text/Transliterator.Position.md)!: the start and limit of the text, the position of the cursor, and the start and limit of transliteration. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.String)`

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(
    text: Replaceable!, 
    index: Transliterator.Position!, 
    insertion: Int
): Unit
```

Transliterates the portion of the text buffer that can be transliterated unambiguosly after a new character has been inserted, typically as a result of a keyboard event. This is a convenience method; see `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.String)` for details.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the buffer holding transliterated and untransliterated text |
| `index` | [Transliterator.Position](../android/icu/text/Transliterator.Position.md)!: the start and limit of the text, the position of the cursor, and the start and limit of transliteration. |
| `insertion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): text to be inserted and possibly transliterated into the translation buffer at `index.contextLimit`. |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#transliterate(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position,%20kotlin.String)`

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(
    text: Replaceable!, 
    index: Transliterator.Position!, 
    insertion: String!
): Unit
```

Transliterates the portion of the text buffer that can be transliterated unambiguosly after new text has been inserted, typically as a result of a keyboard event. The new text in `insertion` will be inserted into `text` at `index.contextLimit`, advancing `index.contextLimit` by `insertion.length()`. Then the transliterator will try to transliterate characters of `text` between `index.start` and `index.contextLimit`. Characters before `index.start` will not be changed.

Upon return, values in `index` will be updated. `index.contextStart` will be advanced to the first character that future calls to this method will read. `index.start` and `index.contextLimit` will be adjusted to delimit the range of text that future calls to this method may change.

Typical usage of this method begins with an initial call with `index.contextStart` and `index.contextLimit` set to indicate the portion of `text` to be transliterated, and `index.start == index.contextStart`. Thereafter, `index` can be used without modification in future calls, provided that all changes to `text` are made via this method.

This method assumes that future calls may be made that will insert new text into the buffer. As a result, it only performs unambiguous transliterations. After the last call to this method, there may be untransliterated text that is waiting for more input to resolve an ambiguity. In order to perform these pending transliterations, clients should call `https://developer.android.com/reference/kotlin/android/icu/text/Transliterator#finishTransliteration(android.icu.text.Replaceable,%20android.icu.text.Transliterator.Position)` after the last call to this method has been made.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the buffer holding transliterated and untransliterated text |
| `index` | [Transliterator.Position](../android/icu/text/Transliterator.Position.md)!: the start and limit of the text, the position of the cursor, and the start and limit of transliteration. |
| `insertion` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: text to be inserted and possibly transliterated into the translation buffer at `index.contextLimit`. If `null` then no text is inserted. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `index` is invalid |

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(
    text: Replaceable!, 
    start: Int, 
    limit: Int
): Int
```

Transliterates a segment of a string, with optional filtering.

| Parameters ||
|---|---|
| `text` | [Replaceable](../android/icu/text/Replaceable.md)!: the string to be transliterated |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the beginning index, inclusive; `0 <= start <= limit`. |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ending index, exclusive; `start <= limit <= text.length()`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The new limit index. The text previously occupying `[start, limit)` has been transliterated, possibly to a string of a different length, at `[start, `*new-limit* `)`, where *new-limit* is the return value. If the input offsets are out of bounds, the returned value is -1 and the input string remains unchanged. |

### transliterate

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun transliterate(text: String!): String!
```

Transliterate an entire string and returns the result. Convenience method.

| Parameters ||
|---|---|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the string to be transliterated |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The transliterated text |
