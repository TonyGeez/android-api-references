Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamTokenizer

```
open class StreamTokenizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.StreamTokenizer](StreamTokenizer.md) |

The `StreamTokenizer` class takes an input stream and parses it into "tokens", allowing the tokens to be read one at a time. The parsing process is controlled by a table and a number of flags that can be set to various states. The stream tokenizer can recognize identifiers, numbers, quoted strings, and various comment styles.

Each byte read from the input stream is regarded as a character in the range `'\u005Cu0000'` through `'\u005Cu00FF'`. The character value is used to look up five possible attributes of the character: *white space* , *alphabetic* , *numeric* , *string quote* , and *comment character*. Each character can have zero or more of these attributes.

In addition, an instance has four flags. These flags indicate:

- Whether line terminators are to be returned as tokens or treated as white space that merely separates tokens.
- Whether C-style comments are to be recognized and skipped.
- Whether C++-style comments are to be recognized and skipped.
- Whether the characters of identifiers are converted to lowercase.

A typical application first constructs an instance of this class, sets up the syntax tables, and then repeatedly loops calling the `nextToken` method in each iteration of the loop until it returns the value `TT_EOF`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_EOF:kotlin.Int` A constant indicating that the end of the stream has been read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_EOL:kotlin.Int` A constant indicating that the end of the line has been read. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_NUMBER:kotlin.Int` A constant indicating that a number token has been read. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_WORD:kotlin.Int` A constant indicating that a word token has been read. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#StreamTokenizer(java.io.InputStream)(is: https://developer.android.com/reference/kotlin/java/io/InputStream!)` Creates a stream tokenizer that parses the specified input stream. |
| `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#StreamTokenizer(java.io.Reader)(r: https://developer.android.com/reference/kotlin/java/io/Reader!)` Create a tokenizer that parses the given character stream. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#commentChar(kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specified that the character argument starts a single-line comment. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#eolIsSignificant(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Determines whether or not ends of line are treated as tokens. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#lineno()()` Return the current line number. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#lowerCaseMode(kotlin.Boolean)(fl: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Determines whether or not word token are automatically lowercased. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()()` Parses the next token from the input stream of this tokenizer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ordinaryChar(kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies that the character argument is "ordinary" in this tokenizer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ordinaryChars(kotlin.Int,%20kotlin.Int)(low: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies that all characters *c* in the range `low <= c <= high` are "ordinary" in this tokenizer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#parseNumbers()()` Specifies that numbers should be parsed by this tokenizer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#pushBack()()` Causes the next call to the `nextToken` method of this tokenizer to return the current value in the `ttype` field, and not to modify the value in the `nval` or `sval` field. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#quoteChar(kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies that matching pairs of this character delimit string constants in this tokenizer. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#resetSyntax()()` Resets this tokenizer's syntax table so that all characters are "ordinary. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#slashSlashComments(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Determines whether or not the tokenizer recognizes C++-style comments. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#slashStarComments(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Determines whether or not the tokenizer recognizes C-style comments. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#toString()()` Returns the string representation of the current stream token and the line number it occurs on. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#whitespaceChars(kotlin.Int,%20kotlin.Int)(low: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies that all characters *c* in the range `low <= c <= high` are white space characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#wordChars(kotlin.Int,%20kotlin.Int)(low: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, hi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Specifies that all characters *c* in the range `low <= c <= high` are word constituents. |

| Properties ||
|---|---|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nval:kotlin.Double` If the current token is a number, this field contains the value of that number. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#sval:kotlin.String` If the current token is a word token, this field contains a string giving the characters of the word token. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int` After a call to the `nextToken` method, this field contains the type of the token just read. |
| --- | --- |

## Constants

### TT_EOF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TT_EOF: Int
```

A constant indicating that the end of the stream has been read.

 Value: -1

### TT_EOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TT_EOL: Int
```

A constant indicating that the end of the line has been read.

 Value: 10

### TT_NUMBER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TT_NUMBER: Int
```

A constant indicating that a number token has been read.

 Value: -2

### TT_WORD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TT_WORD: Int
```

A constant indicating that a word token has been read.

 Value: -3

## Public constructors

### StreamTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamTokenizer(is: InputStream!)
```

**Deprecated:** *As of JDK version 1.1, the preferred way to tokenize an input stream is to convert it into a character stream, for example:*

```kotlin
Reader r = new BufferedReader(new InputStreamReader(is));
    StreamTokenizer st = new StreamTokenizer(r);
  
```

