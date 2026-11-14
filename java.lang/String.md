Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# String

```
class String : CharSequence, Comparable<String!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.String](String.md) |

The `String` class represents character strings. All string literals in Java programs, such as `"abc"`, are implemented as instances of this class.

Strings are constant; their values cannot be changed after they are created. String buffers support mutable strings. Because String objects are immutable they can be shared. For example:

```kotlin
String str = "abc";
  
```

is equivalent to:

```kotlin
char data[] = {'a', 'b', 'c'};
      String str = new String(data);
  
```

Here are some more examples of how strings can be used:

```kotlin
System.out.println("abc");
      String cde = "cde";
      System.out.println("abc" + cde);
      String c = "abc".substring(2,3);
      String d = cde.substring(1, 2);
  
```

The class `String` includes methods for examining individual characters of the sequence, for comparing strings, for searching strings, for extracting substrings, and for creating a copy of a string with all characters translated to uppercase or to lowercase. Case mapping is based on the Unicode Standard version specified by the `https://developer.android.com/reference/kotlin/java/lang/Character` class.

The Java language provides special support for the string concatenation operator ( + ), and for conversion of other objects to strings. For additional information on string concatenation and conversion, see *The Java™ Language Specification*.

Unless otherwise noted, passing a `null` argument to a constructor or method in this class will cause a `https://developer.android.com/reference/kotlin/java/lang/NullPointerException` to be thrown.

A `String` represents a string in the UTF-16 format in which *supplementary characters* are represented by *surrogate pairs* (see the section [Unicode Character Representations](Character.md) in the `Character` class for more information). Index values refer to `char` code units, so a supplementary character uses two positions in a `String`.

The `String` class provides methods for dealing with Unicode code points (i.e., characters), in addition to those for dealing with Unicode code units (i.e., `char` values).

Unless otherwise noted, methods for comparing Strings do not take locale into account. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides methods for finer-grain, locale-sensitive String comparison.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/String#String()()` Initializes a newly created `String` object so that it represents an empty character sequence. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Constructs a new `String` by decoding the specified array of bytes using the platform's default charset. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int)(ascii: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, hibyte: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allocates a new `String` containing characters constructed from an array of 8-bit integer values. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs a new `String` by decoding the specified subarray of bytes using the platform's default charset. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(ascii: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, hibyte: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allocates a new `String` constructed from a subarray of an array of 8-bit integer values. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, charsetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.nio.charset.Charset)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, charset: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)` Constructs a new `String` by decoding the specified subarray of bytes using the specified [charset](../java.nio.charset/Charset.md). |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.String)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, charsetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs a new `String` by decoding the specified array of bytes using the specified [charset](../java.nio.charset/Charset.md). |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20java.nio.charset.Charset)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, charset: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)` Constructs a new `String` by decoding the specified array of bytes using the specified [charset](../java.nio.charset/Charset.md). |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.CharArray)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Allocates a new `String` so that it represents the sequence of characters currently contained in the character array argument. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allocates a new `String` that contains characters from a subarray of the character array argument. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.IntArray,%20kotlin.Int,%20kotlin.Int)(codePoints: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Allocates a new `String` that contains characters from a subarray of the [Unicode code point](Character.md) array argument. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.String)(original: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Initializes a newly created `String` object so that it represents the same sequence of characters as the argument; in other words, the newly created string is a copy of the argument string. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(java.lang.StringBuffer)(buffer: https://developer.android.com/reference/kotlin/java/lang/StringBuffer)` Allocates a new string that contains the sequence of characters currently contained in the string buffer argument. |
| `https://developer.android.com/reference/kotlin/java/lang/String#String(java.lang.StringBuilder)(builder: https://developer.android.com/reference/kotlin/java/lang/StringBuilder)` Allocates a new string that contains the sequence of characters currently contained in the string builder argument. |

