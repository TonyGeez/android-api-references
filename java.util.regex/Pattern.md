# Pattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Pattern

```
class Pattern : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.regex.Pattern](../java/util/regex/Pattern.md) |

A compiled representation of a regular expression.

A regular expression, specified as a string, must first be compiled into an instance of this class. The resulting pattern can then be used to create a [Matcher](../java/util/regex/Matcher.md) object that can match arbitrary against the regular expression. All of the state involved in performing a match resides in the matcher, so many matchers can share the same pattern.

A typical invocation sequence is thus 

```kotlin
Pattern p = Pattern.#compile("a*b");
  Matcher m = p.<code><a docref="java.util.regex.Pattern$matcher(kotlin.CharSequence)">matcher</a></code>("aaaaab");
  boolean b = m.<code><a docref="java.util.regex.Matcher$matches()">matches</a></code>();
```

A [matches](../java/util/regex/Pattern.md))method is defined by this class as a convenience for when a regular expression is used just once. This method compiles an expression and matches an input sequence against it in a single invocation. The statement 

```kotlin
boolean b = Pattern.matches("a*b", "aaaaab");
```
is equivalent to the three statements above, though for repeated matches it is less efficient since it does not allow the compiled pattern to be reused.

Instances of this class are immutable and are safe for use by multiple concurrent threads. Instances of the [Matcher](../java/util/regex/Matcher.md) class are not safe for such use.

## Summary of regular-expression constructs

[d](../java/util/regex/Pattern.md) [m](../java/util/regex/Pattern.md) [s](../java/util/regex/Pattern.md) [u](../java/util/regex/Pattern.md) [x](../java/util/regex/Pattern.md) [U](../java/util/regex/Pattern.md)

| Construct | Matches |
| --- | --- |
| Characters ||
| *x* | The character*x* |
| `\\` | The backslash character |
| --- | --- |
| `\0`*n* | The character with octal value`0`*n* (0`<=`*n* `<=`7) |
| `\0`*nn* | The character with octal value`0`*nn* (0`<=`*n* `<=`7) |
| `\0`*mnn* | The character with octal value`0`*mnn* (0`<=`*m* `<=`3, 0`<=`*n* `<=`7) |
| --- | --- |
| `\x`*hh* | The character with hexadecimal value`0x`*hh* |
| `\u`*hhhh* | The character with hexadecimal value`0x`*hhhh* |
| `\x`*{h...h}* | The character with hexadecimal value`0x`*h...h* ([Character.MIN_CODE_POINT](../java/lang/Character.md)\<=`0x`*h...h* \<= [Character.MAX_CODE_POINT](../java/lang/Character.md)) |
| --- | --- |
| `\N{`*name* `}` | The character with Unicode character name*'name'* |
| `\t` | The tab character (`'\u0009'`) |
| `\n` | The newline (line feed) character (`'\u000A'`) |
| --- | --- |
| `\r` | The carriage-return character (`'\u000D'`) |
| `\f` | The form-feed character (`'\u000C'`) |
| `\a` | The alert (bell) character (`'\u0007'`) |
| --- | --- |
| `\e` | The escape character (`'\u001B'`) |
| `\c`*x* | The control character corresponding to*x* |
| Character classes ||
| --- | --- |
| `[abc]` | `a`,`b`, or`c`(simple class) |
| `[^abc]` | Any character except`a`,`b`, or`c`(negation) |
| `[a-zA-Z]` | `a`through`z`or`A`through`Z`, inclusive (range) |
| --- | --- |
| `[a-d[m-p]]` | `a`through`d`, or`m`through`p`:`[a-dm-p]`(union) |
| `[a-z&&[def]]` | `d`,`e`, or`f`(intersection) |
| `[a-z&&[^bc]]` | `a`through`z`, except for`b`and`c`:`[ad-z]`(subtraction) |
| --- | --- |
| `[a-z&&[^m-p]]` | `a`through`z`, and not`m`through`p`:`[a-lq-z]`(subtraction) |
| Predefined character classes ||
| `.` | Any character (may or may not match [line terminators](../java/util/regex/Pattern.md)) |
| --- | --- |
| `\d` | A digit:`\p{IsDigit}` |
| `\D` | A non-digit:`[^\d]` |
| `\h` | A horizontal whitespace character:`[ \t\xA0\u1680\u180e\u2000-\u200a\u202f\u205f\u3000]` |
| --- | --- |
| `\H` | A non-horizontal whitespace character:`[^\h]` |
| `\s` | A whitespace character:`\p{IsWhite_Space}` |
| `\S` | A non-whitespace character:`[^\s]` |
| --- | --- |
| `\v` | A vertical whitespace character:`[\n\x0B\f\r\x85\u2028\u2029]` |
| `\V` | A non-vertical whitespace character:`[^\v]` |
| `\w` | A word character:`[\p{alpha}\p{gc=Mark}\p{digit}\p{gc=Connector_Punctuation}\p{Join_Control}]` |
| --- | --- |
| `\W` | A non-word character:`[^\w]` |
| **POSIX character classes (Unicode-aware)** ||
| `\p{Lower}` | A lower-case alphabetic character:`\p{IsLowercase}` |
| --- | --- |
| `\p{Upper}` | An upper-case alphabetic character:`\p{IsUppercase}` |
| `\p{ASCII}` | All ASCII:`[\x00-\x7F]` |
| `\p{Alpha}` | An alphabetic character:`[\p{IsAlphabetic}]` |
| --- | --- |
| `\p{IsDigit}` | A decimal digit:`\p{gc=Decimal_Number}` |
| `\p{Alnum}` | An alphanumeric character:`[\p{Alpha}\p{Digit}]` |
| `\p{Punct}` | Punctuation:`\p{IsPunctuation}` |
| --- | --- |
| `\p{Graph}` | A visible character:`[^p{space}\p{gc=Control}\p{gc=Surrogate}\p{gc=Unassigned}]` |
| `\p{Print}` | A printable character:`[\p{Graph}\p{Blank}&&[^\p{Cntrl}]]` |
| `\p{Blank}` | A space or a tab:`[\p{gc=Space_Separator}\N{CHARACTER TABULATION}]` |
| --- | --- |
| `\p{Cntrl}` | A control character:`\p{gc=Control}` |
| `\p{XDigit}` | A hexadecimal digit:`[\p{gc=Decimal_Number}\p{IsHex_Digit}]` |
| `\p{Space}` | A whitespace character:`\p{IsWhite_Space}` |
| --- | --- |
| POSIX-Compatible expression | See [Unicode documentation](http://www.unicode.org/reports/tr18/#Compatibility_Properties) |
| java.lang.Character classes (simple [java character type](../java/util/regex/Pattern.md)) ||
| `\p{javaLowerCase}` | Equivalent to java.lang.Character.isLowerCase() |
| --- | --- |
| `\p{javaUpperCase}` | Equivalent to java.lang.Character.isUpperCase() |
| `\p{javaWhitespace}` | Equivalent to java.lang.Character.isWhitespace() |
| `\p{javaMirrored}` | Equivalent to java.lang.Character.isMirrored() |
| --- | --- |
| Classes for Unicode scripts, blocks, categories and binary properties ||
| `\p{IsLatin}` | A Latin script character ([script](../java/util/regex/Pattern.md)) |
| `\p{InGreek}` | A character in the Greek block ([block](../java/util/regex/Pattern.md)) |
| --- | --- |
| `\p{Lu}` | An uppercase letter ([category](../java/util/regex/Pattern.md)) |
| `\p{IsAlphabetic}` | An alphabetic character ([binary property](../java/util/regex/Pattern.md)) |
| `\p{Sc}` | A currency symbol |
| --- | --- |
| `\P{InGreek}` | Any character except one in the Greek block (negation) |
| `[\p{L}&&[^\p{Lu}]]` | Any letter except an uppercase letter (subtraction) |
| Boundary matchers ||
| --- | --- |
| `^` | The beginning of a line |
| `$` | The end of a line |
| `\b` | A word boundary |
| --- | --- |
| `\B` | A non-word boundary |
| `\A` | The beginning of the input |
| `\G` | The end of the previous match |
| --- | --- |
| `\Z` | The end of the input but for the final [terminator](../java/util/regex/Pattern.md), if any |
| `\z` | The end of the input |
| Linebreak matcher ||
| --- | --- |
| `\R` | Any Unicode linebreak sequence, is equivalent to`\u000D\u000A|[\u000A\u000B\u000C\u000D\u0085\u2028\u2029] ` |
| Unicode Extended Grapheme matcher ||
| `\X` | Any Unicode extended grapheme cluster |
| --- | --- |
| Greedy quantifiers ||
| *X* `?` | *X*, once or not at all |
| *X* `*` | *X*, zero or more times |
| --- | --- |
| *X* `+` | *X*, one or more times |
| *X* `{`*n* `}` | *X* , exactly*n*times |
| *X* `{`*n* `,`} | *X* , at least*n*times |
| --- | --- |
| *X* `{`*n* `,`*m* `}` | *X* , at least*n* but not more than*m*times |
| Reluctant quantifiers ||
| *X* `??` | *X*, once or not at all |
| --- | --- |
| *X* `*?` | *X*, zero or more times |
| *X* `+?` | *X*, one or more times |
| *X* `{`*n* `}?` | *X* , exactly*n*times |
| --- | --- |
| *X* `{`*n* `,}?` | *X* , at least*n*times |
| *X* `{`*n* `,`*m* `}?` | *X* , at least*n* but not more than*m*times |
| Possessive quantifiers ||
| --- | --- |
| *X* `?+` | *X*, once or not at all |
| *X* `*+` | *X*, zero or more times |
| *X* `++` | *X*, one or more times |
| --- | --- |
| *X* `{`*n* `}+` | *X* , exactly*n*times |
| *X* `{`*n* `,}+` | *X* , at least*n*times |
| *X* `{`*n* `,`*m* `}+` | *X* , at least*n* but not more than*m*times |
| --- | --- |
| Logical operators ||
| *XY* | *X* followed by*Y* |
| *X* `|`*Y* | Either*X* or*Y* |
| --- | --- | --- |
| `(`*X* `)` | X, as a [capturing group](../java/util/regex/Pattern.md) |
| Back references ||
| `\`*n* | Whatever the*n* th [capturing group](../java/util/regex/Pattern.md) matched |
| --- | --- |
| `\`*k* \<*name*\> | Whatever the [named-capturing group](../java/util/regex/Pattern.md)"name" matched. Only available for API 26 or above |
| Quotation ||
| `\` | Nothing, but quotes the following character |
| --- | --- |
| `\Q` | Nothing, but quotes all characters until`\E` |
| `\E` | Nothing, but ends quoting started by`\Q` |
| Special constructs (named-capturing and non-capturing) ||
| --- | --- |
| `(?<` [name](../java/util/regex/Pattern.md)`>`*X* `)` | *X*, as a named-capturing group. Only available for API 26 or above. |
| `(?:`*X* `)` | *X*, as a non-capturing group |
| `(?idmsux-idmsux) ` |
| `(?idmsuxU-idmsuxU:`*X* `)` | *X* , as a [non-capturing group](../java/util/regex/Pattern.md) with the given flags [i](../java/util/regex/Pattern.md) [d](../java/util/regex/Pattern.md) [m](../java/util/regex/Pattern.md) [s](../java/util/regex/Pattern.md) [u](../java/util/regex/Pattern.md) [x](../java/util/regex/Pattern.md) [U](../java/util/regex/Pattern.md) on - off |
| --- | --- |
| `(?=`*X* `)` | *X*, via zero-width positive lookahead |
| `(?!`*X* `)` | *X*, via zero-width negative lookahead |
| `(?<=`*X* `)` | *X*, via zero-width positive lookbehind |
| --- | --- |
| `(?<!`*X* `)` | *X*, via zero-width negative lookbehind |
| `(?>`*X* `)` | *X*, as an independent, non-capturing group |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## Backslashes, escapes, and quoting

The backslash character (`'\'`) serves to introduce escaped constructs, as defined in the table above, as well as to quote characters that otherwise would be interpreted as unescaped constructs. Thus the expression`\\`matches a single backslash and`\{`matches a left brace.

It is an error to use a backslash prior to any alphabetic character that does not denote an escaped construct; these are reserved for future extensions to the regular-expression language. A backslash may be used prior to a non-alphabetic character regardless of whether that character is part of an unescaped construct.

Backslashes within string literals in Java source code are interpreted as required by The Java Language Specification as either Unicode escapes (section {@jls 3.3}) or other character escapes (section {@jls 3.10.6}) It is therefore necessary to double backslashes in string literals that represent regular expressions to protect them from interpretation by the Java bytecode compiler. The string literal`"\b"`, for example, matches a single backspace character when interpreted as a regular expression, while`"\\b"`matches a word boundary. The string literal`"\(hello\)"`is illegal and leads to a compile-time error; in order to match the string`(hello)`the string literal`"\\(hello\\)"`must be used.

## Character Classes

Character classes may appear within other character classes, and may be composed by the union operator (implicit) and the intersection operator (`&&`). The union operator denotes a class that contains every character that is in at least one of its operand classes. The intersection operator denotes a class that contains every character that is in both of its operand classes.

The precedence of character-class operators is as follows, from highest to lowest:

| Precedence | Name | Example |
| --- | --- | --- |
| 1 | Literal escape | `\x` |
| 2 | Grouping | `[...]` |
| 3 | Range | `a-z` |
| --- | --- | --- |
| 4 | Union | `[a-e][i-u]` |
| 5 | Intersection | `[a-z&&[aeiou]]` |
|------------|----------------|------------------|

Note that a different set of metacharacters are in effect inside a character class than outside a character class. For instance, the regular expression`.`loses its special meaning inside a character class, while the expression`-`becomes a range forming metacharacter.

## Line terminators

A*line terminator* is a one- or two-character sequence that marks the end of a line of the input character sequence. Any Unicode linebreak sequence [`'\R'`](../java/util/regex/Pattern.md) is recognized as*line terminator*. In particular, on Android, the following are also recognized as line terminators:

- A vertical tabulation character (`'\u000B'`), or
- A form-feed character (`'\u000C'`).

If [UNIX_LINES](../java/util/regex/Pattern.md) mode is activated, then the only line terminators recognized are newline characters.

The regular expression`.`matches any character except a line terminator unless the [DOTALL](../java/util/regex/Pattern.md) flag is specified.

By default, the regular expressions`^`and`$`ignore line terminators and only match at the beginning and the end, respectively, of the entire input sequence. If [MULTILINE](../java/util/regex/Pattern.md) mode is activated then`^`matches at the beginning of input and after any line terminator except at the end of input. When in [MULTILINE](../java/util/regex/Pattern.md) mode`$`matches just before a line terminator or the end of the input sequence.

## Groups and capturing

### Group number

Capturing groups are numbered by counting their opening parentheses from left to right. In the expression`((A)(B(C)))`, for example, there are four such groups:

1. `((A)(B(C)))`
2. `(A)`
3. `(B(C))`
4. `(C)`

Group zero always stands for the entire expression.

Capturing groups are so named because, during a match, each subsequence of the input sequence that matches such a group is saved. The captured subsequence may be used later in the expression, via a back reference, and may also be retrieved from the matcher once the match operation is complete.

### Group name

The constructs and APIs are available since API level 26. A capturing group can also be assigned a "name", a`named-capturing group`, and then be back-referenced later by the "name". Group names are composed of the following characters. The first character must be a`letter`.

- The uppercase letters`'A'`through`'Z'`(`'\u0041'`through`'\u005a'`),
- The lowercase letters`'a'`through`'z'`(`'\u0061'`through`'\u007a'`),
- The digits`'0'`through`'9'`(`'\u0030'`through`'\u0039'`),

A`named-capturing group`is still numbered as described in [Group number](../java/util/regex/Pattern.md).

The captured input associated with a group is always the subsequence that the group most recently matched. If a group is evaluated a second time because of quantification then its previously-captured value, if any, will be retained if the second evaluation fails. Matching the string`"aba"`against the expression`(a(b)?)+`, for example, leaves group two set to`"b"`. All captured input is discarded at the beginning of each match.

Groups beginning with`(?`are either pure,*non-capturing* groups that do not capture text and do not count towards the group total, or*named-capturing*group.

## Unicode support

This class is in conformance with Level 1 of [*Unicode Technical Standard #18: Unicode Regular Expressions*](http://www.unicode.org/reports/tr18/), plus RL2.1 Canonical Equivalents and RL2.2 Extended Grapheme Clusters.

**Unicode escape sequences** such as`\u2014`in Java source code are processed as described in section {@jls 3.3} of The Java Language Specification. Such escape sequences are also implemented directly by the regular-expression parser so that Unicode escapes can be used in expressions that are read from files or from the keyboard. Thus the strings`"\u2014"`and`"\\u2014"`, while not equal, compile into the same pattern, which matches the character with hexadecimal value`0x2014`.

A Unicode character can also be represented by using its**Hex notation** (hexadecimal code point value) directly as described in construct`\x{...}`, for example a supplementary character U+2011F can be specified as`\x{2011F}`, instead of two consecutive Unicode escape sequences of the surrogate pair`\uD840``\uDD1F`.

**Unicode character names** are supported by the named character construct`\N{`...`}`, for example,`\N{WHITE SMILING FACE}`specifies character`\u263A`. The character names supported by this class are the valid Unicode character names matched by`java.lang.Character.codePointOf(String) Character.codePointOf(name)`.

[**Unicode extended grapheme clusters**](http://www.unicode.org/reports/tr18/#Default_Grapheme_Clusters) are supported by the grapheme cluster matcher`\X`.

Unicode scripts, blocks, categories and binary properties are written with the`\p`and`\P`constructs as in Perl.`\p{`*prop* `}`matches if the input has the property*prop* , while`\P{`*prop* `}`does not match if the input has that property.

Scripts, blocks, categories and binary properties can be used both inside and outside of a character class.

**Scripts** are specified either with the prefix`Is`supported since Android 10, as in`IsHiragana`, or by using the`script`keyword (or its short form`sc`) as in`script=Hiragana`or`sc=Hiragana`.

The script names supported by`Pattern`are the valid script names accepted and defined by [UnicodeScript.forName](../java/lang/Character.UnicodeScript.md)).

**Blocks** are specified with the prefix`In`, as in`InMongolian`, or by using the keyword`block`(or its short form`blk`) as in`block=Mongolian`or`blk=Mongolian`.

The block names supported by`Pattern`are the valid block names accepted and defined by [UnicodeBlock.forName](../java/lang/Character.UnicodeBlock.md)).

**Categories** may be specified with the optional prefix`Is`: Both`\p{IsL}`supported since Android 10 and`\p{L}`denote the category of Unicode letters. Same as scripts and blocks, categories can also be specified by using the keyword`general_category`(or its short form`gc`) as in`general_category=Lu`or`gc=Lu`.

The supported categories are those of [*The Unicode Standard*](http://www.unicode.org/standard/standard.html) in the version specified by the [Character](../java/lang/Character.md) class. The category names are those defined in the Standard, both normative and informative.

**Binary properties** are specified with the prefix`Is`since Android 10, as in`IsAlphabetic`. The prefix`Is`isn't needed before Android 10, as in`Alphabetic`. The supported binary properties by`Pattern`are

- Alphabetic
- Ideographic
- Letter
- Lowercase
- Uppercase
- Titlecase
- Punctuation
- Control
- White_Space
- Digit
- Hex_Digit
- Join_Control
- Noncharacter_Code_Point
- Assigned

The**Predefined Character classes** and**POSIX character classes** are in conformance with the recommendation of*Annex C: Compatibility Properties* of [*Unicode Technical Standard #18: Unicode Regular Expressions*](http://www.unicode.org/reports/tr18/).

Categories that behave like the java.lang.Character boolean is*methodname* methods (except for the deprecated ones) are available through the same`\p{`*prop* `}`syntax where the specified property has the name`java`*methodname*.

### Behavior starting from API level 10 (Android 2.3)

Starting from Android 2.3 Gingerbread, ICU4C becomes the backend of the regular expression implementation. Android could behave differently compared with other regex implementation, e.g. literal right brace ('}') has to be escaped on Android.

Some other behavior differences can be found in the [ICU documentation](https://unicode-org.github.io/icu/userguide/strings/regexp.html#differences-with-java-regular-expressions).

## Comparison to Perl 5

The`Pattern`engine performs traditional NFA-based matching with ordered alternation as occurs in Perl 5.

Perl constructs not supported by this class:

- The backreference constructs,`\g{`*n* `}`for the*n* th [capturing group](../java/util/regex/Pattern.md) and`\g{`*name* `}`for [named-capturing group](../java/util/regex/Pattern.md).
- The conditional constructs`(?(`*condition* `)`*X* `)`and`(?(`*condition* `)`*X* `|`*Y* `)`,
| --- | --- |
- The embedded code constructs`(?{`*code* `})`and`(??{`*code* `})`,
- The embedded comment syntax`(?#comment)`, and
- The preprocessing operations`\l``\u`,`\L`, and`\U`.

Constructs supported by this class but not by Perl:

- Character-class union and intersection as described [above](../java/util/regex/Pattern.md).

Notable differences from Perl:

- In Perl,`\1`through`\9`are always interpreted as back references; a backslash-escaped number greater than`9`is treated as a back reference if at least that many subexpressions exist, otherwise it is interpreted, if possible, as an octal escape. In this class octal escapes must always begin with a zero. In this class, [compile(java.lang.String)](../java/util/regex/Pattern.md))throws [PatternSyntaxException](../java/util/regex/PatternSyntaxException.md) for any non-existent back references. Please use`\Q`and`\E`to quote any digit literals followed by back references.
- Perl uses the`g`flag to request a match that resumes where the last match left off. This functionality is provided implicitly by the [Matcher](../java/util/regex/Matcher.md) class: Repeated invocations of the java.util.regex.Matcher#find method will resume where the last match left off, unless the matcher is reset.
- In Perl, embedded flags at the top level of an expression affect the whole expression. In this class, embedded flags always take effect at the point at which they appear, whether they are at the top level or within a group; in the latter case, flags are restored at the end of the group just as in Perl.

For a more precise description of the behavior of regular expression constructs, please see [*Mastering Regular Expressions, 3rd Edition*, Jeffrey E. F. Friedl, O'Reilly and Associates, 2006.](http://www.oreilly.com/catalog/regex3/)

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CANON_EQ](../java/util/regex/Pattern.md) This flag is not supported on Android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CASE_INSENSITIVE](../java/util/regex/Pattern.md) Enables case-insensitive matching. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMMENTS](../java/util/regex/Pattern.md) Permits whitespace and comments in pattern. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DOTALL](../java/util/regex/Pattern.md) Enables dotall mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LITERAL](../java/util/regex/Pattern.md) Enables literal parsing of the pattern. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MULTILINE](../java/util/regex/Pattern.md) Enables multiline mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNICODE_CASE](../java/util/regex/Pattern.md) Enables Unicode-aware case folding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNICODE_CHARACTER_CLASS](../java/util/regex/Pattern.md) This flag is not supported on Android, and Unicode character classes are always used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNIX_LINES](../java/util/regex/Pattern.md) Enables Unix lines mode. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Predicate](../java/util/function/Predicate.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [asMatchPredicate](../java/util/regex/Pattern.md))`()` Creates a predicate that tests if this pattern matches a given input string. |
| [Predicate](../java/util/function/Predicate.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [asPredicate](../java/util/regex/Pattern.md))`()` Creates a predicate that tests if this pattern is found in a given input string. |
| static [Pattern](../java/util/regex/Pattern.md) | [compile](../java/util/regex/Pattern.md))`(`regex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Compiles the given regular expression into a pattern. |
| --- | --- |
| static [Pattern](../java/util/regex/Pattern.md) | [compile](../java/util/regex/Pattern.md))`(`regex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Compiles the given regular expression into a pattern with the given flags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [flags](../java/util/regex/Pattern.md))`()` Returns this pattern's match flags. |
| [Matcher](../java/util/regex/Matcher.md) | [matcher](../java/util/regex/Pattern.md))`(`input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Creates a matcher that will match the given input against this pattern. |
| --- | --- |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](../java/util/regex/Pattern.md))`(`regex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Compiles the given regular expression and attempts to match the given input against it. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [pattern](../java/util/regex/Pattern.md))`()` Returns the regular expression from which this pattern was compiled. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [quote](../java/util/regex/Pattern.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns a literal pattern`String`for the specified`String`. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [split](../java/util/regex/Pattern.md))`(`input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Splits the given input sequence around matches of this pattern. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [split](../java/util/regex/Pattern.md))`(`input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Splits the given input sequence around matches of this pattern. |
| [Stream](../java/util/stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [splitAsStream](../java/util/regex/Pattern.md))`(`input:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Creates a stream from the given input sequence around matches of this pattern. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/regex/Pattern.md))`()` Returns the string representation of this pattern. |