<br />

Creates a stream tokenizer that parses the specified input stream. The stream tokenizer is initialized to the following default state:

- All byte values `'A'` through `'Z'`, `'a'` through `'z'`, and `'\u005Cu00A0'` through `'\u005Cu00FF'` are considered to be alphabetic.
- All byte values `'\u005Cu0000'` through `'\u005Cu0020'` are considered to be white space.
- `'/'` is a comment character.
- Single quote `'\u005C''` and double quote `'"'` are string quote characters.
- Numbers are parsed.
- Ends of lines are treated as white space, not as separate tokens.
- C-style and C++-style comments are not recognized.

<br />

| Parameters ||
|---|---|
| `is` | [InputStream](InputStream.md)!: an input stream. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/BufferedReader`
- `https://developer.android.com/reference/kotlin/java/io/InputStreamReader`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#StreamTokenizer(java.io.Reader)`

### StreamTokenizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
StreamTokenizer(r: Reader!)
```

Create a tokenizer that parses the given character stream.

| Parameters ||
|---|---|
| `r` | [Reader](Reader.md)!: a Reader object providing the input stream. |

## Public methods

### commentChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun commentChar(ch: Int): Unit
```

Specified that the character argument starts a single-line comment. All characters from the comment character to the end of the line are ignored by this stream tokenizer.

Any other attribute settings for the specified character are cleared.

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character. |

### eolIsSignificant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun eolIsSignificant(flag: Boolean): Unit
```

Determines whether or not ends of line are treated as tokens. If the flag argument is true, this tokenizer treats end of lines as tokens; the `nextToken` method returns `TT_EOL` and also sets the `ttype` field to this value when an end of line is read.

A line is a sequence of characters ending with either a carriage-return character (`'\u005Cr'`) or a newline character (`'\u005Cn'`). In addition, a carriage-return character followed immediately by a newline character is treated as a single end-of-line token.

If the `flag` is false, end-of-line characters are treated as white space and serve only to separate tokens.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` indicates that end-of-line characters are separate tokens; `false` indicates that end-of-line characters are white space. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_EOL:kotlin.Int`

### lineno

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lineno(): Int
```

Return the current line number.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the current line number of this stream tokenizer. |

### lowerCaseMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lowerCaseMode(fl: Boolean): Unit
```

Determines whether or not word token are automatically lowercased. If the flag argument is `true`, then the value in the `sval` field is lowercased whenever a word token is returned (the `ttype` field has the value `TT_WORD` by the `nextToken` method of this tokenizer.

If the flag argument is `false`, then the `sval` field is not modified.

| Parameters ||
|---|---|
| `fl` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` indicates that all word tokens should be lowercased. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_WORD:kotlin.Int`

### nextToken

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextToken(): Int
```

Parses the next token from the input stream of this tokenizer. The type of the next token is returned in the `ttype` field. Additional information about the token may be in the `nval` field or the `sval` field of this tokenizer.

Typical clients of this class first set up the syntax tables and then sit in a loop calling nextToken to parse successive tokens until TT_EOF is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of the `ttype` field. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nval:kotlin.Double`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#sval:kotlin.String`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### ordinaryChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ordinaryChar(ch: Int): Unit
```

Specifies that the character argument is "ordinary" in this tokenizer. It removes any special significance the character has as a comment character, word component, string delimiter, white space, or number character. When such a character is encountered by the parser, the parser treats it as a single-character token and sets `ttype` field to the character value.

Making a line terminator character "ordinary" may interfere with the ability of a `StreamTokenizer` to count lines. The `lineno` method may no longer reflect the presence of such terminator characters in its line count.

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### ordinaryChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun ordinaryChars(
    low: Int, 
    hi: Int
): Unit
```

Specifies that all characters *c* in the range `low <= c <= high` are "ordinary" in this tokenizer. See the `ordinaryChar` method for more information on a character being ordinary.

| Parameters ||
|---|---|
| `low` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the low end of the range. |
| `hi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the high end of the range. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ordinaryChar(kotlin.Int)`

### parseNumbers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun parseNumbers(): Unit
```

Specifies that numbers should be parsed by this tokenizer. The syntax table of this tokenizer is modified so that each of the twelve characters:

```kotlin
0 1 2 3 4 5 6 7 8 9 . -
  