| Public methods ||
|---|---|
| [IntStream](../java.util.stream/IntStream.md) | `https://developer.android.com/reference/kotlin/java/lang/String#chars()()` Returns a stream of `int` zero-extending the `char` values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#codePointAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character (Unicode code point) at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#codePointBefore(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character (Unicode code point) before the specified index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#codePointCount(kotlin.Int,%20kotlin.Int)(beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the number of Unicode code points in the specified text range of this `String`. |
| [IntStream](../java.util.stream/IntStream.md) | `https://developer.android.com/reference/kotlin/java/lang/String#codePoints()()` Returns a stream of code point values from this sequence. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#compareTo(kotlin.String)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Compares two strings lexicographically. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#compareToIgnoreCase(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Compares two strings lexicographically, ignoring case differences. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#concat(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Concatenates the specified string to the end of this string. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#contains(kotlin.CharSequence)(s: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Returns true if and only if this string contains the specified sequence of char values. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#contentEquals(kotlin.CharSequence)(cs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Compares this string to the specified `CharSequence`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#contentEquals(java.lang.StringBuffer)(sb: https://developer.android.com/reference/kotlin/java/lang/StringBuffer)` Compares this string to the specified `StringBuffer`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#copyValueOf(kotlin.CharArray)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Equivalent to `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#copyValueOf(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Equivalent to `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#endsWith(kotlin.String)(suffix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Tests if this string ends with the specified suffix. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this string to the specified object. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#equalsIgnoreCase(kotlin.String)(anotherString: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Compares this `String` to another `String`, ignoring case considerations. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#format(kotlin.String,%20kotlin.Any)(format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, vararg args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns a formatted string using the specified format string and arguments. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#format(java.util.Locale,%20kotlin.String,%20kotlin.Any)(l: https://developer.android.com/reference/kotlin/java/util/Locale.html#, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, vararg args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns a formatted string using the specified locale, format string, and arguments. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#formatted(kotlin.Any)(vararg args: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Formats using this string as the format string, and the supplied arguments. |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `char` value at the specified index. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/String#getBytes()()` Encodes this `String` into a sequence of bytes using the platform's default charset, storing the result into a new byte array. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#getBytes(kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int)(srcBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!, dstBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Copies characters from this string into the destination byte array. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/String#getBytes(kotlin.String)(charsetName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Encodes this `String` into a sequence of bytes using the named charset, storing the result into a new byte array. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/String#getBytes(java.nio.charset.Charset)(charset: https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#)` Encodes this `String` into a sequence of bytes using the given [charset](../java.nio.charset/Charset.md), storing the result into a new byte array. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int)(srcBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, srcEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dst: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, dstBegin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#hashCode()()` Returns a hash code for this string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#indent(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Adjusts the indentation of each line of this string based on the value of `n`, and normalizes line termination characters. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#indexOf(kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the first occurrence of the specified character. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#indexOf(kotlin.Int,%20kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#indexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the index within this string of the first occurrence of the specified substring. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#indexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the first occurrence of the specified substring, starting at the specified index. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#intern()()` Returns a canonical representation for the string object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#isBlank()()` Returns `true` if the string is empty or contains only `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` codepoints, otherwise `false`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#isEmpty()()` Returns `true` if, and only if, `https://developer.android.com/reference/kotlin/java/lang/String#length:kotlin.Int` is `0`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#join(kotlin.CharSequence,%20kotlin.CharSequence)(delimiter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, vararg elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Returns a new String composed of copies of the `CharSequence elements` joined together with a copy of the specified `delimiter`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#join(kotlin.CharSequence,%20kotlin.collections.MutableIterable)(delimiter: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!>)` Returns a new `String` composed of copies of the `CharSequence elements` joined together with a copy of the specified `delimiter`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#lastIndexOf(kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the last occurrence of the specified character. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#lastIndexOf(kotlin.Int,%20kotlin.Int)(ch: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the last occurrence of the specified character, searching backward starting at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#lastIndexOf(kotlin.String)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the index within this string of the last occurrence of the specified substring. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#lastIndexOf(kotlin.String,%20kotlin.Int)(str: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this string of the last occurrence of the specified substring, searching backward starting at the specified index. |
| [Stream](../java.util.stream/Stream.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/String#lines()()` Returns a stream of lines extracted from this string, separated by line terminators. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#matches(kotlin.String)(regex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Tells whether or not this string matches the given [regular expression](../java.util.regex/Pattern.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#offsetByCodePoints(kotlin.Int,%20kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, codePointOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index within this `String` that is offset from the given `index` by `codePointOffset` code points. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#regionMatches(kotlin.Boolean,%20kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)(ignoreCase: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, toffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, ooffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests if two string regions are equal. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#regionMatches(kotlin.Int,%20kotlin.String,%20kotlin.Int,%20kotlin.Int)(toffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, ooffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, len: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests if two string regions are equal. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#repeat(kotlin.Int)(count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string whose value is the concatenation of this string repeated `count` times. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#replace(kotlin.Char,%20kotlin.Char)(oldChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html, newChar: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns a string resulting from replacing all occurrences of `oldChar` in this string with `newChar`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#replace(kotlin.CharSequence,%20kotlin.CharSequence)(target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, replacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Replaces each substring of this string that matches the literal target sequence with the specified literal replacement sequence. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#replaceAll(kotlin.String,%20kotlin.String)(regex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, replacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Replaces each substring of this string that matches the given [regular expression](../java.util.regex/Pattern.md) with the given replacement. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#replaceFirst(kotlin.String,%20kotlin.String)(regex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, replacement: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Replaces the first substring of this string that matches the given [regular expression](../java.util.regex/Pattern.md) with the given replacement. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/String#split(kotlin.String)(regex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Splits this string around matches of the given [regular expression](../java.util.regex/Pattern.md). |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/String#split(kotlin.String,%20kotlin.Int)(regex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, limit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Splits this string around matches of the given [regular expression](../java.util.regex/Pattern.md). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#startsWith(kotlin.String)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Tests if this string starts with the specified prefix. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#startsWith(kotlin.String,%20kotlin.Int)(prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, toffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Tests if the substring of this string beginning at the specified index starts with the specified prefix. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#strip()()` Returns a string whose value is this string, with all leading and trailing `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#stripIndent()()` Returns a string whose value is this string, with incidental removed from the beginning and end of every line. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#stripLeading()()` Returns a string whose value is this string, with all leading `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#stripTrailing()()` Returns a string whose value is this string, with all trailing `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#subSequence(kotlin.Int,%20kotlin.Int)(startIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a character sequence that is a subsequence of this sequence. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#substring(kotlin.Int)(beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string that is a substring of this string. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#substring(kotlin.Int,%20kotlin.Int)(beginIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, endIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a string that is a substring of this string. |
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/java/lang/String#toCharArray()()` Converts this string to a new character array. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()()` Converts all of the characters in this `String` to lower case using the rules of the default locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#)` Converts all of the characters in this `String` to lower case using the rules of the given `Locale`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#toString()()` This object (which is already a string!) is itself returned. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()()` Converts all of the characters in this `String` to upper case using the rules of the default locale. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#)` Converts all of the characters in this `String` to upper case using the rules of the given `Locale`. |
| R | `https://developer.android.com/reference/kotlin/java/lang/String#transform(java.util.function.Function)(f: https://developer.android.com/reference/kotlin/java/util/function/Function.html#<in https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, out R>)` This method allows the application of a function to `this` string. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#translateEscapes()()` Returns a string whose value is this string, with escape sequences translated as if in a string literal. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#trim()()` Returns a string whose value is this string, with all leading and trailing space removed, where space is defined as any character whose codepoint is less than or equal to `'U+0020'` (the space character). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Boolean)(b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Returns the string representation of the `boolean` argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Char)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` Returns the string representation of the `char` argument. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!)` Returns the string representation of the `char` array argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, count: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the string representation of a specific subarray of the `char` array argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Double)(d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Returns the string representation of the `double` argument. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Float)(f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the string representation of the `float` argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the string representation of the `int` argument. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Any)(obj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns the string representation of the `Object` argument. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.Long)(l: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the string representation of the `long` argument. |

| Properties ||
|---|---|
| static [Comparator](../java.util/Comparator.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/lang/String#CASE_INSENSITIVE_ORDER:java.util.Comparator` A Comparator that orders `String` objects as by `compareToIgnoreCase`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/String#length:kotlin.Int` Returns the length of this string. |

## Public constructors

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String()
```

Initializes a newly created `String` object so that it represents an empty character sequence. Note that use of this constructor is unnecessary since Strings are immutable.

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(bytes: ByteArray!)
```

Constructs a new `String` by decoding the specified array of bytes using the platform's default charset. The length of the new `String` is a function of the charset, and hence may not be equal to the length of the byte array.

The behavior of this constructor when the given bytes are not valid in the default charset is unspecified. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#` class should be used when more control over the decoding process is required.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be decoded into characters |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    ascii: ByteArray!, 
    hibyte: Int)
```

**Deprecated:** *This method does not properly convert bytes into characters. As of JDK 1.1, the preferred way to do this is via the `String` constructors that take a `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`, charset name, or that use the platform's default charset.*

Allocates a new `String` containing characters constructed from an array of 8-bit integer values. Each character *c* in the resulting string is constructed from the corresponding component *b* in the byte array such that:

```kotlin
<b><i>c</i></b>== (char)(((hibyte & 0xff) << 8)
                          | (<b><i>b</i></b>& 0xff))
  
```

<br />

| Parameters ||
|---|---|
| `ascii` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be converted to characters |
| `hibyte` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top 8 bits of each 16-bit Unicode code unit |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.nio.charset.Charset)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20java.nio.charset.Charset)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray)`

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int)
```

Constructs a new `String` by decoding the specified subarray of bytes using the platform's default charset. The length of the new `String` is a function of the charset, and hence may not be equal to the length of the subarray.

The behavior of this constructor when the given bytes are not valid in the default charset is unspecified. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#` class should be used when more control over the decoding process is required.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be decoded into characters |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first byte to decode |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to decode |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `offset` is negative, `length` is negative, or `offset` is greater than `bytes.length - length` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    ascii: ByteArray!, 
    hibyte: Int, 
    offset: Int, 
    count: Int)
```

**Deprecated:** *This method does not properly convert bytes into characters. As of JDK 1.1, the preferred way to do this is via the `String` constructors that take a `https://developer.android.com/reference/kotlin/java/nio/charset/Charset.html#`, charset name, or that use the platform's default charset.*

Allocates a new `String` constructed from a subarray of an array of 8-bit integer values.

The `offset` argument is the index of the first byte of the subarray, and the `count` argument specifies the length of the subarray.

Each `byte` in the subarray is converted to a `char` as specified in the `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int)` constructor.

| Parameters ||
|---|---|
| `ascii` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be converted to characters |
| `hibyte` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The top 8 bits of each 16-bit Unicode code unit |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial offset |
| --- | --- |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The length |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `offset` is negative, `count` is negative, or `offset` is greater than `ascii.length - count` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20java.nio.charset.Charset)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray,%20java.nio.charset.Charset)`
- `https://developer.android.com/reference/kotlin/java/lang/String#String(kotlin.ByteArray)`

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int, 
    charsetName: String)
```

### String

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    bytes: ByteArray!, 
    offset: Int, 
    length: Int, 
    charset: Charset)
```

Constructs a new `String` by decoding the specified subarray of bytes using the specified [charset](../java.nio.charset/Charset.md). The length of the new `String` is a function of the charset, and hence may not be equal to the length of the subarray.

This method always replaces malformed-input and unmappable-character sequences with this charset's default replacement string. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#` class should be used when more control over the decoding process is required.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be decoded into characters |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the first byte to decode |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to decode |
| --- | --- |
| `charset` | [Charset](../java.nio.charset/Charset.md): The [charset](../java.nio.charset/Charset.md) to be used to decode the `bytes` |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `offset` is negative, `length` is negative, or `offset` is greater than `bytes.length - length` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    bytes: ByteArray!, 
    charsetName: String)
```

Constructs a new `String` by decoding the specified array of bytes using the specified [charset](../java.nio.charset/Charset.md). The length of the new `String` is a function of the charset, and hence may not be equal to the length of the byte array.

The behavior of this constructor when the given bytes are not valid in the given charset is unspecified. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#` class should be used when more control over the decoding process is required.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be decoded into characters |
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of a supported [charset](../java.nio.charset/Charset.md) |

| Exceptions ||
|---|---|
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### String

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    bytes: ByteArray!, 
    charset: Charset)
```

Constructs a new `String` by decoding the specified array of bytes using the specified [charset](../java.nio.charset/Charset.md). The length of the new `String` is a function of the charset, and hence may not be equal to the length of the byte array.

This method always replaces malformed-input and unmappable-character sequences with this charset's default replacement string. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder.html#` class should be used when more control over the decoding process is required.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The bytes to be decoded into characters |
| `charset` | [Charset](../java.nio.charset/Charset.md): The [charset](../java.nio.charset/Charset.md) to be used to decode the `bytes` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(value: CharArray!)
```

Allocates a new `String` so that it represents the sequence of characters currently contained in the character array argument. The contents of the character array are copied; subsequent modification of the character array does not affect the newly created string.

| Parameters ||
|---|---|
| `value` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The initial value of the string |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    value: CharArray!, 
    offset: Int, 
    count: Int)
```