## Constants

### CANON_EQ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANON_EQ: Int
```

This flag is not supported on Android. 

 Value: 128

### CASE_INSENSITIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CASE_INSENSITIVE: Int
```

Enables case-insensitive matching.

Case-insensitive matching is Unicode-aware on Android.

Case-insensitive matching can also be enabled via the embedded flag expression`(?i)`.

Specifying this flag may impose a slight performance penalty. 

 Value: 2

### COMMENTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMMENTS: Int
```

Permits whitespace and comments in pattern.

In this mode, whitespace is ignored, and embedded comments starting withare ignored until the end of a line.

Comments mode can also be enabled via the embedded flag expression`(?x)`. 

 Value: 4

### DOTALL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DOTALL: Int
```

Enables dotall mode.

In dotall mode, the expression`.`matches any character, including a line terminator. By default this expression does not match line terminators.

Dotall mode can also be enabled via the embedded flag expression`(?s)`. (The`s`is a mnemonic for "single-line" mode, which is what this is called in Perl.) 

 Value: 32

### LITERAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LITERAL: Int
```

Enables literal parsing of the pattern.

When this flag is specified then the input string that specifies the pattern is treated as a sequence of literal characters. Metacharacters or escape sequences in the input sequence will be given no special meaning.

The flags CASE_INSENSITIVE and UNICODE_CASE retain their impact on matching when used in conjunction with this flag. The other flags become superfluous.

There is no embedded flag character for enabling literal parsing. 

 Value: 16

### MULTILINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MULTILINE: Int
```