```

<br />

has the "numeric" attribute.

When the parser encounters a word token that has the format of a double precision floating-point number, it treats the token as a number rather than a word, by setting the `ttype` field to the value `TT_NUMBER` and putting the numeric value of the token into the `nval` field.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nval:kotlin.Double`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_NUMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### pushBack

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pushBack(): Unit
```

Causes the next call to the `nextToken` method of this tokenizer to return the current value in the `ttype` field, and not to modify the value in the `nval` or `sval` field.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nval:kotlin.Double`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#sval:kotlin.String`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### quoteChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun quoteChar(ch: Int): Unit
```

Specifies that matching pairs of this character delimit string constants in this tokenizer.

When the `nextToken` method encounters a string constant, the `ttype` field is set to the string delimiter and the `sval` field is set to the body of the string.

If a string quote character is encountered, then a string is recognized, consisting of all characters after (but not including) the string quote character, up to (but not including) the next occurrence of that same string quote character, or a line terminator, or end of file. The usual escape sequences such as `"\u005Cn"` and `"\u005Ct"` are recognized and converted to single characters as the string is parsed.

Any other attribute settings for the specified character are cleared.

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the character. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#sval:kotlin.String`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### resetSyntax

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun resetSyntax(): Unit
```

Resets this tokenizer's syntax table so that all characters are "ordinary." See the `ordinaryChar` method for more information on a character being ordinary.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ordinaryChar(kotlin.Int)`

### slashSlashComments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun slashSlashComments(flag: Boolean): Unit
```

Determines whether or not the tokenizer recognizes C++-style comments. If the flag argument is `true`, this stream tokenizer recognizes C++-style comments. Any occurrence of two consecutive slash characters (`'/'`) is treated as the beginning of a comment that extends to the end of the line.

If the flag argument is `false`, then C++-style comments are not treated specially.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` indicates to recognize and ignore C++-style comments. |

### slashStarComments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun slashStarComments(flag: Boolean): Unit
```

Determines whether or not the tokenizer recognizes C-style comments. If the flag argument is `true`, this stream tokenizer recognizes C-style comments. All text between successive occurrences of `/*` and `*/` are discarded.

If the flag argument is `false`, then C-style comments are not treated specially.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` indicates to recognize and ignore C-style comments. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the string representation of the current stream token and the line number it occurs on.

The precise string returned is unspecified, although the following example can be considered typical:

```kotlin
Token['a'], line 10
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the token |

**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nval:kotlin.Double`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#sval:kotlin.String`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### whitespaceChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun whitespaceChars(
    low: Int, 
    hi: Int
): Unit
```

Specifies that all characters *c* in the range `low <= c <= high` are white space characters. White space characters serve only to separate tokens in the input stream.

Any other attribute settings for the characters in the specified range are cleared.

| Parameters ||
|---|---|
| `low` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the low end of the range. |
| `hi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the high end of the range. |

### wordChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun wordChars(
    low: Int, 
    hi: Int
): Unit
```

Specifies that all characters *c* in the range `low <= c <= high` are word constituents. A word token consists of a word constituent followed by zero or more word constituents or number constituents.

| Parameters ||
|---|---|
| `low` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the low end of the range. |
| `hi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the high end of the range. |

## Properties

### nval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var nval: Double
```

If the current token is a number, this field contains the value of that number. The current token is a number when the value of the `ttype` field is `TT_NUMBER`.

The initial value of this field is 0.0.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_NUMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### sval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var sval: String!
```

If the current token is a word token, this field contains a string giving the characters of the word token. When the current token is a quoted string token, this field contains the body of the string.

The current token is a word when the value of the `ttype` field is `TT_WORD`. The current token is a quoted string token when the value of the `ttype` field is a quote character.

The initial value of this field is null.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#quoteChar(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_WORD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#ttype:kotlin.Int`

### ttype

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var ttype: Int
```

After a call to the `nextToken` method, this field contains the type of the token just read. For a single character token, its value is the single character, converted to an integer. For a quoted string token, its value is the quote character. Otherwise, its value is one of the following:

- `TT_WORD` indicates that the token is a word.
- `TT_NUMBER` indicates that the token is a number.
- `TT_EOL` indicates that the end of line has been read. The field can only have this value if the `eolIsSignificant` method has been called with the argument `true`.
- `TT_EOF` indicates that the end of the input stream has been reached.

<br />

The initial value of this field is -4.
**See Also**

- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#eolIsSignificant(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#nextToken()`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#quoteChar(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_EOF:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_EOL:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_NUMBER:kotlin.Int`
- `https://developer.android.com/reference/kotlin/java/io/StreamTokenizer#TT_WORD:kotlin.Int`