Allocates a new `String` that contains characters from a subarray of the character array argument. The `offset` argument is the index of the first character of the subarray and the `count` argument specifies the length of the subarray. The contents of the subarray are copied; subsequent modification of the character array does not affect the newly created string.

| Parameters ||
|---|---|
| `value` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: Array that is the source of characters |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial offset |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The length |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If `offset` is negative, `count` is negative, or `offset` is greater than `value.length - count` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(
    codePoints: IntArray!, 
    offset: Int, 
    count: Int)
```

Allocates a new `String` that contains characters from a subarray of the [Unicode code point](Character.md) array argument. The `offset` argument is the index of the first code point of the subarray and the `count` argument specifies the length of the subarray. The contents of the subarray are converted to `char`s; subsequent modification of the `int` array does not affect the newly created string.

| Parameters ||
|---|---|
| `codePoints` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array that is the source of Unicode code points |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The initial offset |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The length |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If any invalid Unicode code point is found in `codePoints` |
| `java.lang.IndexOutOfBoundsException` | If `offset` is negative, `count` is negative, or `offset` is greater than `codePoints.length - count` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(original: String)
```

Initializes a newly created `String` object so that it represents the same sequence of characters as the argument; in other words, the newly created string is a copy of the argument string. Unless an explicit copy of `original` is needed, use of this constructor is unnecessary since Strings are immutable.

| Parameters ||
|---|---|
| `original` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A `String` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(buffer: StringBuffer)
```

Allocates a new string that contains the sequence of characters currently contained in the string buffer argument. The contents of the string buffer are copied; subsequent modification of the string buffer does not affect the newly created string.

| Parameters ||
|---|---|
| `buffer` | [StringBuffer](StringBuffer.md): A `StringBuffer` |

### String

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
String(builder: StringBuilder)
```

Allocates a new string that contains the sequence of characters currently contained in the string builder argument. The contents of the string builder are copied; subsequent modification of the string builder does not affect the newly created string.

This constructor is provided to ease migration to `StringBuilder`. Obtaining a string from a string builder via the `toString` method is likely to run faster and is generally preferred.

| Parameters ||
|---|---|
| `builder` | [StringBuilder](StringBuilder.md): A `StringBuilder` |

## Public methods

### chars

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun chars(): IntStream
```

Returns a stream of `int` zero-extending the `char` values from this sequence. Any char which maps to a [surrogate code point](https://developer.android.com//reference/java/lang/Character.html#unicode) is passed through uninterpreted.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of char values from this sequence |

### codePointAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointAt(index: Int): Int
```

Returns the character (Unicode code point) at the specified index. The index refers to `char` values (Unicode code units) and ranges from `0` to `https://developer.android.com/reference/kotlin/java/lang/String#length:kotlin.Int``- 1`.

If the `char` value specified at the given index is in the high-surrogate range, the following index is less than the length of this `String`, and the `char` value at the following index is in the low-surrogate range, then the supplementary code point corresponding to this surrogate pair is returned. Otherwise, the `char` value at the given index is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the `char` values |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the code point value of the character at the `index` |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than the length of this string. |

### codePointBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointBefore(index: Int): Int
```

Returns the character (Unicode code point) before the specified index. The index refers to `char` values (Unicode code units) and ranges from `1` to `https://developer.android.com/reference/kotlin/java/lang/CharSequence#length()`.

If the `char` value at `(index - 1)` is in the low-surrogate range, `(index - 2)` is not negative, and the `char` value at `(index - 2)` is in the high-surrogate range, then the supplementary code point value of the surrogate pair is returned. If the `char` value at `index - 1` is an unpaired low-surrogate or a high-surrogate, the surrogate value is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index following the code point that should be returned |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Unicode code point value before the given index. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is less than 1 or greater than the length of this string. |

### codePointCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePointCount(
    beginIndex: Int, 
    endIndex: Int
): Int
```

Returns the number of Unicode code points in the specified text range of this `String`. The text range begins at the specified `beginIndex` and extends to the `char` at index `endIndex - 1`. Thus the length (in `char`s) of the text range is `endIndex-beginIndex`. Unpaired surrogates within the text range count as one code point each.

| Parameters ||
|---|---|
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to the first `char` of the text range. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index after the last `char` of the text range. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of Unicode code points in the specified text range |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `beginIndex` is negative, or `endIndex` is larger than the length of this `String`, or `beginIndex` is larger than `endIndex`. |

### codePoints

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun codePoints(): IntStream
```

Returns a stream of code point values from this sequence. Any surrogate pairs encountered in the sequence are combined as if by [Character.toCodePoint](Character.md)) and the result is passed to the stream. Any other code units, including ordinary BMP characters, unpaired surrogates, and undefined code units, are zero-extended to `int` values which are then passed to the stream.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/IntStream.html#` | an IntStream of Unicode code points from this sequence |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: String): Int
```

Compares two strings lexicographically. The comparison is based on the Unicode value of each character in the strings. The character sequence represented by this `String` object is compared lexicographically to the character sequence represented by the argument string. The result is a negative integer if this `String` object lexicographically precedes the argument string. The result is a positive integer if this `String` object lexicographically follows the argument string. The result is zero if the strings are equal; returns `0` exactly when the `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)` method would return `true`.

This is the definition of lexicographic ordering. If two strings are different, then either they have different characters at some index that is a valid index for both strings, or their lengths are different, or both. If they have different characters at one or more index positions, let *k* be the smallest such index; then the string whose character at position *k* has the smaller value, as determined by using the `<` operator, lexicographically precedes the other string. In this case, `compareTo` returns the difference of the two character values at position `k` in the two string -- that is, the value:

```kotlin
this.charAt(k)-anotherString.charAt(k)
  
```
If there is no index position at which they differ, then the shorter string lexicographically precedes the longer string. In this case, `compareTo` returns the difference of the lengths of the strings -- that is, the value:

```kotlin
this.length()-anotherString.length()
  
```

For finer-grained String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `anotherString` | the `String` to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value `0` if the argument string is equal to this string; a value less than `0` if this string is lexicographically less than the string argument; and a value greater than `0` if this string is lexicographically greater than the string argument. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### compareToIgnoreCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareToIgnoreCase(str: String): Int
```

Compares two strings lexicographically, ignoring case differences. This method returns an integer whose sign is that of calling `compareTo` with normalized versions of the strings where case differences have been eliminated by calling `Character.toLowerCase(Character.toUpperCase(character))` on each character.

Note that this method does *not* take locale into account, and will result in an unsatisfactory ordering for certain locales. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides locale-sensitive comparison.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the `String` to be compared. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative integer, zero, or a positive integer as the specified String is greater than, equal to, or less than this String, ignoring case considerations. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/text/Collator.html#`

### concat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun concat(str: String): String
```

Concatenates the specified string to the end of this string.

If the length of the argument string is `0`, then this `String` object is returned. Otherwise, a `String` object is returned that represents a character sequence that is the concatenation of the character sequence represented by this `String` object and the character sequence represented by the argument string.

Examples:

```kotlin
"cares".concat("s") returns "caress"
  "to".concat("get").concat("her") returns "together"
  
```

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the `String` that is concatenated to the end of this `String`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string that represents the concatenation of this object's characters followed by the string argument's characters. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contains(s: CharSequence): Boolean
```

Returns true if and only if this string contains the specified sequence of char values.

| Parameters ||
|---|---|
| `s` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the sequence to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this string contains `s`, false otherwise |

### contentEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contentEquals(cs: CharSequence): Boolean
```

Compares this string to the specified `CharSequence`. The result is `true` if and only if this `String` represents the same sequence of char values as the specified sequence. Note that if the `CharSequence` is a `StringBuffer` then the method synchronizes on it.

For finer-grained String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The sequence to compare this `String` against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `String` represents the same sequence of char values as the specified sequence, `false` otherwise |

### contentEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun contentEquals(sb: StringBuffer): Boolean
```

Compares this string to the specified `StringBuffer`. The result is `true` if and only if this `String` represents the same sequence of characters as the specified `StringBuffer`. This method synchronizes on the `StringBuffer`.

For finer-grained String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `sb` | [StringBuffer](StringBuffer.md): The `StringBuffer` to compare this `String` against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this `String` represents the same sequence of characters as the specified `StringBuffer`, `false` otherwise |

### copyValueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyValueOf(data: CharArray!): String
```

Equivalent to `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray)`.

| Parameters ||
|---|---|
| `data` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the character array. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` that contains the characters of the character array. |

### copyValueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copyValueOf(
    data: CharArray!, 
    offset: Int, 
    count: Int
): String
```

Equivalent to `https://developer.android.com/reference/kotlin/java/lang/String#valueOf(kotlin.CharArray,%20kotlin.Int,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `data` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the character array. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): initial offset of the subarray. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): length of the subarray. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` that contains the characters of the specified subarray of the character array. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `offset` is negative, or `count` is negative, or `offset+count` is larger than `data.length`. |

### endsWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun endsWith(suffix: String): Boolean
```

Tests if this string ends with the specified suffix.

| Parameters ||
|---|---|
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the suffix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character sequence represented by the argument is a suffix of the character sequence represented by this object; `false` otherwise. Note that the result will be `true` if the argument is the empty string or is equal to this `String` object as determined by the `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)` method. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Compares this string to the specified object. The result is `true` if and only if the argument is not `null` and is a `String` object that represents the same sequence of characters as this object.

For finer-grained String comparison, refer to `https://developer.android.com/reference/kotlin/java/text/Collator.html#`.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `anObject` | The object to compare this `String` against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given object represents a `String` equivalent to this string, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#compareTo(kotlin.String)`
- `https://developer.android.com/reference/kotlin/java/lang/String#equalsIgnoreCase(kotlin.String)`

### equalsIgnoreCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equalsIgnoreCase(anotherString: String?): Boolean
```

Compares this `String` to another `String`, ignoring case considerations. Two strings are considered equal ignoring case if they are of the same length and corresponding characters in the two strings are equal ignoring case.

Two characters `c1` and `c2` are considered the same ignoring case if at least one of the following is true:

- The two characters are the same (as compared by the `==` operator)
- Calling `Character.toLowerCase(Character.toUpperCase(char))` on each character produces the same result

Note that this method does *not* take locale into account, and will result in unsatisfactory results for certain locales. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides locale-sensitive comparison.

| Parameters ||
|---|---|
| `anotherString` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The `String` to compare this `String` against |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the argument is not `null` and it represents an equivalent `String` ignoring case; `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)`

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun format(
    format: String, 
    vararg args: Any!
): String
```

Returns a formatted string using the specified format string and arguments.

The locale always used is the one returned by `https://developer.android.com/reference/kotlin/java/util/Locale.html#getDefault(java.util.Locale.Category)` with `https://developer.android.com/reference/kotlin/java/util/Locale.Category.html#` category specified.

| Parameters ||
|---|---|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A [format string](../java.util/Formatter.md) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A formatted string |

| Exceptions ||
|---|---|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the formatter class specification. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`

### format

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun format(
    l: Locale, 
    format: String, 
    vararg args: Any!
): String
```

Returns a formatted string using the specified locale, format string, and arguments.

| Parameters ||
|---|---|
| `l` | [Locale](../java.util/Locale.md): The [locale](../java.util/Locale.md) to apply during formatting. If `l` is `null` then no localization is applied. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A [format string](../java.util/Formatter.md) |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in the format string. If there are more arguments than format specifiers, the extra arguments are ignored. The number of arguments is variable and may be zero. The maximum number of arguments is limited by the maximum dimension of a Java array as defined by The Java™ Virtual Machine Specification. The behaviour on a `null` argument depends on the [conversion](../java.util/Formatter.md). |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A formatted string |

| Exceptions ||
|---|---|
| `java.util.IllegalFormatException` | If a format string contains an illegal syntax, a format specifier that is incompatible with the given arguments, insufficient arguments given the format string, or other illegal conditions. For specification of all possible formatting errors, see the [Details](../java.util/Formatter.md) section of the formatter class specification |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`

### formatted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun formatted(vararg args: Any!): String
```

Formats using this string as the format string, and the supplied arguments.

| Parameters ||
|---|---|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Arguments referenced by the format specifiers in this string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A formatted string |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#format(kotlin.String,%20kotlin.Any)`
- `https://developer.android.com/reference/kotlin/java/util/Formatter.html#`

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(index: Int): Char
```

Returns the `char` value at the specified index. An index ranges from `0` to `length() - 1`. The first `char` value of the sequence is at index `0`, the next at index `1`, and so on, as for array indexing.

If the `char` value specified by the index is a [surrogate](Character.md), the surrogate value is returned.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the `char` value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html` | the `char` value at the specified index of this string. The first `char` value is at index `0`. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `index` argument is negative or not less than the length of this string. |

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBytes(): ByteArray!
```

Encodes this `String` into a sequence of bytes using the platform's default charset, storing the result into a new byte array.

The behavior of this method when this string cannot be encoded in the default charset is unspecified. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#` class should be used when more control over the encoding process is required.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | The resultant byte array |

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBytes(
    srcBegin: Int, 
    srcEnd: Int, 
    dst: ByteArray!, 
    dstBegin: Int
): Unit
```

**Deprecated:** *This method does not properly convert characters into bytes. As of JDK 1.1, the preferred way to do this is via the `https://developer.android.com/reference/kotlin/java/lang/String#getBytes()` method, which uses the platform's default charset.*

Copies characters from this string into the destination byte array. Each byte receives the 8 low-order bits of the corresponding character. The eight high-order bits of each character are not copied and do not participate in the transfer in any way.

The first character to be copied is at index `srcBegin`; the last character to be copied is at index `srcEnd-1`. The total number of characters to be copied is `srcEnd-srcBegin`. The characters, converted to bytes, are copied into the subarray of `dst` starting at index `dstBegin` and ending at index:

```kotlin
dstBegin + (srcEnd-srcBegin) - 1
  
```

| Parameters ||
|---|---|
| `srcBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of the first character in the string to copy |
| `srcEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index after the last character in the string to copy |
| `dst` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: The destination array |
| --- | --- |
| `dstBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The start offset in the destination array |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | If any of the following is true: - `srcBegin` is negative - `srcBegin` is greater than `srcEnd` - `srcEnd` is greater than the length of this String - `dstBegin` is negative - `dstBegin+(srcEnd-srcBegin)` is larger than `dst.length` |

### getBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBytes(charsetName: String): ByteArray!
```

Encodes this `String` into a sequence of bytes using the named charset, storing the result into a new byte array.

The behavior of this method when this string cannot be encoded in the given charset is unspecified. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#` class should be used when more control over the encoding process is required.

| Parameters ||
|---|---|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of a supported [charset](../java.nio.charset/Charset.md) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | The resultant byte array |

| Exceptions ||
|---|---|
| `java.io.UnsupportedEncodingException` | If the named charset is not supported |

### getBytes

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBytes(charset: Charset): ByteArray!
```

Encodes this `String` into a sequence of bytes using the given [charset](../java.nio.charset/Charset.md), storing the result into a new byte array.

This method always replaces malformed-input and unmappable-character sequences with this charset's default replacement byte array. The `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder.html#` class should be used when more control over the encoding process is required.

| Parameters ||
|---|---|
| `charset` | [Charset](../java.nio.charset/Charset.md): The [java.nio.charset.Charset](../java.nio.charset/Charset.md) to be used to encode the `String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | The resultant byte array |

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChars(
    srcBegin: Int, 
    srcEnd: Int, 
    dst: CharArray!, 
    dstBegin: Int
): Unit
```

| Parameters ||
|---|---|
| `srcBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `srcEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |
| `dst` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: |
| --- | --- |
| `dstBegin` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code for this string. The hash code for a `String` object is computed as

```kotlin
s[0]*31^(n-1) + s[1]*31^(n-2) + ... + s[n-1]
  
```
using `int` arithmetic, where `s[i]` is the *i* th character of the string, `n` is the length of the string, and `^` indicates exponentiation. (The hash value of the empty string is zero.)

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### indent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indent(n: Int): String
```

Adjusts the indentation of each line of this string based on the value of `n`, and normalizes line termination characters.

This string is conceptually separated into lines using `https://developer.android.com/reference/kotlin/java/lang/String#lines()`. Each line is then adjusted as described below and then suffixed with a line feed `"\n"` (U+000A). The resulting lines are then concatenated and returned.

If `n > 0` then `n` spaces (U+0020) are inserted at the beginning of each line.

If `n < 0` then up to `n` [white space characters](Character.md)) are removed from the beginning of each line. If a given line does not contain sufficient white space then all leading [white space characters](Character.md)) are removed. Each white space character is treated as a single character. In particular, the tab character `"\t"` (U+0009) is considered a single character; it is not expanded.

If `n == 0` then the line remains unchanged. However, line terminators are still normalized.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of leading [white space characters](Character.md)) to add or remove |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string with indentation adjusted and line endings normalized |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#lines()`
- `https://developer.android.com/reference/kotlin/java/lang/String#isBlank()`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(ch: Int): Int
```

Returns the index within this string of the first occurrence of the specified character. If a character with value `ch` occurs in the character sequence represented by this `String` object, then the index (in Unicode code units) of the first such occurrence is returned. For values of `ch` in the range from 0 to 0xFFFF (inclusive), this is the smallest value *k* such that:

```kotlin
this.charAt(<i>k</i>) == ch
  
