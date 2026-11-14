Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Charset

```
abstract class Charset : Comparable<Charset!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.charset.Charset](Charset.md) |

A named mapping between sequences of sixteen-bit Unicode [code units](../java.lang/Character.md) and sequences of bytes. This class defines methods for creating decoders and encoders and for retrieving the various names associated with a charset. Instances of this class are immutable.

This class also defines static methods for testing whether a particular charset is supported, for locating charset instances by name, and for constructing a map that contains every charset for which support is available in the current Java virtual machine. Support for new charsets can be added via the service-provider interface defined in the CharsetProvider class.

All of the methods defined in this class are safe for use by multiple concurrent threads.

## Charset names

Charsets are named by strings composed of the following characters:

- The uppercase letters `'A'` through `'Z'` (`'\u0041'` through `'\u005a'`),
- The lowercase letters `'a'` through `'z'` (`'\u0061'` through `'\u007a'`),
- The digits `'0'` through `'9'` (`'\u0030'` through `'\u0039'`),
- The dash character `'-'` (`'\u002d'`, HYPHEN-MINUS),
- The plus character `'+'` (`'\u002b'`, PLUS SIGN),
- The period character `'.'` (`'\u002e'`, FULL STOP),
- The colon character `':'` (`'\u003a'`, COLON), and
- The underscore character `'_'` (`'\u005f'`, LOW LINE).

A charset name must begin with either a letter or a digit. The empty string is not a legal charset name. Charset names are not case-sensitive; that is, case is always ignored when comparing charset names. Charset names generally follow the conventions documented in [*RFC 2278: IANA Charset Registration Procedures*](http://www.ietf.org/rfc/rfc2278.txt).

Every charset has a *canonical name* and may also have one or more *aliases* . The canonical name is returned by the name method of this class. Canonical names are, by convention, usually in upper case. The aliases of a charset are returned by the aliases method.

Some charsets have an *historical name* that is defined for compatibility with previous versions of the Java platform. A charset's historical name is either its canonical name or one of its aliases. The historical name is returned by the `getEncoding()` methods of the getEncoding and getEncoding classes.

If a charset listed in the [*IANA Charset Registry*](http://www.iana.org/assignments/character-sets) is supported by an implementation of the Java platform then its canonical name must be the name listed in the registry. Many charsets are given more than one name in the registry, in which case the registry identifies one of the names as *MIME-preferred* . If a charset has more than one registry name then its canonical name must be the MIME-preferred name and the other names in the registry must be valid aliases. If a supported charset is not listed in the IANA registry then its canonical name must begin with one of the strings `"X-"` or `"x-"`.

The IANA charset registry does change over time, and so the canonical name and the aliases of a particular charset may also change over time. To ensure compatibility it is recommended that no alias ever be removed from a charset, and that if the canonical name of a charset is changed then its previous canonical name be made into an alias.

## Standard charsets

Every implementation of the Java platform is required to support the following standard charsets. Consult the release documentation for your implementation to see if any other charsets are supported. The behavior of such optional charsets may differ between implementations.

| Charset | Description |
| --- | --- |
| `US-ASCII` | Seven-bit ASCII, a.k.a. `ISO646-US`, a.k.a. the Basic Latin block of the Unicode character set |
| `ISO-8859-1 ` | ISO Latin Alphabet No. 1, a.k.a. `ISO-LATIN-1` |
| `UTF-8` | Eight-bit UCS Transformation Format |
| --- | --- |
| `UTF-16BE` | Sixteen-bit UCS Transformation Format, big-endian byte order |
| `UTF-16LE` | Sixteen-bit UCS Transformation Format, little-endian byte order |
| `UTF-16` | Sixteen-bit UCS Transformation Format, byte order identified by an optional byte-order mark |
|---|---|

The `UTF-8` charset is specified by [*RFC 2279*](http://www.ietf.org/rfc/rfc2279.txt); the transformation format upon which it is based is specified in Amendment 2 of ISO 10646-1 and is also described in the [*Unicode Standard*](http://www.unicode.org/unicode/standard/standard.html).

The `UTF-16` charsets are specified by [*RFC 2781*](http://www.ietf.org/rfc/rfc2781.txt); the transformation formats upon which they are based are specified in Amendment 1 of ISO 10646-1 and are also described in the [*Unicode Standard*](http://www.unicode.org/unicode/standard/standard.html).

The `UTF-16` charsets use sixteen-bit quantities and are therefore sensitive to byte order. In these encodings the byte order of a stream may be indicated by an initial *byte-order mark* represented by the Unicode character `'\uFEFF'`. Byte-order marks are handled as follows:

- When decoding, the `UTF-16BE` and `UTF-16LE` charsets interpret the initial byte-order marks as a ZERO-WIDTH NON-BREAKING SPACE; when encoding, they do not write byte-order marks.
- When decoding, the `UTF-16` charset interprets the byte-order mark at the beginning of the input stream to indicate the byte-order of the stream but defaults to big-endian if there is no byte-order mark; when encoding, it uses big-endian byte order and writes a big-endian byte-order mark.

In any case, byte order marks occurring after the first element of an input sequence are not omitted since the same code is used to represent ZERO-WIDTH NON-BREAKING SPACE.

Android note: The Android platform default is always UTF-8.

The StandardCharsets class defines constants for each of the standard charsets.

## Terminology

The name of this class is taken from the terms used in [*RFC 2278*](http://www.ietf.org/rfc/rfc2278.txt). In that document a *charset* is defined as the combination of one or more coded character sets and a character-encoding scheme. (This definition is confusing; some other software systems define *charset* as a synonym for *coded character set*.)

A *coded character set* is a mapping between a set of abstract characters and a set of integers. US-ASCII, ISO 8859-1, JIS X 0201, and Unicode are examples of coded character sets.

Some standards have defined a *character set* to be simply a set of abstract characters without an associated assigned numbering. An alphabet is an example of such a character set. However, the subtle distinction between *character set* and *coded character set* is rarely used in practice; the former has become a short form for the latter, including in the Java API specification.

A *character-encoding scheme* is a mapping between one or more coded character sets and a set of octet (eight-bit byte) sequences. UTF-8, UTF-16, ISO 2022, and EUC are examples of character-encoding schemes. Encoding schemes are often associated with a particular coded character set; UTF-8, for example, is used only to encode Unicode. Some schemes, however, are associated with multiple coded character sets; EUC, for example, can be used to encode characters in a variety of Asian coded character sets.

When a coded character set is used exclusively with a single character-encoding scheme then the corresponding charset is usually named for the coded character set; otherwise a charset is usually named for the encoding scheme and, possibly, the locale of the coded character sets that it supports. Hence `US-ASCII` is both the name of a coded character set and of the charset that encodes it, while `EUC-JP` is the name of the charset that encodes the JIS X 0201, JIS X 0208, and JIS X 0212 coded character sets for the Japanese language.

The native character encoding of the Java programming language is UTF-16. A charset in the Java platform therefore defines a mapping between sequences of sixteen-bit UTF-16 code units (that is, sequences of chars) and sequences of bytes.

## Summary

| Protected constructors ||
|---|---|
| Charset Initializes a new charset with the given canonical name and alias set. |

| Public methods ||
|---|---|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | aliases Returns a set containing this charset's aliases. |
| open static [SortedMap](../java.util/SortedMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Charset](Charset.md)!\>! | availableCharsets Constructs a sorted map from canonical charset names to charset objects. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canEncode Tells whether or not this charset supports encoding. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares this charset to another. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Tells whether or not this charset contains the given charset. |
| [CharBuffer](../java.nio/CharBuffer.md)! | decode Convenience method that decodes bytes in this charset into Unicode characters. |
| --- | --- |
| open static [Charset](Charset.md)! | defaultCharset Returns the default charset of this Java virtual machine. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | displayName Returns this charset's human-readable name for the default locale. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | displayName Returns this charset's human-readable name for the given locale. |
| --- | --- |
| [ByteBuffer](../java.nio/ByteBuffer.md)! | encode Convenience method that encodes a string into bytes in this charset. |
| [ByteBuffer](../java.nio/ByteBuffer.md)! | encode Convenience method that encodes Unicode characters into bytes in this charset. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Tells whether or not this object is equal to another. |
| --- | --- |
| open static [Charset](Charset.md)! | forName Returns a charset object for the named charset. |
| open static [Charset](Charset.md)! | forName Returns a charset object for the named charset. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Computes a hashcode for this charset. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRegistered Tells whether or not this charset is registered in the [IANA Charset Registry](http://www.iana.org/assignments/character-sets). |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSupported Tells whether the named charset is supported. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | name Returns this charset's canonical name. |
| --- | --- |
| abstract [CharsetDecoder](CharsetDecoder.md)! | newDecoder Constructs a new decoder for this charset. |
| abstract [CharsetEncoder](CharsetEncoder.md)! | newEncoder Constructs a new encoder for this charset. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string describing this charset. |
| --- | --- |

## Protected constructors

### Charset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected Charset(
    canonicalName: String!, 
    aliases: Array<String!>!)
```