Enables multiline mode.

In multiline mode the expressions`^`and`$`match just after or just before, respectively, a line terminator or the end of the input sequence. By default these expressions only match at the beginning and the end of the entire input sequence.

Multiline mode can also be enabled via the embedded flag expression`(?m)`. 

 Value: 8

### UNICODE_CASE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNICODE_CASE: Int
```

Enables Unicode-aware case folding. This flag is ignoredon Android. When [CASE_INSENSITIVE](../java/util/regex/Pattern.md) flag is provided, case-insensitive matching is always done in a manner consistent with the Unicode Standard.

The embedded flag`(?u)`is ignored.

Specifying this flag may impose a performance penalty. 

 Value: 64

### UNICODE_CHARACTER_CLASS

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNICODE_CHARACTER_CLASS: Int
```

This flag is not supported on Android, and Unicode character classes are always used.

See the Unicode version of*Predefined character classes* and*POSIX character classes* are in conformance with [*Unicode Technical Standard #18: Unicode Regular Expressions*](http://www.unicode.org/reports/tr18/)*Annex C: Compatibility Properties*.

<br />

 Value: 256

### UNIX_LINES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNIX_LINES: Int
```

Enables Unix lines mode.

In this mode, only the`'\n'`line terminator is recognized in the behavior of`.`,`^`, and`$`.

Unix lines mode can also be enabled via the embedded flag expression`(?d)`. 

 Value: 1

## Public methods

### asMatchPredicate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun asMatchPredicate(): Predicate<String!>
```

Creates a predicate that tests if this pattern matches a given input string.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Predicate](../java/util/function/Predicate.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The predicate which can be used for matching an input string against this pattern. |

**See Also**

- [java.util.regex.Matcher#matches](../java/util/regex/Matcher.md)) 

### asPredicate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun asPredicate(): Predicate<String!>
```

Creates a predicate that tests if this pattern is found in a given input string.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Predicate](../java/util/function/Predicate.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The predicate which can be used for finding a match on a subsequence of a string |

**See Also**

### compile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compile(regex: String): Pattern
```

Compiles the given regular expression into a pattern.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The expression to be compiled |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Pattern](../java/util/regex/Pattern.md) | the given regular expression compiled into a pattern |

| Exceptions ||
|------------------------------------------|---------------------------------------|
| `java.util.regex.PatternSyntaxException` | If the expression's syntax is invalid |

### compile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun compile(
    regex: String, 
    flags: Int
): Pattern
```

Compiles the given regular expression into a pattern with the given flags.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The expression to be compiled |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Match flags, a bit mask that may include [CASE_INSENSITIVE](../java/util/regex/Pattern.md), [MULTILINE](../java/util/regex/Pattern.md), [DOTALL](../java/util/regex/Pattern.md), [UNICODE_CASE](../java/util/regex/Pattern.md), [UNIX_LINES](../java/util/regex/Pattern.md), [LITERAL](../java/util/regex/Pattern.md), and [COMMENTS](../java/util/regex/Pattern.md) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Pattern](../java/util/regex/Pattern.md) | the given regular expression compiled into a pattern with the given flags |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If bit values other than those corresponding to the defined match flags are set in`flags` |
| `java.util.regex.PatternSyntaxException` | If the expression's syntax is invalid |

### flags

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun flags(): Int
```