```
is true. For other values of `ch`, it is the smallest value *k* such that:

```kotlin
this.codePointAt(<i>k</i>) == ch
  
```
is true. In either case, if no such character occurs in this string, then `-1` is returned.

<br />

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a character (Unicode code point). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the character in the character sequence represented by this object, or `-1` if the character does not occur. |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(
    ch: Int, 
    fromIndex: Int
): Int
```

Returns the index within this string of the first occurrence of the specified character, starting the search at the specified index.

If a character with value `ch` occurs in the character sequence represented by this `String` object at an index no smaller than `fromIndex`, then the index of the first such occurrence is returned. For values of `ch` in the range from 0 to 0xFFFF (inclusive), this is the smallest value *k* such that:

```kotlin
(this.charAt(<i>k</i>) == ch) <code>&amp;&amp;</code>(<i>k</i>>= fromIndex)
  
```
is true. For other values of `ch`, it is the smallest value *k* such that:

```kotlin
(this.codePointAt(<i>k</i>) == ch) <code>&amp;&amp;</code>(<i>k</i>>= fromIndex)
  
```
is true. In either case, if no such character occurs in this string at or after position `fromIndex`, then `-1` is returned.

There is no restriction on the value of `fromIndex`. If it is negative, it has the same effect as if it were zero: this entire string may be searched. If it is greater than the length of this string, it has the same effect as if it were equal to the length of this string: `-1` is returned.

All indices are specified in `char` values (Unicode code units).

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a character (Unicode code point). |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to start the search from. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the character in the character sequence represented by this object that is greater than or equal to `fromIndex`, or `-1` if the character does not occur. |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(str: String): Int
```

Returns the index within this string of the first occurrence of the specified substring.

The returned index is the smallest value `k` for which:

```kotlin
<code>this.startsWith(str, k)
  </code>
```
If no such value of `k` exists, then `-1` is returned.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the substring to search for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the specified substring, or `-1` if there is no such occurrence. |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun indexOf(
    str: String, 
    fromIndex: Int
): Int
```

Returns the index within this string of the first occurrence of the specified substring, starting at the specified index.

The returned index is the smallest value `k` for which:

```kotlin
<code>k &gt;= Math.min(fromIndex, this.length()) &amp;&amp;
                    this.startsWith(str, k)
  </code>
```
If no such value of `k` exists, then `-1` is returned.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the substring to search for. |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index from which to start the search. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the specified substring, starting at the specified index, or `-1` if there is no such occurrence. |

### intern

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun intern(): String
```

Returns a canonical representation for the string object.

A pool of strings, initially empty, is maintained privately by the class `String`.

When the intern method is invoked, if the pool already contains a string equal to this `String` object as determined by the `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)` method, then the string from the pool is returned. Otherwise, this `String` object is added to the pool and a reference to this `String` object is returned.

It follows that for any two strings `s` and `t`, `s.intern() == t.intern()` is `true` if and only if `s.equals(t)` is `true`.

All literal strings and string-valued constant expressions are interned. String literals are defined in section 3.10.5 of the The Java™ Language Specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string that has the same contents as this string, but is guaranteed to be from a pool of unique strings. |

### isBlank

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isBlank(): Boolean
```

Returns `true` if the string is empty or contains only `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` codepoints, otherwise `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the string is empty or contains only `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` codepoints, otherwise `false` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### isEmpty

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEmpty(): Boolean
```

Returns `true` if, and only if, `https://developer.android.com/reference/kotlin/java/lang/String#length:kotlin.Int` is `0`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if `https://developer.android.com/reference/kotlin/java/lang/String#length:kotlin.Int` is `0`, otherwise `false` |

### join

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun join(
    delimiter: CharSequence, 
    vararg elements: CharSequence!
): String
```

Returns a new String composed of copies of the `CharSequence elements` joined together with a copy of the specified `delimiter`. For example,

```kotlin
<code>String message = String.join("-", "Java", "is", "cool");
      // message returned is: "Java-is-cool"
  </code>
```
Note that if an element is null, then `"null"` is added.

<br />

| Parameters ||
|---|---|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): the delimiter that separates each element |
| `elements` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: the elements to join together. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a new `String` that is composed of the `elements` separated by the `delimiter` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `delimiter` or `elements` is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/StringJoiner.html#`

### join

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun join(
    delimiter: CharSequence, 
    elements: MutableIterable<CharSequence!>
): String
```

Returns a new `String` composed of copies of the `CharSequence elements` joined together with a copy of the specified `delimiter`. For example,

```kotlin
<code>List&lt;String&gt; strings = List.of("Java", "is", "cool");
      String message = String.join(" ", strings);
      //message returned is: "Java is cool"
 
      Set&lt;String&gt; strings =
          new LinkedHashSet&lt;&gt;(List.of("Java", "is", "very", "cool"));
      String message = String.join("-", strings);
      //message returned is: "Java-is-very-cool"
  </code>
```
Note that if an individual element is `null`, then `"null"` is added.

<br />

| Parameters ||
|---|---|
| `delimiter` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): a sequence of characters that is used to separate each of the `elements` in the resulting `String` |
| `elements` | [MutableIterable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterable/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>: an `Iterable` that will have its `elements` joined together. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a new `String` that is composed from the `elements` argument |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `delimiter` or `elements` is `null` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#join(kotlin.CharSequence,%20kotlin.CharSequence)`
- `https://developer.android.com/reference/kotlin/java/util/StringJoiner.html#`

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(ch: Int): Int
```

Returns the index within this string of the last occurrence of the specified character. For values of `ch` in the range from 0 to 0xFFFF (inclusive), the index (in Unicode code units) returned is the largest value *k* such that:

```kotlin
this.charAt(<i>k</i>) == ch
  
```
is true. For other values of `ch`, it is the largest value *k* such that:

```kotlin
this.codePointAt(<i>k</i>) == ch
  
```
is true. In either case, if no such character occurs in this string, then `-1` is returned. The `String` is searched backwards starting at the last character.

<br />

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a character (Unicode code point). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the character in the character sequence represented by this object, or `-1` if the character does not occur. |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(
    ch: Int, 
    fromIndex: Int
): Int
```

Returns the index within this string of the last occurrence of the specified character, searching backward starting at the specified index. For values of `ch` in the range from 0 to 0xFFFF (inclusive), the index returned is the largest value *k* such that:

```kotlin
(this.charAt(<i>k</i>) == ch) <code>&amp;&amp;</code>(<i>k</i><= fromIndex)
  
```
is true. For other values of `ch`, it is the largest value *k* such that:

```kotlin
(this.codePointAt(<i>k</i>) == ch) <code>&amp;&amp;</code>(<i>k</i><= fromIndex)
  
```
is true. In either case, if no such character occurs in this string at or before position `fromIndex`, then `-1` is returned.

<br />

All indices are specified in `char` values (Unicode code units).

| Parameters ||
|---|---|
| `ch` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a character (Unicode code point). |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to start the search from. There is no restriction on the value of `fromIndex`. If it is greater than or equal to the length of this string, it has the same effect as if it were equal to one less than the length of this string: this entire string may be searched. If it is negative, it has the same effect as if it were -1: -1 is returned. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the character in the character sequence represented by this object that is less than or equal to `fromIndex`, or `-1` if the character does not occur before that point. |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(str: String): Int
```

Returns the index within this string of the last occurrence of the specified substring. The last occurrence of the empty string "" is considered to occur at the index value `this.length()`.

The returned index is the largest value `k` for which:

```kotlin
<code>this.startsWith(str, k)
  </code>
```
If no such value of `k` exists, then `-1` is returned.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the substring to search for. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the specified substring, or `-1` if there is no such occurrence. |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lastIndexOf(
    str: String, 
    fromIndex: Int
): Int
```

Returns the index within this string of the last occurrence of the specified substring, searching backward starting at the specified index.

The returned index is the largest value `k` for which:

```kotlin
<code>k &lt;= Math.min(fromIndex, this.length()) &amp;&amp;
                    this.startsWith(str, k)
  </code>
```
If no such value of `k` exists, then `-1` is returned.

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the substring to search for. |
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to start the search from. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the specified substring, searching backward from the specified index, or `-1` if there is no such occurrence. |

### lines

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lines(): Stream<String!>
```

Returns a stream of lines extracted from this string, separated by line terminators.

A *line terminator* is one of the following: a line feed character `"\n"` (U+000A), a carriage return character `"\r"` (U+000D), or a carriage return followed immediately by a line feed `"\r\n"` (U+000D U+000A).

A *line* is either a sequence of zero or more characters followed by a line terminator, or it is a sequence of one or more characters followed by the end of the string. A line does not include the line terminator.

The stream returned by this method contains the lines from this string in the order in which they occur.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/stream/Stream.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | the stream of lines extracted from this string |

### matches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun matches(regex: String): Boolean
```

