Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Scanner

```
class Scanner : Closeable, MutableIterator<String!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.Scanner](Scanner.md) |

A simple text scanner which can parse primitive types and strings using regular expressions.

A `Scanner` breaks its input into tokens using a delimiter pattern, which by default matches whitespace. The resulting tokens may then be converted into values of different types using the various `next` methods.

For example, this code allows a user to read a number from `System.in`:

```kotlin
<code>Scanner sc = new Scanner(System.in);
      int i = sc.nextInt();
  </code>
```

As another example, this code allows `long` types to be assigned from entries in a file `myNumbers`:

```kotlin
<code>Scanner sc = new Scanner(new File("myNumbers"));
       while (sc.hasNextLong()) {
           long aLong = sc.nextLong();
       }
  </code>
```

The scanner can also use delimiters other than whitespace. This example reads several items in from a string:

```kotlin
<code>String input = "1 fish 2 fish red fish blue fish";
      Scanner s = new Scanner(input).useDelimiter("\\s*fish\\s*");
      System.out.println(s.nextInt());
      System.out.println(s.nextInt());
      System.out.println(s.next());
      System.out.println(s.next());
      s.close();
  </code>
```

prints the following output:

```kotlin
<code>1
      2
      red
      blue
  </code>
```

The same output can be generated with this code, which uses a regular expression to parse all four tokens at once:

```kotlin
<code>String input = "1 fish 2 fish red fish blue fish";
      Scanner s = new Scanner(input);
      s.findInLine("(\\d+) fish (\\d+) fish (\\w+) fish (\\w+)");
      MatchResult result = s.match();
      for (int i=1; i&lt;=result.groupCount(); i++)
          System.out.println(result.group(i));
      s.close();
  </code>
```

The default whitespace delimiter used by a scanner is as recognized by isWhitespace. The reset method will reset the value of the scanner's delimiter to the default whitespace delimiter regardless of whether it was previously changed.

A scanning operation may block waiting for input.

The #next and #hasNext methods and their companion methods (such as #nextInt and #hasNextInt) first skip any input that matches the delimiter pattern, and then attempt to return the next token. Both `hasNext()` and `next()` methods may block waiting for further input. Whether a `hasNext()` method blocks has no connection to whether or not its associated `next()` method will block. The tokens method may also block waiting for input.

The #findInLine, #findWithinHorizon, #skip, and #findAll methods operate independently of the delimiter pattern. These methods will attempt to match the specified pattern with no regard to delimiters in the input and thus can be used in special circumstances where delimiters are not relevant. These methods may block waiting for more input.

When a scanner throws an InputMismatchException, the scanner will not pass the token that caused the exception, so that it may be retrieved or skipped via some other method.

Depending upon the type of delimiting pattern, empty tokens may be returned. For example, the pattern `"\\s+"` will return no empty tokens since it matches multiple instances of the delimiter. The delimiting pattern `"\\s"` could return empty tokens since it only passes one space at a time.

A scanner can read text from any object which implements the `https://developer.android.com/reference/kotlin/java/lang/Readable.html#` interface. If an invocation of the underlying readable's read method throws an `https://developer.android.com/reference/kotlin/java/io/IOException.html#` then the scanner assumes that the end of the input has been reached. The most recent `IOException` thrown by the underlying readable can be retrieved via the ioException method.

When a `Scanner` is closed, it will close its input source if the source implements the `https://developer.android.com/reference/kotlin/java/io/Closeable.html#` interface.

A `Scanner` is not safe for multithreaded use without external synchronization.

Unless otherwise mentioned, passing a `null` parameter into any method of a `Scanner` will cause a `NullPointerException` to be thrown.

A scanner will default to interpreting numbers as decimal unless a different radix has been set by using the useRadix method. The reset method will reset the value of the scanner's radix to `10` regardless of whether it was previously changed.

## Localized numbers

An instance of this class is capable of scanning numbers in the standard formats as well as in the formats of the scanner's locale. A scanner's initial locale is the value returned by the getDefault method; it may be changed via the useLocale method. The reset method will reset the value of the scanner's locale to the initial locale regardless of whether it was previously changed.

The localized formats are defined in terms of the following parameters, which for a particular locale are taken from that locale's `https://developer.android.com/reference/kotlin/java/text/DecimalFormat.html#` object, `df`, and its and `https://developer.android.com/reference/kotlin/java/text/DecimalFormatSymbols.html#` object, `dfs`.

*LocalGroupSeparator*
: The character used to separate thousands groups, *i.e.,* `dfs.`getGroupingSeparator

*LocalDecimalSeparator*
: The character used for the decimal point, *i.e.,* `dfs.`getDecimalSeparator