Returns this pattern's match flags.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The match flags specified when this pattern was compiled |

### matcher

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matcher(input: CharSequence): Matcher
```

Creates a matcher that will match the given input against this pattern.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The character sequence to be matched |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [Matcher](../java/util/regex/Matcher.md) | A new matcher for this pattern |

### matches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun matches(
    regex: String, 
    input: CharSequence
): Boolean
```

Compiles the given regular expression and attempts to match the given input against it.

An invocation of this convenience method of the form 

```kotlin
Pattern.matches(regex, input);
```
behaves in exactly the same way as the expression 

```kotlin
Pattern.compile(regex).matcher(input).matches()
```

If a pattern is to be used multiple times, compiling it once and reusing it will be more efficient than invoking this method each time.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The expression to be compiled |
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The character sequence to be matched |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether or not the regular expression matches on the input |

| Exceptions ||
|------------------------------------------|---------------------------------------|
| `java.util.regex.PatternSyntaxException` | If the expression's syntax is invalid |

### pattern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun pattern(): String
```

Returns the regular expression from which this pattern was compiled.

| Return ||
|----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The source of this pattern |

### quote

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun quote(s: String): String
```

Returns a literal pattern`String`for the specified`String`.

This method produces a`String`that can be used to create a`Pattern`that would match the string`s`as if it were a literal pattern.
Metacharacters or escape sequences in the input sequence will be given no special meaning.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The string to be literalized |

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A literal string replacement |

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun split(input: CharSequence): Array<String!>
```

Splits the given input sequence around matches of this pattern.

This method works as if by invoking the two-argument [split](../java/util/regex/Pattern.md))method with the given input sequence and a limit argument of zero. Trailing empty strings are therefore not included in the resulting array.

The input`"boo:and:foo"`, for example, yields the following results with these expressions:

| Regex | Result |
| --- | --- |
| : | `{ "boo", "and", "foo" }` |
| o | `{ "b", "", ":and:f" }` |
|-------|---------------------------|

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The character sequence to be split |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The array of strings computed by splitting the input around matches of this pattern |

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun split(
    input: CharSequence, 
    limit: Int
): Array<String!>
```