Initializes a new charset with the given canonical name and alias set.

| Parameters ||
|---|---|
| `canonicalName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The canonical name of this charset |
| `aliases` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: An array of this charset's aliases, or null if it has no aliases |

| Exceptions ||
|---|---|
| `java.nio.charset.IllegalCharsetNameException` | If the canonical name or any of the aliases are illegal |

## Public methods

### aliases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun aliases(): MutableSet<String!>!
```

Returns a set containing this charset's aliases.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | An immutable set of this charset's aliases |

### availableCharsets

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun availableCharsets(): SortedMap<String!, Charset!>!
```

Constructs a sorted map from canonical charset names to charset objects.

The map returned by this method will have one entry for each charset for which support is available in the current Java virtual machine. If two or more supported charsets have the same canonical name then the resulting map will contain just one of them; which one it will contain is not specified.

The invocation of this method, and the subsequent use of the resulting map, may cause time-consuming disk or network I/O operations to occur. This method is provided for applications that need to enumerate all of the available charsets, for example to allow user charset selection. This method is not used by the #forName method, which instead employs an efficient incremental lookup algorithm.

This method may return different results at different times if new charset providers are dynamically made available to the current Java virtual machine. In the absence of such changes, the charsets returned by this method are exactly those that can be retrieved via the #forName method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/SortedMap.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://developer.android.com/reference/kotlin/java/nio/charset/Charset#!>!` | An immutable, case-insensitive map from canonical charset names to charset objects |