*LocalPositivePrefix*
: The string that appears before a positive number (may be empty), *i.e.,* `df.`getPositivePrefix

*LocalPositiveSuffix*
: The string that appears after a positive number (may be empty), *i.e.,* `df.`getPositiveSuffix

*LocalNegativePrefix*
: The string that appears before a negative number (may be empty), *i.e.,* `df.`getNegativePrefix

*LocalNegativeSuffix*
: The string that appears after a negative number (may be empty), *i.e.,* `df.`getNegativeSuffix

*LocalNaN*
: The string that represents not-a-number for floating-point values, *i.e.,* `dfs.`getNaN

*LocalInfinity*
: The string that represents infinity for floating-point values, *i.e.,* `dfs.`getInfinity

### Number syntax

The strings that can be parsed as numbers by an instance of this class are specified in terms of the following regular-expression grammar, where Rmax is the highest digit in the radix being used (for example, Rmax is 9 in base 10).

*NonAsciiDigit*:
: A non-ASCII character c for which java.lang.Character#isDigit`(c)` returns true

*Non0Digit*:
: `[1-`*Rmax* `] | `*NonASCIIDigit*
| --- | --- |

*Digit*:
: `[0-`*Rmax* `] | `*NonASCIIDigit*
| --- | --- |

*GroupedNumeral*:
: `( `*Non0Digit* *Digit* `? `*Digit* `?`
: `( `*LocalGroupSeparator* *Digit* *Digit* *Digit* `)+ )`

*Numeral*:
: `( ( `*Digit* `+ ) | `*GroupedNumeral* `)`
| --- | --- |

*Integer*:
: `( [-+]? ( `*Numeral* `) )`
: `| `*LocalPositivePrefix* *Numeral* *LocalPositiveSuffix*
| --- | --- |
: `| `*LocalNegativePrefix* *Numeral* *LocalNegativeSuffix*

*DecimalNumeral*:
: *Numeral*
: `| `*Numeral* *LocalDecimalSeparator* *Digit* `*`
| --- | --- |
: `| `*LocalDecimalSeparator* *Digit* `+`

*Exponent*:
: `( [eE] [+-]? `*Digit* `+ )`

*Decimal*:
: `( [-+]? `*DecimalNumeral* *Exponent* `? )`
: `| `*LocalPositivePrefix* *DecimalNumeral* *LocalPositiveSuffix* *Exponent* `?`
| --- | --- |
: `| `*LocalNegativePrefix* *DecimalNumeral* *LocalNegativeSuffix* *Exponent* `?`

*HexFloat*:
: `[-+]? 0[xX][0-9a-fA-F]*\.[0-9a-fA-F]+ ([pP][-+]?[0-9]+)?`

*NonNumber*:
: `NaN | `*LocalNan* `| Infinity | `*LocalInfinity*
| --- | --- | --- | --- |

*SignedNonNumber*:
: `( [-+]? `*NonNumber* `)`
: `| `*LocalPositivePrefix* *NonNumber* *LocalPositiveSuffix*
| --- | --- |
: `| `*LocalNegativePrefix* *NonNumber* *LocalNegativeSuffix*

*Float*:
: *Decimal* `| `*HexFloat* `| `*SignedNonNumber*
| --- | --- | --- |

Whitespace is not significant in the above regular expressions.

## Summary