Tells whether or not this string matches the given [regular expression](../java.util.regex/Pattern.md).

An invocation of this method of the form *str* `.matches(`*regex* `)` yields exactly the same result as the expression
`https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`.`https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#matches(kotlin.String,%20kotlin.CharSequence)`

| Parameters ||
|---|---|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the regular expression to which this string is to be matched |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this string matches the given regular expression |

| Exceptions ||
|---|---|
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`

### offsetByCodePoints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun offsetByCodePoints(
    index: Int, 
    codePointOffset: Int
): Int
```

Returns the index within this `String` that is offset from the given `index` by `codePointOffset` code points. Unpaired surrogates within the text range given by `index` and `codePointOffset` count as one code point each.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index to be offset |
| `codePointOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the offset in code points |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index within this `String` |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `index` is negative or larger then the length of this `String`, or if `codePointOffset` is positive and the substring starting with `index` has fewer than `codePointOffset` code points, or if `codePointOffset` is negative and the substring before `index` has fewer than the absolute value of `codePointOffset` code points. |

### regionMatches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun regionMatches(
    ignoreCase: Boolean, 
    toffset: Int, 
    other: String, 
    ooffset: Int, 
    len: Int
): Boolean
```

Tests if two string regions are equal.

A substring of this `String` object is compared to a substring of the argument `other`. The result is `true` if these substrings represent character sequences that are the same, ignoring case if and only if `ignoreCase` is true. The substring of this `String` object to be compared begins at index `toffset` and has length `len`. The substring of `other` to be compared begins at index `ooffset` and has length `len`. The result is `false` if and only if at least one of the following is true:

- `toffset` is negative.
- `ooffset` is negative.
- `toffset+len` is greater than the length of this `String` object.
- `ooffset+len` is greater than the length of the other argument.
- `ignoreCase` is `false` and there is some nonnegative integer *k* less than `len` such that:

  ```kotlin
  this.charAt(toffset+k) != other.charAt(ooffset+k)
    
  ```
- `ignoreCase` is `true` and there is some nonnegative integer *k* less than `len` such that:

  ```kotlin
  Character.toLowerCase(Character.toUpperCase(this.charAt(toffset+k))) !=
        Character.toLowerCase(Character.toUpperCase(other.charAt(ooffset+k)))
    
  ```

Note that this method does *not* take locale into account, and will result in unsatisfactory results for certain locales when `ignoreCase` is `true`. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides locale-sensitive comparison.

| Parameters ||
|---|---|
| `ignoreCase` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true`, ignore case when comparing characters. |
| `toffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the starting offset of the subregion in this string. |
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string argument. |
| --- | --- |
| `ooffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the starting offset of the subregion in the string argument. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of characters to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified subregion of this string matches the specified subregion of the string argument; `false` otherwise. Whether the matching is exact or case insensitive depends on the `ignoreCase` argument. |

### regionMatches

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun regionMatches(
    toffset: Int, 
    other: String, 
    ooffset: Int, 
    len: Int
): Boolean
```

Tests if two string regions are equal.

A substring of this `String` object is compared to a substring of the argument other. The result is true if these substrings represent identical character sequences. The substring of this `String` object to be compared begins at index `toffset` and has length `len`. The substring of other to be compared begins at index `ooffset` and has length `len`. The result is `false` if and only if at least one of the following is true:

- `toffset` is negative.
- `ooffset` is negative.
- `toffset+len` is greater than the length of this `String` object.
- `ooffset+len` is greater than the length of the other argument.
- There is some nonnegative integer *k* less than `len` such that: `this.charAt(toffset + `*k* `) != other.charAt(ooffset + ` *k* `)`

Note that this method does *not* take locale into account. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides locale-sensitive comparison.

| Parameters ||
|---|---|
| `toffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the starting offset of the subregion in this string. |
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string argument. |
| `ooffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the starting offset of the subregion in the string argument. |
| --- | --- |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of characters to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified subregion of this string exactly matches the specified subregion of the string argument; `false` otherwise. |

### repeat

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun repeat(count: Int): String
```

Returns a string whose value is the concatenation of this string repeated `count` times.

If this string is empty or count is zero then the empty string is returned.

| Parameters ||
|---|---|
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of times to repeat |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string composed of this string repeated `count` times or the empty string if this string is empty or count is zero |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `count` is negative. |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replace(
    oldChar: Char, 
    newChar: Char
): String
```

Returns a string resulting from replacing all occurrences of `oldChar` in this string with `newChar`.

If the character `oldChar` does not occur in the character sequence represented by this `String` object, then a reference to this `String` object is returned. Otherwise, a `String` object is returned that represents a character sequence identical to the character sequence represented by this `String` object, except that every occurrence of `oldChar` is replaced by an occurrence of `newChar`.

Examples:

```kotlin
"mesquite in your cellar".replace('e', 'o')
          returns "mosquito in your collar"
  "the war of baronets".replace('r', 'y')
          returns "the way of bayonets"
  "sparring with a purple porpoise".replace('p', 't')
          returns "starring with a turtle tortoise"
  "JonL".replace('q', 'x') returns "JonL" (no change)
  
```

| Parameters ||
|---|---|
| `oldChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the old character. |
| `newChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): the new character. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string derived from this string by replacing every occurrence of `oldChar` with `newChar`. |

### replace

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replace(
    target: CharSequence, 
    replacement: CharSequence
): String
```

Replaces each substring of this string that matches the literal target sequence with the specified literal replacement sequence. The replacement proceeds from the beginning of the string to the end, for example, replacing "aa" with "b" in the string "aaa" will result in "ba" rather than "ab".

| Parameters ||
|---|---|
| `target` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The sequence of char values to be replaced |
| `replacement` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The replacement sequence of char values |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The resulting string |

### replaceAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replaceAll(
    regex: String, 
    replacement: String
): String
```

Replaces each substring of this string that matches the given [regular expression](../java.util.regex/Pattern.md) with the given replacement.

An invocation of this method of the form *str* `.replaceAll(`*regex* `,` *repl* `)` yields exactly the same result as the expression
`` `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`.java.util.regex.Pattern#compile(regex).`https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#matcher(kotlin.CharSequence)`(str).java.util.regex.Matcher#replaceAll(repl) ``

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string; see java.util.regex.Matcher#replaceAll. Use `https://developer.android.com/reference/kotlin/java/util/regex/Matcher.html#quoteReplacement(kotlin.String)` to suppress the special meaning of these characters, if desired.

| Parameters ||
|---|---|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the regular expression to which this string is to be matched |
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string to be substituted for each match |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The resulting `String` |

| Exceptions ||
|---|---|
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`

### replaceFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun replaceFirst(
    regex: String, 
    replacement: String
): String
```

Replaces the first substring of this string that matches the given [regular expression](../java.util.regex/Pattern.md) with the given replacement.

An invocation of this method of the form *str* `.replaceFirst(`*regex* `,` *repl* `)` yields exactly the same result as the expression
`` `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`.java.util.regex.Pattern#compile(regex).`https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#matcher(kotlin.CharSequence)`(str).java.util.regex.Matcher#replaceFirst(repl) ``