### canEncode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canEncode(): Boolean
```

Tells whether or not this charset supports encoding.

Nearly all charsets support encoding. The primary exceptions are special-purpose *auto-detect* charsets whose decoders can determine which of several possible encoding schemes is in use by examining the input byte sequence. Such charsets do not support encoding because there is no way to determine which encoding should be used on output. Implementations of such charsets should override this method to return `false`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this charset supports encoding |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: Charset!): Int
```

Compares this charset to another.

Charsets are ordered by their canonical names, without regard to case.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `that` | The charset to which this charset is to be compared |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A negative integer, zero, or a positive integer as this charset is less than, equal to, or greater than the specified charset |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun contains(cs: Charset!): Boolean
```

Tells whether or not this charset contains the given charset.

A charset *C* is said to *contain* a charset *D* if, and only if, every character representable in *D* is also representable in *C* . If this relationship holds then it is guaranteed that every string that can be encoded in *D* can also be encoded in *C* without performing any replacements.

That *C* contains *D* does not imply that each character representable in *C* by a particular byte sequence is represented in *D* by the same byte sequence, although sometimes this is the case.

Every charset contains itself.

This method computes an approximation of the containment relation: If it returns `true` then the given charset is known to be contained by this charset; if it returns `false`, however, then it is not necessarily the case that the given charset is not contained in this charset.

| Parameters ||
|---|---|
| `cs` | [Charset](Charset.md)!: The given charset |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given charset is contained in this charset |

### decode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun decode(bb: ByteBuffer!): CharBuffer!
```

Convenience method that decodes bytes in this charset into Unicode characters.

An invocation of this method upon a charset `cs` returns the same result as the expression

```kotlin
cs.newDecoder()
        .onMalformedInput(CodingErrorAction.REPLACE)
        .onUnmappableCharacter(CodingErrorAction.REPLACE)
        .decode(bb); 
```
except that it is potentially more efficient because it can cache decoders between successive invocations.

This method always replaces malformed-input and unmappable-character sequences with this charset's default replacement byte array. In order to detect such sequences, use the decode method directly.

| Parameters ||
|---|---|
| `bb` | [ByteBuffer](../java.nio/ByteBuffer.md)!: The byte buffer to be decoded |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/CharBuffer.html#!` | A char buffer containing the decoded characters |