| Public constructors ||
|---|---|
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified input stream. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified input stream. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified input stream. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified source. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified string. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified channel. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified channel. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified channel. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |
| Scanner Constructs a new `Scanner` that produces values scanned from the specified file. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes this scanner. |
| [Pattern](../java.util.regex/Pattern.md)! | delimiter Returns the `Pattern` this `Scanner` is currently using to match delimiters. |
| [Stream](../java.util.stream/Stream.md)\< [MatchResult](../java.util.regex/MatchResult.md)!\>! | findAll Returns a stream of match results that match the provided pattern string. |
| --- | --- |
| [Stream](../java.util.stream/Stream.md)\< [MatchResult](../java.util.regex/MatchResult.md)!\>! | findAll Returns a stream of match results from this scanner. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | findInLine Attempts to find the next occurrence of a pattern constructed from the specified string, ignoring delimiters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | findInLine Attempts to find the next occurrence of the specified pattern ignoring delimiters. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | findWithinHorizon Attempts to find the next occurrence of a pattern constructed from the specified string, ignoring delimiters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | findWithinHorizon Attempts to find the next occurrence of the specified pattern. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNext Returns true if this scanner has another token in its input. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNext Returns true if the next token matches the pattern constructed from the specified string. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNext Returns true if the next complete token matches the specified pattern. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextBigDecimal Returns true if the next token in this scanner's input can be interpreted as a `BigDecimal` using the nextBigDecimal method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextBigInteger Returns true if the next token in this scanner's input can be interpreted as a `BigInteger` in the default radix using the #nextBigInteger method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextBigInteger Returns true if the next token in this scanner's input can be interpreted as a `BigInteger` in the specified radix using the #nextBigInteger method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextBoolean Returns true if the next token in this scanner's input can be interpreted as a boolean value using a case insensitive pattern created from the string "true|false". |
| --- | --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextByte Returns true if the next token in this scanner's input can be interpreted as a byte value in the default radix using the #nextByte method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextByte Returns true if the next token in this scanner's input can be interpreted as a byte value in the specified radix using the #nextByte method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextDouble Returns true if the next token in this scanner's input can be interpreted as a double value using the nextDouble method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextFloat Returns true if the next token in this scanner's input can be interpreted as a float value using the nextFloat method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextInt Returns true if the next token in this scanner's input can be interpreted as an int value in the default radix using the #nextInt method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextInt Returns true if the next token in this scanner's input can be interpreted as an int value in the specified radix using the #nextInt method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextLine Returns true if there is another line in the input of this scanner. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextLong Returns true if the next token in this scanner's input can be interpreted as a long value in the default radix using the #nextLong method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextLong Returns true if the next token in this scanner's input can be interpreted as a long value in the specified radix using the #nextLong method. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextShort Returns true if the next token in this scanner's input can be interpreted as a short value in the default radix using the #nextShort method. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasNextShort Returns true if the next token in this scanner's input can be interpreted as a short value in the specified radix using the #nextShort method. |
| [IOException](../java.io/IOException.md)! | ioException Returns the `IOException` last thrown by this `Scanner`'s underlying `Readable`. |
| --- | --- |
| [Locale](Locale.md)! | locale Returns this scanner's locale. |
| [MatchResult](../java.util.regex/MatchResult.md)! | match Returns the match result of the last scanning operation performed by this scanner. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | next Finds and returns the next complete token from this scanner. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | next Returns the next token if it matches the pattern constructed from the specified string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | next Returns the next token if it matches the specified pattern. |
| [BigDecimal](../java.math/BigDecimal.md)! | nextBigDecimal Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#`. |
| --- | --- |
| [BigInteger](../java.math/BigInteger.md)! | nextBigInteger Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#`. |
| [BigInteger](../java.math/BigInteger.md)! | nextBigInteger Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | nextBoolean Scans the next token of the input into a boolean value and returns that value. |
| --- | --- |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | nextByte Scans the next token of the input as a `byte`. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | nextByte Scans the next token of the input as a `byte`. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | nextDouble Scans the next token of the input as a `double`. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | nextFloat Scans the next token of the input as a `float`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | nextInt Scans the next token of the input as an `int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | nextInt Scans the next token of the input as an `int`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | nextLine Advances this scanner past the current line and returns the input that was skipped. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | nextLong Scans the next token of the input as a `long`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | nextLong Scans the next token of the input as a `long`. |
| --- | --- |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | nextShort Scans the next token of the input as a `short`. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | nextShort Scans the next token of the input as a `short`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | radix Returns this scanner's default radix. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | remove The remove operation is not supported by this implementation of `Iterator`. |
| [Scanner](Scanner.md)! | reset Resets this scanner. |
| [Scanner](Scanner.md)! | skip Skips input that matches a pattern constructed from the specified string. |
| --- | --- |
| [Scanner](Scanner.md)! | skip Skips input that matches the specified pattern, ignoring delimiters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns the string representation of this `Scanner`. |
| [Stream](../java.util.stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | tokens Returns a stream of delimiter-separated tokens from this scanner. |
| --- | --- |
| [Scanner](Scanner.md)! | useDelimiter Sets this scanner's delimiting pattern to a pattern constructed from the specified `String`. |
| [Scanner](Scanner.md)! | useDelimiter Sets this scanner's delimiting pattern to the specified pattern. |
| [Scanner](Scanner.md)! | useLocale Sets this scanner's locale to the specified locale. |
| --- | --- |
| [Scanner](Scanner.md)! | useRadix Sets this scanner's default radix to the specified radix. |

## Public constructors

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: File!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the underlying platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|---|---|
| `source` | [File](../java.io/File.md)!: A file to be scanned |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if source is not found |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: File!, 
    charsetName: String!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [File](../java.io/File.md)!: A file to be scanned |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The encoding type used to convert bytes from the file into characters to be scanned |

| Exceptions ||
|---|---|
| `java.io.FileNotFoundException` | if source is not found |
| `java.lang.IllegalArgumentException` | if the specified encoding is not found |

### Scanner

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: File!, 
    charset: Charset!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [File](../java.io/File.md)!: A file to be scanned |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: The charset used to convert bytes from the file into characters to be scanned |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs opening the source |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: InputStream!)
```