Note that backslashes (`\`) and dollar signs (`$`) in the replacement string may cause the results to be different than if it were being treated as a literal replacement string; see java.util.regex.Matcher#replaceFirst. Use `https://developer.android.com/reference/kotlin/java/util/regex/Matcher.html#quoteReplacement(kotlin.String)` to suppress the special meaning of these characters, if desired.

| Parameters ||
|---|---|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the regular expression to which this string is to be matched |
| `replacement` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the string to be substituted for the first match |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The resulting `String` |

| Exceptions ||
|---|---|
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun split(regex: String): Array<String!>
```

Splits this string around matches of the given [regular expression](../java.util.regex/Pattern.md).

This method works as if by invoking the two-argument `https://developer.android.com/reference/kotlin/java/lang/String#split(kotlin.String,%20kotlin.Int)` method with the given expression and a limit argument of zero. Trailing empty strings are therefore not included in the resulting array.

The string `"boo:and:foo"`, for example, yields the following results with these expressions:

| Regex | Result |
| --- | --- |
| : | `{ "boo", "and", "foo" }` |
| o | `{ "b", "", ":and:f" }` |
|---|---|

| Parameters ||
|---|---|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the delimiting regular expression |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | the array of strings computed by splitting this string around matches of the given regular expression |

| Exceptions ||
|---|---|
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`

### split

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun split(
    regex: String, 
    limit: Int
): Array<String!>
```

Splits this string around matches of the given [regular expression](../java.util.regex/Pattern.md).

The array returned by this method contains each substring of this string that is terminated by another substring that matches the given expression or is terminated by the end of the string. The substrings in the array are in the order in which they occur in this string. If the expression does not match any part of the input then the resulting array has just one element, namely this string.

When there is a positive-width match at the beginning of this string then an empty leading substring is included at the beginning of the resulting array. A zero-width match at the beginning however never produces such empty leading substring.

The `limit` parameter controls the number of times the pattern is applied and therefore affects the length of the resulting array.

- If the *limit* is positive then the pattern will be applied at most *limit* - 1 times, the array's length will be no greater than *limit*, and the array's last entry will contain all input beyond the last matched delimiter.
- If the *limit* is zero then the pattern will be applied as many times as possible, the array can have any length, and trailing empty strings will be discarded.
- If the *limit* is negative then the pattern will be applied as many times as possible and the array can have any length.

The string `"boo:and:foo"`, for example, yields the following results with these parameters:

| Regex | Limit | Result |
| --- | --- | --- |
| : | 2 | `{ "boo", "and:foo" }` |
| : | 5 | `{ "boo", "and", "foo" }` |
| : | -2 | `{ "boo", "and", "foo" }` |
| --- | --- | --- |
| o | 5 | `{ "b", "", ":and:f", "", "" }` |
| o | -2 | `{ "b", "", ":and:f", "", "" }` |
| o | 0 | `{ "b", "", ":and:f" }` |
|---|---|---|

An invocation of this method of the form *str.* `split(`*regex* `,` *n* `)` yields the same result as the expression
`` `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`.java.util.regex.Pattern#compile(regex).`https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#split(kotlin.CharSequence,%20kotlin.Int)`(str, n) ``

| Parameters ||
|---|---|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the delimiting regular expression |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the result threshold, as described above |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | the array of strings computed by splitting this string around matches of the given regular expression |

| Exceptions ||
|---|---|
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/regex/Pattern.html#`

### startsWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startsWith(prefix: String): Boolean
```

Tests if this string starts with the specified prefix.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the prefix. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character sequence represented by the argument is a prefix of the character sequence represented by this string; `false` otherwise. Note also that `true` will be returned if the argument is an empty string or is equal to this `String` object as determined by the `https://developer.android.com/reference/kotlin/java/lang/String#equals(kotlin.Any)` method. |

### startsWith

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startsWith(
    prefix: String, 
    toffset: Int
): Boolean
```

Tests if the substring of this string beginning at the specified index starts with the specified prefix.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the prefix. |
| `toffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): where to begin looking in this string. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the character sequence represented by the argument is a prefix of the substring of this object starting at index `toffset`; `false` otherwise. The result is `false` if `toffset` is negative or greater than the length of this `String` object; otherwise the result is the same as the result of the expression ```kotlin this.substring(toffset).startsWith(prefix) ``` |

### strip

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun strip(): String
```

Returns a string whose value is this string, with all leading and trailing `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed.

If this `String` object represents an empty string, or if all code points in this string are `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`, then an empty string is returned.

Otherwise, returns a substring of this string beginning with the first code point that is not a `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` up to and including the last code point that is not a `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`.

This method may be used to strip `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` from the beginning and end of a string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string whose value is this string, with all leading and trailing white space removed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### stripIndent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stripIndent(): String
```

Returns a string whose value is this string, with incidental removed from the beginning and end of every line.

Incidental [white space](Character.md)) is often present in a text block to align the content with the opening delimiter. For example, in the following code, dots represent incidental [white space](Character.md)):

```kotlin
String html = """
  ..............<html>
  ..............    <body>
  ..............        <p>Hello, world</p>
  ..............    </body>
  ..............</html>
  ..............""";
  
```
This method treats the incidental [white space](Character.md)) as indentation to be stripped, producing a string that preserves the relative indentation of the content. Using | to visualize the start of each line of the string:
| --- | --- |

```kotlin
|<html>
  |    <body>
  |        <p>Hello, world</p>
  |    </body>
  |</html>
  
```
First, the individual lines of this string are extracted. A *line* is a sequence of zero or more characters followed by either a line terminator or the end of the string. If the string has at least one line terminator, the last line consists of the characters between the last terminator and the end of the string. Otherwise, if the string has no terminators, the last line is the start of the string to the end of the string, in other words, the entire string. A line does not include the line terminator.

Then, the *minimum indentation* (min) is determined as follows:

- For each non-blank line (as defined by `https://developer.android.com/reference/kotlin/java/lang/String#isBlank()`), the leading [white space](Character.md)) characters are counted.

- The leading [white space](Character.md)) characters on the last line are also counted even if [blank](String.md)).

The *min* value is the smallest of these counts.

For each [non-blank](String.md)) line, *min* leading [white space](Character.md)) characters are removed, and any trailing [white](Character.md)) characters are removed. [Blank](String.md)) lines are replaced with the empty string.

Finally, the lines are joined into a new string, using the LF character `"\n"` (U+000A) to separate lines.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string with incidental indentation removed and line terminators normalized |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#lines()`
- `https://developer.android.com/reference/kotlin/java/lang/String#isBlank()`
- `https://developer.android.com/reference/kotlin/java/lang/String#indent(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### stripLeading

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stripLeading(): String
```

Returns a string whose value is this string, with all leading `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed.

If this `String` object represents an empty string, or if all code points in this string are `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`, then an empty string is returned.

Otherwise, returns a substring of this string beginning with the first code point that is not a `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` up to to and including the last code point of this string.

This method may be used to trim `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` from the beginning of a string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string whose value is this string, with all leading white space removed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### stripTrailing

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stripTrailing(): String
```

Returns a string whose value is this string, with all trailing `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` removed.

If this `String` object represents an empty string, or if all characters in this string are `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`, then an empty string is returned.

Otherwise, returns a substring of this string beginning with the first code point of this string up to and including the last code point that is not a `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`.

This method may be used to trim `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)` from the end of a string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string whose value is this string, with all trailing white space removed |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Character#isWhitespace(kotlin.Int)`

### subSequence

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun subSequence(
    startIndex: Int, 
    endIndex: Int
): CharSequence
```

Returns a character sequence that is a subsequence of this sequence.

An invocation of this method of the form

```kotlin
str.subSequence(begin, end)
```
behaves in exactly the same way as the invocation

```kotlin
str.substring(begin, end)
```

| Parameters ||
|---|---|
| `start` | the start index, inclusive |
| `end` | the end index, exclusive |
| `beginIndex` | the begin index, inclusive. |
| --- | --- |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the end index, exclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html` | the specified subsequence. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `beginIndex` or `endIndex` is negative, if `endIndex` is greater than `length()`, or if `beginIndex` is greater than `endIndex` |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(beginIndex: Int): String
```

Returns a string that is a substring of this string. The substring begins with the character at the specified index and extends to the end of this string.

Examples:

```kotlin
"unhappy".substring(2) returns "happy"
  "Harbison".substring(3) returns "bison"
  "emptiness".substring(9) returns "" (an empty string)
  
```

| Parameters ||
|---|---|
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the beginning index, inclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the specified substring. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `beginIndex` is negative or larger than the length of this `String` object. |

### substring

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun substring(
    beginIndex: Int, 
    endIndex: Int
): String
```

Returns a string that is a substring of this string. The substring begins at the specified `beginIndex` and extends to the character at index `endIndex - 1`. Thus the length of the substring is `endIndex-beginIndex`.

Examples:

```kotlin
"hamburger".substring(4, 8) returns "urge"
  "smiles".substring(1, 5) returns "mile"
  
```

| Parameters ||
|---|---|
| `beginIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the beginning index, inclusive. |
| `endIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ending index, exclusive. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the specified substring. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the `beginIndex` is negative, or `endIndex` is larger than the length of this `String` object, or `beginIndex` is larger than `endIndex`. |

### toCharArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toCharArray(): CharArray!
```

Converts this string to a new character array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!` | a newly allocated character array whose length is the length of this string and whose contents are initialized to contain the character sequence represented by this string. |

### toLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLowerCase(): String
```

Converts all of the characters in this `String` to lower case using the rules of the default locale. This is equivalent to calling `toLowerCase(Locale.getDefault())`.

**Note:** This method is locale sensitive, and may produce unexpected results if used for strings that are intended to be interpreted locale independently. Examples are programming language identifiers, protocol keys, and HTML tags. For instance, `"TITLE".toLowerCase()` in a Turkish locale returns `"t\u005Cu0131tle"`, where '\\u005Cu0131' is the LATIN SMALL LETTER DOTLESS I character. To obtain correct results for locale insensitive strings, use `toLowerCase(Locale.ROOT)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the `String`, converted to lowercase. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase(java.util.Locale)`

### toLowerCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toLowerCase(locale: Locale): String
```