### defaultCharset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun defaultCharset(): Charset!
```

Returns the default charset of this Java virtual machine.

Android note: The Android platform default is always UTF-8.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/Charset#!` | A charset object for the default charset |

### displayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun displayName(): String!
```

Returns this charset's human-readable name for the default locale.

The default implementation of this method simply returns this charset's canonical name. Concrete subclasses of this class may override this method in order to provide a localized display name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The display name of this charset in the default locale |

### displayName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun displayName(locale: Locale!): String!
```

Returns this charset's human-readable name for the given locale.

The default implementation of this method simply returns this charset's canonical name. Concrete subclasses of this class may override this method in order to provide a localized display name.

| Parameters ||
|---|---|
| `locale` | [Locale](../java.util/Locale.md)!: The locale for which the display name is to be retrieved |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The display name of this charset in the given locale |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun encode(str: String!): ByteBuffer!
```

Convenience method that encodes a string into bytes in this charset.

An invocation of this method upon a charset `cs` returns the same result as the expression

```kotlin
cs.encode(CharBuffer.wrap(s)); 
```

| Parameters ||
|---|---|
| `str` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The string to be encoded |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!` | A byte buffer containing the encoded characters |

### encode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun encode(cb: CharBuffer!): ByteBuffer!
```

Convenience method that encodes Unicode characters into bytes in this charset.

An invocation of this method upon a charset `cs` returns the same result as the expression

```kotlin
cs.newEncoder()
        .onMalformedInput(CodingErrorAction.REPLACE)
        .onUnmappableCharacter(CodingErrorAction.REPLACE)
        .encode(bb); 
```
except that it is potentially more efficient because it can cache encoders between successive invocations.

This method always replaces malformed-input and unmappable-character sequences with this charset's default replacement string. In order to detect such sequences, use the encode method directly.

| Parameters ||
|---|---|
| `cb` | [CharBuffer](../java.nio/CharBuffer.md)!: The char buffer to be encoded |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#!` | A byte buffer containing the encoded characters |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Tells whether or not this object is equal to another.

Two charsets are equal if, and only if, they have the same canonical names. A charset is never equal to any other type of object.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this charset is equal to the given object |

### forName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun forName(charsetName: String!): Charset!
```

Returns a charset object for the named charset.

| Parameters ||
|---|---|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the requested charset; may be either a canonical name or an alias |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/Charset#!` | A charset object for the named charset |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given `charsetName` is null |
| `java.nio.charset.IllegalCharsetNameException` | If the given charset name is illegal |
| `java.nio.charset.UnsupportedCharsetException` | If no support for the named charset is available in this instance of the Java virtual machine |
| --- | --- |

### forName

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun forName(
    charsetName: String!, 
    fallback: Charset!
): Charset!
```

Returns a charset object for the named charset. If the charset object for the named charset is not available or `charsetName` is not a legal charset name, then `fallback` is returned.

| Parameters ||
|---|---|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the requested charset; may be either a canonical name or an alias |
| `fallback` | [Charset](Charset.md)!: fallback charset in case the charset object for the named charset is not available or `charsetName` is not a legal charset name. May be `null` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/Charset#!` | A charset object for the named charset, or `fallback` in case the charset object for the named charset is not available or `charsetName` is not a legal charset name |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given `charsetName` is `null` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Computes a hashcode for this charset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer hashcode |

### isRegistered

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRegistered(): Boolean
```

Tells whether or not this charset is registered in the [IANA Charset Registry](http://www.iana.org/assignments/character-sets).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this charset is known by its implementor to be registered with the IANA |

### isSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isSupported(charsetName: String!): Boolean
```

Tells whether the named charset is supported.

| Parameters ||
|---|---|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the requested charset; may be either a canonical name or an alias |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, support for the named charset is available in the current Java virtual machine |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given `charsetName` is null |
| `java.nio.charset.IllegalCharsetNameException` | If the given charset name is illegal |

### name

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun name(): String!
```

Returns this charset's canonical name.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The canonical name of this charset |

### newDecoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun newDecoder(): CharsetDecoder!
```

Constructs a new decoder for this charset.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetDecoder!` | A new decoder for this charset |

### newEncoder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun newEncoder(): CharsetEncoder!
```

Constructs a new encoder for this charset.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/charset/CharsetEncoder!` | A new encoder for this charset |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | If this charset does not support encoding |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string describing this charset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string describing this charset |