Constructs a new `Scanner` that produces values scanned from the specified input stream. Bytes from the stream are converted into characters using the underlying platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|---|---|
| `source` | [InputStream](../java.io/InputStream.md)!: An input stream to be scanned |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: InputStream!, 
    charsetName: String!)
```

Constructs a new `Scanner` that produces values scanned from the specified input stream. Bytes from the stream are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [InputStream](../java.io/InputStream.md)!: An input stream to be scanned |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The encoding type used to convert bytes from the stream into characters to be scanned |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified character set does not exist |

### Scanner

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: InputStream!, 
    charset: Charset!)
```

Constructs a new `Scanner` that produces values scanned from the specified input stream. Bytes from the stream are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [InputStream](../java.io/InputStream.md)!: an input stream to be scanned |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: the charset used to convert bytes from the file into characters to be scanned |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: Readable!)
```

Constructs a new `Scanner` that produces values scanned from the specified source.

| Parameters ||
|---|---|
| `source` | [Readable](../java.lang/Readable.md)!: A character source implementing the `https://developer.android.com/reference/kotlin/java/lang/Readable.html#` interface |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: String!)
```

Constructs a new `Scanner` that produces values scanned from the specified string.

| Parameters ||
|---|---|
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string to scan |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: ReadableByteChannel!)
```

Constructs a new `Scanner` that produces values scanned from the specified channel. Bytes from the source are converted into characters using the underlying platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|---|---|
| `source` | [ReadableByteChannel](../java.nio.channels/ReadableByteChannel.md)!: A channel to scan |

### Scanner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: ReadableByteChannel!, 
    charsetName: String!)
```

Constructs a new `Scanner` that produces values scanned from the specified channel. Bytes from the source are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [ReadableByteChannel](../java.nio.channels/ReadableByteChannel.md)!: A channel to scan |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The encoding type used to convert bytes from the channel into characters to be scanned |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the specified character set does not exist |

### Scanner

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: ReadableByteChannel!, 
    charset: Charset!)
```

Constructs a new `Scanner` that produces values scanned from the specified channel. Bytes from the source are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [ReadableByteChannel](../java.nio.channels/ReadableByteChannel.md)!: a channel to scan |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: the encoding type used to convert bytes from the channel into characters to be scanned |

### Scanner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(source: Path!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the underlying platform's [default charset](../java.nio.charset/Charset.md)).

| Parameters ||
|---|---|
| `source` | [Path](../java.nio.file/Path.md)!: the path to the file to be scanned |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs opening source |

### Scanner

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: Path!, 
    charsetName: String!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [Path](../java.nio.file/Path.md)!: the path to the file to be scanned |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The encoding type used to convert bytes from the file into characters to be scanned |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs opening source |
| `java.lang.IllegalArgumentException` | if the specified encoding is not found |

### Scanner

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Scanner(
    source: Path!, 
    charset: Charset!)
```

Constructs a new `Scanner` that produces values scanned from the specified file. Bytes from the file are converted into characters using the specified charset.

| Parameters ||
|---|---|
| `source` | [Path](../java.nio.file/Path.md)!: the path to the file to be scanned |
| `charset` | [Charset](../java.nio.charset/Charset.md)!: the charset used to convert bytes from the file into characters to be scanned |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs opening the source |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this scanner.

If this scanner has not yet been closed then if its underlying [readable](../java.lang/Readable.md) also implements the `https://developer.android.com/reference/kotlin/java/io/Closeable.html#` interface then the readable's `close` method will be invoked. If this scanner is already closed then invoking this method will have no effect.

Attempting to perform search operations after a scanner has been closed will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### delimiter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun delimiter(): Pattern!
```

Returns the `Pattern` this `Scanner` is currently using to match delimiters.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/regex/Pattern!` | this scanner's delimiting pattern. |

### findAll

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findAll(patString: String!): Stream<MatchResult!>!
```

Returns a stream of match results that match the provided pattern string. The effect is equivalent to the following code:

```kotlin
<code>scanner.findAll(Pattern.compile(patString))
  </code>
```

<br />

| Parameters ||
|---|---|
| `patString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the pattern string |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream<https://developer.android.com/reference/kotlin/java/util/regex/MatchResult!>!` | a sequential stream of match results |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.lang.NullPointerException` | if patString is null |
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |
| --- | --- |

**See Also**

- Pattern