Converts all of the characters in this `String` to lower case using the rules of the given `Locale`. Case mapping is based on the Unicode Standard version specified by the `https://developer.android.com/reference/kotlin/java/lang/Character` class. Since case mappings are not always 1:1 char mappings, the resulting `String` may be a different length than the original `String`.

Examples of lowercase mappings are in the following table:

| Language Code of Locale | Upper Case | Lower Case | Description |
|---|---|---|---|
| tr (Turkish) | \\u0130 | \\u0069 | capital letter I with dot above -\> small letter i |
| tr (Turkish) | \\u0049 | \\u0131 | capital letter I -\> small letter dotless i |
| (all) | French Fries | french fries | lowercased all chars in String |
| --- | --- | --- | --- |
| (all) | ΙΧΘΥΣ | ιχθυσ | lowercased all chars in String |

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md): use the case transformation rules for this locale |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the `String`, converted to lowercase. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()`
- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()`
- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase(java.util.Locale)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

This object (which is already a string!) is itself returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the string itself. |

### toUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toUpperCase(): String
```

Converts all of the characters in this `String` to upper case using the rules of the default locale. This method is equivalent to `toUpperCase(Locale.getDefault())`.

**Note:** This method is locale sensitive, and may produce unexpected results if used for strings that are intended to be interpreted locale independently. Examples are programming language identifiers, protocol keys, and HTML tags. For instance, `"title".toUpperCase()` in a Turkish locale returns `"T\u005Cu0130TLE"`, where '\\u005Cu0130' is the LATIN CAPITAL LETTER I WITH DOT ABOVE character. To obtain correct results for locale insensitive strings, use `toUpperCase(Locale.ROOT)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the `String`, converted to uppercase. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase(java.util.Locale)`

### toUpperCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toUpperCase(locale: Locale): String
```

Converts all of the characters in this `String` to upper case using the rules of the given `Locale`. Case mapping is based on the Unicode Standard version specified by the `https://developer.android.com/reference/kotlin/java/lang/Character` class. Since case mappings are not always 1:1 char mappings, the resulting `String` may be a different length than the original `String`.

Examples of locale-sensitive and 1:M case mappings are in the following table.

| Language Code of Locale | Lower Case | Upper Case | Description |
|---|---|---|---|
| tr (Turkish) | \\u0069 | \\u0130 | small letter i -\> capital letter I with dot above |
| tr (Turkish) | \\u0131 | \\u0049 | small letter dotless i -\> capital letter I |
| (all) | \\u00df | \\u0053 \\u0053 | small letter sharp s -\> two letters: SS |
| --- | --- | --- | --- |
| (all) | Fahrvergnügen | FAHRVERGNÜGEN | |

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md): use the case transformation rules for this locale |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the `String`, converted to uppercase. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/String#toUpperCase()`
- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase()`
- `https://developer.android.com/reference/kotlin/java/lang/String#toLowerCase(java.util.Locale)`

### transform

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <R : Any!> transform(f: Function<in String!, out R>): R
```

This method allows the application of a function to `this` string. The function should expect a single String argument and produce an `R` result.

Any exception thrown by `f.apply()` will be propagated to the caller.

| Parameters ||
|---|---|
| `<R>` | the type of the result |
| `f` | [Function](../java.util.function/Function.md)\<in [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, out R\>: a function to apply |

| Return ||
|---|---|
| `R` | the result of applying the function to this string |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/function/Function.html#`

### translateEscapes

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun translateEscapes(): String
```

Returns a string whose value is this string, with escape sequences translated as if in a string literal.

Escape sequences are translated as follows;

| Escape | Name | Translation |
| --- | --- | --- |
| `\u005Cb` | backspace | `U+0008` |
| `\u005Ct` | horizontal tab | `U+0009` |
| `\u005Cn` | line feed | `U+000A` |
| --- | --- | --- |
| `\u005Cf` | form feed | `U+000C` |
| `\u005Cr` | carriage return | `U+000D` |
| `\u005Cs` | space | `U+0020` |
| --- | --- | --- |
| `\u005C"` | double quote | `U+0022` |
| `\u005C'` | single quote | `U+0027` |
| `\u005C\u005C` | backslash | `U+005C` |
| --- | --- | --- |
| `\u005C0 - \u005C377` | octal escape | code point equivalents |
| `\u005C<line-terminator>` | continuation | discard |
|---|---|---|

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | String with escape sequences translated. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | when an escape sequence is malformed. |

### trim

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun trim(): String
```

Returns a string whose value is this string, with all leading and trailing space removed, where space is defined as any character whose codepoint is less than or equal to `'U+0020'` (the space character).

If this `String` object represents an empty character sequence, or the first and last characters of character sequence represented by this `String` object both have codes that are not space (as defined above), then a reference to this `String` object is returned.

Otherwise, if all characters in this string are space (as defined above), then a `String` object representing an empty string is returned.

Otherwise, let *k* be the index of the first character in the string whose code is not a space (as defined above) and let *m* be the index of the last character in the string whose code is not a space (as defined above). A `String` object is returned, representing the substring of this string that begins with the character at index *k* and ends with the character at index *m* -that is, the result of `this.substring(k, m + 1)`.

This method may be used to trim space (as defined above) from the beginning and end of a string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string whose value is this string, with all leading and trailing space removed, or this string if it has no leading or trailing space. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(b: Boolean): String
```

Returns the string representation of the `boolean` argument.

| Parameters ||
|---|---|
| `b` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a `boolean`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | if the argument is `true`, a string equal to `"true"` is returned; otherwise, a string equal to `"false"` is returned. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(c: Char): String
```

Returns the string representation of the `char` argument.

| Parameters ||
|---|---|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html): a `char`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string of length `1` containing as its single character the argument `c`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(data: CharArray!): String
```

Returns the string representation of the `char` array argument. The contents of the character array are copied; subsequent modification of the character array does not affect the returned string.

| Parameters ||
|---|---|
| `data` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the character array. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` that contains the characters of the character array. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(
    data: CharArray!, 
    offset: Int, 
    count: Int
): String
```

Returns the string representation of a specific subarray of the `char` array argument.

The `offset` argument is the index of the first character of the subarray. The `count` argument specifies the length of the subarray. The contents of the subarray are copied; subsequent modification of the character array does not affect the returned string.

| Parameters ||
|---|---|
| `data` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: the character array. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): initial offset of the subarray. |
| `count` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): length of the subarray. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` that contains the characters of the specified subarray of the character array. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if `offset` is negative, or `count` is negative, or `offset+count` is larger than `data.length`. |

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(d: Double): String
```

Returns the string representation of the `double` argument.

The representation is exactly the one returned by the `Double.toString` method of one argument.

| Parameters ||
|---|---|
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): a `double`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the `double` argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Double#toString(kotlin.Double)`

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(f: Float): String
```

Returns the string representation of the `float` argument.

The representation is exactly the one returned by the `Float.toString` method of one argument.

| Parameters ||
|---|---|
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): a `float`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the `float` argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Float#toString(kotlin.Float)`

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(i: Int): String
```

Returns the string representation of the `int` argument.

The representation is exactly the one returned by the `Integer.toString` method of one argument.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the `int` argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Integer#toString(kotlin.Int,%20kotlin.Int)`

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(obj: Any?): String
```

Returns the string representation of the `Object` argument.

| Parameters ||
|---|---|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: an `Object`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | if the argument is `null`, then a string equal to `"null"`; otherwise, the value of `obj.toString()` is returned. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Object#toString()`

### valueOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun valueOf(l: Long): String
```

Returns the string representation of the `long` argument.

The representation is exactly the one returned by the `Long.toString` method of one argument.

| Parameters ||
|---|---|
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a `long`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the `long` argument. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/Long#toString(kotlin.Long)`

## Properties

### CASE_INSENSITIVE_ORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CASE_INSENSITIVE_ORDER: Comparator<String!>!
```

A Comparator that orders `String` objects as by `compareToIgnoreCase`. This comparator is serializable.

Note that this Comparator does *not* take locale into account, and will result in an unsatisfactory ordering for certain locales. The `https://developer.android.com/reference/kotlin/java/text/Collator.html#` class provides locale-sensitive comparison.
**See Also**

- `https://developer.android.com/reference/kotlin/java/text/Collator.html#`

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val length: Int
```

Returns the length of this string. The length is equal to the number of [Unicode code units](Character.md) in the string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the sequence of characters represented by this object. |