Splits the given input sequence around matches of this pattern.

The array returned by this method contains each substring of the input sequence that is terminated by another subsequence that matches this pattern or is terminated by the end of the input sequence. The substrings in the array are in the order in which they occur in the input. If this pattern does not match any subsequence of the input then the resulting array has just one element, namely the input sequence in string form.

When there is a positive-width match at the beginning of the input sequence then an empty leading substring is included at the beginning of the resulting array. A zero-width match at the beginning however can only produce such an empty leading substring for apps running on or targeting API versions \<= 28.

The`limit`parameter controls the number of times the pattern is applied and therefore affects the length of the resulting array.

- If the*limit* is positive then the pattern will be applied at most*limit* - 1 times, the array's length will be no greater than*limit*, and the array's last entry will contain all input beyond the last matched delimiter.
- If the*limit*is zero then the pattern will be applied as many times as possible, the array can have any length, and trailing empty strings will be discarded.
- If the*limit*is negative then the pattern will be applied as many times as possible and the array can have any length.

The input`"boo:and:foo"`, for example, yields the following results with these parameters:

| Regex | Limit | Result |
| --- | --- | --- |
| : | 2 | `{ "boo", "and:foo" }` |
| : | 5 | `{ "boo", "and", "foo" }` |
| : | -2 | `{ "boo", "and", "foo" }` |
| --- | --- | --- |
| o | 5 | `{ "b", "", ":and:f", "", "" }` |
| o | -2 | `{ "b", "", ":and:f", "", "" }` |
| o | 0 | `{ "b", "", ":and:f" }` |
|-------|-------|---------------------------------|

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The character sequence to be split |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result threshold, as described above |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The array of strings computed by splitting the input around matches of this pattern |

### splitAsStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun splitAsStream(input: CharSequence): Stream<String!>
```

Creates a stream from the given input sequence around matches of this pattern.

The stream returned by this method contains each substring of the input sequence that is terminated by another subsequence that matches this pattern or is terminated by the end of the input sequence. The substrings in the stream are in the order in which they occur in the input. Trailing empty strings will be discarded and not encountered in the stream.

If this pattern does not match any subsequence of the input then the resulting stream has just one element, namely the input sequence in string form.

When there is a positive-width match at the beginning of the input sequence then an empty leading substring is included at the beginning of the stream. A zero-width match at the beginning however never produces such empty leading substring.

If the input sequence is mutable, it must remain constant during the execution of the terminal stream operation. Otherwise, the result of the terminal stream operation is undefined.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `input` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):The character sequence to be split |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Stream](../java/util/stream/Stream.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The stream of strings computed by splitting the input around matches of this pattern |

**See Also**

- [#split(CharSequence)](../java/util/regex/Pattern.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns the string representation of this pattern. This is the regular expression from which this pattern was compiled.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The string representation of this pattern |