### findAll

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findAll(pattern: Pattern!): Stream<MatchResult!>!
```

Returns a stream of match results from this scanner. The stream contains the same results in the same order that would be returned by calling `findWithinHorizon(pattern, 0)` and then match successively as long as #findWithinHorizon finds matches.

The resulting stream is sequential and ordered. All stream elements are non-null.

Scanning starts upon initiation of the terminal stream operation, using the current state of this scanner. Subsequent calls to any methods on this scanner other than #close and ioException may return undefined results or may cause undefined effects on the returned stream. The returned stream's source `Spliterator` is *fail-fast* and will, on a best-effort basis, throw a ConcurrentModificationException if any such calls are detected during stream pipeline execution.

After stream pipeline execution completes, this scanner is left in an indeterminate state and cannot be reused.

If this scanner contains a resource that must be released, this scanner should be closed, either by calling its #close method, or by closing the returned stream. Closing the stream will close the underlying scanner. `IllegalStateException` is thrown if the scanner has been closed when this method is called, or if this scanner is closed during stream pipeline execution.

As with the #findWithinHorizon methods, this method might block waiting for additional input, and it might buffer an unbounded amount of input searching for a match.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: the pattern to be matched |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream<https://developer.android.com/reference/kotlin/java/util/regex/MatchResult!>!` | a sequential stream of match results |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.lang.NullPointerException` | if pattern is null |

### findInLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findInLine(pattern: String!): String!
```

Attempts to find the next occurrence of a pattern constructed from the specified string, ignoring delimiters.

An invocation of this method of the form `findInLine(pattern)` behaves in exactly the same way as the invocation `findInLine(Pattern.compile(pattern))`.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying the pattern to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text that matched the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### findInLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findInLine(pattern: Pattern!): String!
```

Attempts to find the next occurrence of the specified pattern ignoring delimiters. If the pattern is found before the next line separator, the scanner advances past the input that matched and returns the string that matched the pattern. If no such pattern is detected in the input up to the next line separator, then `null` is returned and the scanner's position is unchanged. This method may block waiting for input that matches the pattern.

Since this method continues to search through the input looking for the specified pattern, it may buffer all of the input searching for the desired token if no line separators are present.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: the pattern to scan for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text that matched the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### findWithinHorizon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findWithinHorizon(
    pattern: String!, 
    horizon: Int
): String!
```

Attempts to find the next occurrence of a pattern constructed from the specified string, ignoring delimiters.

An invocation of this method of the form `findWithinHorizon(pattern)` behaves in exactly the same way as the invocation `findWithinHorizon(Pattern.compile(pattern), horizon)`.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying the pattern to search for |
| `horizon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the search horizon |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text that matched the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if horizon is negative |
| `java.lang.IllegalStateException` | if this scanner is closed |

### findWithinHorizon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun findWithinHorizon(
    pattern: Pattern!, 
    horizon: Int
): String!
```

Attempts to find the next occurrence of the specified pattern.

This method searches through the input up to the specified search horizon, ignoring delimiters. If the pattern is found the scanner advances past the input that matched and returns the string that matched the pattern. If no such pattern is detected then the null is returned and the scanner's position remains unchanged. This method may block waiting for input that matches the pattern.

A scanner will never search more than `horizon` code points beyond its current position. Note that a match may be clipped by the horizon; that is, an arbitrary match result may have been different if the horizon had been larger. The scanner treats the horizon as a transparent, non-anchoring bound (see useTransparentBounds and useAnchoringBounds).

If horizon is `0`, then the horizon is ignored and this method continues to search through the input looking for the specified pattern without bound. In this case it may buffer all of the input searching for the pattern.

If horizon is negative, then an IllegalArgumentException is thrown.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: the pattern to scan for |
| `horizon` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the search horizon |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the text that matched the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if horizon is negative |
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNext(): Boolean
```

Returns true if this scanner has another token in its input. This method may block while waiting for input to scan. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner has another token |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

**See Also**

- Iterator

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNext(pattern: String!): Boolean
```

Returns true if the next token matches the pattern constructed from the specified string. The scanner does not advance past any input.

An invocation of this method of the form `hasNext(pattern)` behaves in exactly the same way as the invocation `hasNext(Pattern.compile(pattern))`.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying the pattern to scan |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner has another token matching the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNext(pattern: Pattern!): Boolean
```

Returns true if the next complete token matches the specified pattern. A complete token is prefixed and postfixed by input that matches the delimiter pattern. This method may block while waiting for input. The scanner does not advance past any input.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: the pattern to scan for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner has another token matching the specified pattern |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextBigDecimal(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a `BigDecimal` using the nextBigDecimal method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid `BigDecimal` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextBigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextBigInteger(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a `BigInteger` in the default radix using the #nextBigInteger method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid `BigInteger` |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextBigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextBigInteger(radix: Int): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a `BigInteger` in the specified radix using the #nextBigInteger method. The scanner does not advance past any input.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as an integer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid `BigInteger` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextBoolean(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a boolean value using a case insensitive pattern created from the string "true|false". The scanner does not advance past the input that matched.
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid boolean value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextByte(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a byte value in the default radix using the #nextByte method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid byte value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextByte(radix: Int): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a byte value in the specified radix using the #nextByte method. The scanner does not advance past any input.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as a byte value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid byte value |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextDouble(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a double value using the nextDouble method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid double value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextFloat(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a float value using the nextFloat method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid float value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextInt(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as an int value in the default radix using the #nextInt method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid int value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextInt(radix: Int): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as an int value in the specified radix using the #nextInt method. The scanner does not advance past any input.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as an int value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid int value |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextLine(): Boolean
```

Returns true if there is another line in the input of this scanner. This method may block while waiting for input. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner has another line of input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextLong(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a long value in the default radix using the #nextLong method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid long value |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextLong(radix: Int): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a long value in the specified radix using the #nextLong method. The scanner does not advance past any input.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as a long value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid long value |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextShort(): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a short value in the default radix using the #nextShort method. The scanner does not advance past any input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid short value in the default radix |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### hasNextShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasNextShort(radix: Int): Boolean
```

Returns true if the next token in this scanner's input can be interpreted as a short value in the specified radix using the #nextShort method. The scanner does not advance past any input.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as a short value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this scanner's next token is a valid short value in the specified radix |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |

### ioException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun ioException(): IOException!
```

Returns the `IOException` last thrown by this `Scanner`'s underlying `Readable`. This method returns `null` if no such exception exists.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/IOException.html#!` | the last exception thrown by this scanner's readable |

### locale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun locale(): Locale!
```

Returns this scanner's locale.

A scanner's locale affects many elements of its default primitive matching regular expressions; see [localized numbers](Scanner.md) above.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Locale!` | this scanner's locale |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun match(): MatchResult!
```

Returns the match result of the last scanning operation performed by this scanner. This method throws `IllegalStateException` if no match has been performed, or if the last match was not successful.

The various `next` methods of `Scanner` make a match result available if they complete without throwing an exception. For instance, after an invocation of the #nextInt method that returned an int, this method returns a `MatchResult` for the search of the [*Integer*](Scanner.md) regular expression defined above. Similarly the #findInLine, #findWithinHorizon, and #skip methods will make a match available if they succeed.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/regex/MatchResult!` | a match result for the last match operation |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If no match result is available |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun next(): String!
```

Finds and returns the next complete token from this scanner. A complete token is preceded and followed by input that matches the delimiter pattern. This method may block while waiting for input to scan, even if a previous invocation of #hasNext returned `true`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the next token |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if no more tokens are available |
| `java.lang.IllegalStateException` | if this scanner is closed |

**See Also**

- Iterator

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun next(pattern: String!): String!
```

Returns the next token if it matches the pattern constructed from the specified string. If the match is successful, the scanner advances past the input that matched the pattern.

An invocation of this method of the form `next(pattern)` behaves in exactly the same way as the invocation `next(Pattern.compile(pattern))`.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying the pattern to scan |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the next token |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.NoSuchElementException` | if no such tokens are available |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun next(pattern: Pattern!): String!
```

Returns the next token if it matches the specified pattern. This method may block while waiting for input to scan, even if a previous invocation of hasNext returned `true`. If the match is successful, the scanner advances past the input that matched the pattern.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: the pattern to scan for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the next token |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.NoSuchElementException` | if no more tokens are available |

### nextBigDecimal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextBigDecimal(): BigDecimal!
```

Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#`.

If the next token matches the [*Decimal*](Scanner.md) regular expression defined above then the token is converted into a `BigDecimal` value as if by removing all group separators, mapping non-ASCII digits into ASCII digits via the java.lang.Character#digit, and passing the resulting string to the BigDecimal constructor.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigDecimal.html#!` | the `BigDecimal` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Decimal* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if the input is exhausted |
| --- | --- |

### nextBigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextBigInteger(): BigInteger!
```

Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#`.

An invocation of this method of the form `nextBigInteger()` behaves in exactly the same way as the invocation `nextBigInteger(radix)`, where `radix` is the default radix of this scanner.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | the `BigInteger` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if the input is exhausted |
| --- | --- |

### nextBigInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextBigInteger(radix: Int): BigInteger!
```

Scans the next token of the input as a `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#`.

If the next token matches the [*Integer*](Scanner.md) regular expression defined above then the token is converted into a `BigInteger` value as if by removing all group separators, mapping non-ASCII digits into ASCII digits via the java.lang.Character#digit, and passing the resulting string to the BigInteger constructor with the specified radix.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | the `BigInteger` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| --- | --- |
| `java.util.NoSuchElementException` | if the input is exhausted |

### nextBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextBoolean(): Boolean
```

Scans the next token of the input into a boolean value and returns that value. This method will throw `InputMismatchException` if the next token cannot be translated into a valid boolean value. If the match is successful, the scanner advances past the input that matched.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the boolean scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token is not a valid boolean |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextByte(): Byte
```

Scans the next token of the input as a `byte`.

An invocation of this method of the form `nextByte()` behaves in exactly the same way as the invocation `nextByte(radix)`, where `radix` is the default radix of this scanner.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the `byte` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextByte(radix: Int): Byte
```

Scans the next token of the input as a `byte`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid byte value as described below. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Integer*](Scanner.md) regular expression defined above then the token is converted into a `byte` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseByte with the specified radix.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as a byte value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html` | the `byte` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| --- | --- |
| `java.util.NoSuchElementException` | if input is exhausted |

### nextDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextDouble(): Double
```

Scans the next token of the input as a `double`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid double value. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Float*](Scanner.md) regular expression defined above then the token is converted into a `double` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseDouble. If the token matches the localized NaN or infinity strings, then either "Nan" or "Infinity" is passed to parseDouble as appropriate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the `double` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Float* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if the input is exhausted |
| --- | --- |

### nextFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextFloat(): Float
```

Scans the next token of the input as a `float`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid float value as described below. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Float*](Scanner.md) regular expression defined above then the token is converted into a `float` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseFloat. If the token matches the localized NaN or infinity strings, then either "Nan" or "Infinity" is passed to parseFloat as appropriate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the `float` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Float* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextInt(): Int
```

Scans the next token of the input as an `int`.

An invocation of this method of the form `nextInt()` behaves in exactly the same way as the invocation `nextInt(radix)`, where `radix` is the default radix of this scanner.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the `int` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextInt(radix: Int): Int
```

Scans the next token of the input as an `int`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid int value as described below. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Integer*](Scanner.md) regular expression defined above then the token is converted into an `int` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseInt with the specified radix.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as an int value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the `int` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| --- | --- |
| `java.util.NoSuchElementException` | if input is exhausted |

### nextLine

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextLine(): String!
```

Advances this scanner past the current line and returns the input that was skipped. This method returns the rest of the current line, excluding any line separator at the end. The position is set to the beginning of the next line.

Since this method continues to search through the input looking for a line separator, it may buffer all of the input searching for the line to skip if no line separators are present.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the line that was skipped |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.NoSuchElementException` | if no line was found |

### nextLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextLong(): Long
```

Scans the next token of the input as a `long`.

An invocation of this method of the form `nextLong()` behaves in exactly the same way as the invocation `nextLong(radix)`, where `radix` is the default radix of this scanner.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the `long` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextLong(radix: Int): Long
```

Scans the next token of the input as a `long`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid long value as described below. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Integer*](Scanner.md) regular expression defined above then the token is converted into a `long` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseLong with the specified radix.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as an int value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the `long` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| --- | --- |
| `java.util.NoSuchElementException` | if input is exhausted |

### nextShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextShort(): Short
```

Scans the next token of the input as a `short`.

An invocation of this method of the form `nextShort()` behaves in exactly the same way as the invocation nextShort, where `radix` is the default radix of this scanner.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the `short` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| `java.util.NoSuchElementException` | if input is exhausted |
| --- | --- |

### nextShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun nextShort(radix: Int): Short
```

Scans the next token of the input as a `short`. This method will throw `InputMismatchException` if the next token cannot be translated into a valid short value as described below. If the translation is successful, the scanner advances past the input that matched.

If the next token matches the [*Integer*](Scanner.md) regular expression defined above then the token is converted into a `short` value as if by removing all locale specific prefixes, group separators, and locale specific suffixes, then mapping non-ASCII digits into ASCII digits via java.lang.Character#digit, prepending a negative sign (-) if the locale specific negative prefixes and suffixes were present, and passing the resulting string to parseShort with the specified radix.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the radix used to interpret the token as a short value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the `short` scanned from the input |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the radix is out of range |
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.InputMismatchException` | if the next token does not match the *Integer* regular expression, or is out of range |
| --- | --- |
| `java.util.NoSuchElementException` | if input is exhausted |

### radix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun radix(): Int
```

Returns this scanner's default radix.

A scanner's radix affects elements of its default number matching regular expressions; see [localized numbers](Scanner.md) above.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the default radix of this scanner |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun remove(): Unit
```

The remove operation is not supported by this implementation of `Iterator`.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the `next` method has not yet been called, or the `remove` method has already been called after the last call to the `next` method |
| `java.lang.UnsupportedOperationException` | if this method is invoked. |

**See Also**

- Iterator

### reset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reset(): Scanner!
```

Resets this scanner.

Resetting a scanner discards all of its explicit state information which may have been changed by invocations of #useDelimiter, useLocale, or useRadix.

An invocation of this method of the form `scanner.reset()` behaves in exactly the same way as the invocation

```kotlin
<code>scanner.useDelimiter("\\p{javaWhitespace}+")
           .useLocale(Locale.getDefault(Locale.Category.FORMAT))
           .useRadix(10);
  </code>
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun skip(pattern: String!): Scanner!
```

Skips input that matches a pattern constructed from the specified string.

An invocation of this method of the form `skip(pattern)` behaves in exactly the same way as the invocation `skip(Pattern.compile(pattern))`.

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a string specifying the pattern to skip over |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### skip

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun skip(pattern: Pattern!): Scanner!
```

Skips input that matches the specified pattern, ignoring delimiters. This method will skip input if an anchored match of the specified pattern succeeds.

If a match to the specified pattern is not found at the current position, then no input is skipped and a `NoSuchElementException` is thrown.

Since this method seeks to match the specified pattern starting at the scanner's current position, patterns that can match a lot of input (".\*", for example) may cause the scanner to buffer a large amount of input.

Note that it is possible to skip something without risking a `NoSuchElementException` by using a pattern that can match nothing, e.g., `sc.skip("[ \t]*")`.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: a string specifying the pattern to skip over |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |
| `java.util.NoSuchElementException` | if the specified pattern is not found |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns the string representation of this `Scanner`. The string representation of a `Scanner` contains information that may be useful for debugging. The exact format is unspecified.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The string representation of this scanner |

### tokens

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun tokens(): Stream<String!>!
```

Returns a stream of delimiter-separated tokens from this scanner. The stream contains the same tokens that would be returned, starting from this scanner's current state, by calling the #next method repeatedly until the #hasNext method returns false.

The resulting stream is sequential and ordered. All stream elements are non-null.

Scanning starts upon initiation of the terminal stream operation, using the current state of this scanner. Subsequent calls to any methods on this scanner other than #close and ioException may return undefined results or may cause undefined effects on the returned stream. The returned stream's source `Spliterator` is *fail-fast* and will, on a best-effort basis, throw a ConcurrentModificationException if any such calls are detected during stream pipeline execution.

After stream pipeline execution completes, this scanner is left in an indeterminate state and cannot be reused.

If this scanner contains a resource that must be released, this scanner should be closed, either by calling its #close method, or by closing the returned stream. Closing the stream will close the underlying scanner. `IllegalStateException` is thrown if the scanner has been closed when this method is called, or if this scanner is closed during stream pipeline execution.

This method might block waiting for more input.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | a sequential stream of token strings |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this scanner is closed |

### useDelimiter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun useDelimiter(pattern: String!): Scanner!
```

Sets this scanner's delimiting pattern to a pattern constructed from the specified `String`.

An invocation of this method of the form `useDelimiter(pattern)` behaves in exactly the same way as the invocation `useDelimiter(Pattern.compile(pattern))`.

Invoking the reset method will set the scanner's delimiter to the [default](Scanner.md).

| Parameters ||
|---|---|
| `pattern` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: A string specifying a delimiting pattern |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

### useDelimiter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun useDelimiter(pattern: Pattern!): Scanner!
```

Sets this scanner's delimiting pattern to the specified pattern.

| Parameters ||
|---|---|
| `pattern` | [Pattern](../java.util.regex/Pattern.md)!: A delimiting pattern |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

### useLocale

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun useLocale(locale: Locale!): Scanner!
```

Sets this scanner's locale to the specified locale.

A scanner's locale affects many elements of its default primitive matching regular expressions; see [localized numbers](Scanner.md) above.

Invoking the reset method will set the scanner's locale to the [initial locale](Scanner.md).

| Parameters ||
|---|---|
| `locale` | [Locale](Locale.md)!: A string specifying the locale to use |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

### useRadix

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun useRadix(radix: Int): Scanner!
```

Sets this scanner's default radix to the specified radix.

A scanner's radix affects elements of its default number matching regular expressions; see [localized numbers](Scanner.md) above.

If the radix is less than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_RADIX:kotlin.Int` or greater than `https://developer.android.com/reference/kotlin/java/lang/Character.html#MAX_RADIX:kotlin.Int`, then an `IllegalArgumentException` is thrown.

Invoking the reset method will set the scanner's radix to `10`.

| Parameters ||
|---|---|
| `radix` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The radix to use when scanning numbers |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Scanner#!` | this scanner |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if radix is out of range |
