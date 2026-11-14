# SNIHostName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SNIHostName

```
class SNIHostName : SNIServerName
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [javax.net.ssl.SNIServerName](SNIServerName.md) ||
| | ↳ | [javax.net.ssl.SNIHostName](SNIHostName.md) |

Instances of this class represent a server name of type [host_name](StandardConstants.md) in a Server Name Indication (SNI) extension.

As described in section 3, "Server Name Indication", of [TLS Extensions (RFC 6066)](http://www.ietf.org/rfc/rfc6066.txt), "HostName" contains the fully qualified DNS hostname of the server, as understood by the client. The encoded server name value of a hostname is represented as a byte string using ASCII encoding without a trailing dot. This allows the support of Internationalized Domain Names (IDN) through the use of A-labels (the ASCII-Compatible Encoding (ACE) form of a valid string of Internationalized Domain Names for Applications (IDNA)) defined in [RFC 5890](http://www.ietf.org/rfc/rfc5890.txt).

Note that`SNIHostName`objects are immutable.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SNIHostName](SNIHostName.md))`(`encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an`SNIHostName`using the specified encoded value. |
| [SNIHostName](SNIHostName.md))`(`hostname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an`SNIHostName`using the specified hostname. |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [SNIMatcher](SNIMatcher.md)! | [createSNIMatcher](SNIHostName.md))`(`regex:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an [SNIMatcher](SNIMatcher.md) object for`SNIHostName`s. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](SNIHostName.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this server name to the specified object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAsciiName](SNIHostName.md))`()` Returns the [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant hostname of this`SNIHostName`object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](SNIHostName.md))`()` Returns a hash code value for this`SNIHostName`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SNIHostName.md))`()` Returns a string representation of the object, including the DNS hostname in this`SNIHostName`object. |

| Inherited functions ||
|---|---|
| From class [SNIServerName](SNIServerName.md) |------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](SNIServerName.md))`()` <br /> Returns a copy of the encoded server name value of this server name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](SNIServerName.md))`()` <br /> Returns the name type of this server name. <br /> | ||

## Public constructors

### SNIHostName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SNIHostName(encoded: ByteArray!)
```

Creates an`SNIHostName`using the specified encoded value.

This method is normally used to parse the encoded name value in a requested SNI extension.

Per [RFC 6066](http://www.ietf.org/rfc/rfc6066.txt), the encoded name value of a hostname is [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant. However, in the previous version of the SNI extension ([RFC 4366](http://www.ietf.org/rfc/rfc4366.txt)), the encoded hostname is represented as a byte string using UTF-8 encoding. For the purpose of version tolerance, this method allows that the charset of`encoded`argument can be [StandardCharsets.UTF_8](../java.nio.charset/StandardCharsets.md), as well as [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md). [IDN.toASCII(String)](../java.net/IDN.md))is used to translate the`encoded`argument into ASCII Compatible Encoding (ACE) hostname.

It is strongly recommended that this constructor is only used to parse the encoded name value in a requested SNI extension. Otherwise, to comply with [RFC 6066](http://www.ietf.org/rfc/rfc6066.txt), please always use [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant charset and enforce the restrictions on ASCII characters in hostnames (see [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt), [RFC 1122](http://www.ietf.org/rfc/rfc1122.txt), [RFC 1123](http://www.ietf.org/rfc/rfc1123.txt)) for`encoded`argument, or use [SNIHostName.SNIHostName(String)](SNIHostName.md))instead.

The`encoded`argument is illegal if it:

- `encoded`is empty,
- `encoded`ends with a trailing dot,
- `encoded`is not encoded in [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md) or [StandardCharsets.UTF_8](../java.nio.charset/StandardCharsets.md)-compliant charset,
- `encoded`is not a valid Internationalized Domain Name (IDN) compliant with the RFC 3490 specification.

Note that the`encoded`byte array is cloned to protect against subsequent modification.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded hostname of this server name |

| Exceptions ||
|--------------------------------------|-----------------------|
| `java.lang.NullPointerException` | if`encoded`is`null` |
| `java.lang.IllegalArgumentException` | if`encoded`is illegal |

### SNIHostName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SNIHostName(hostname: String!)
```

Creates an`SNIHostName`using the specified hostname.

Note that per [RFC 6066](http://www.ietf.org/rfc/rfc6066.txt), the encoded server name value of a hostname is [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant. In this method,`hostname`can be a user-friendly Internationalized Domain Name (IDN). [IDN.toASCII(String, int)](../java.net/IDN.md))is used to enforce the restrictions on ASCII characters in hostnames (see [RFC 3490](http://www.ietf.org/rfc/rfc3490.txt), [RFC 1122](http://www.ietf.org/rfc/rfc1122.txt), [RFC 1123](http://www.ietf.org/rfc/rfc1123.txt)) and translate the`hostname`into ASCII Compatible Encoding (ACE), as: 

```kotlin
IDN.toASCII(hostname, IDN.USE_STD3_ASCII_RULES);
  
```

The`hostname`argument is illegal if it:

- `hostname`is empty,
- `hostname`ends with a trailing dot,
- `hostname`is not a valid Internationalized Domain Name (IDN) compliant with the RFC 3490 specification.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the hostname of this server name |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.NullPointerException` | if`hostname`is`null` |
| `java.lang.IllegalArgumentException` | if`hostname`is illegal |

## Public methods

### createSNIMatcher

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createSNIMatcher(regex: String!): SNIMatcher!
```

Creates an [SNIMatcher](SNIMatcher.md) object for`SNIHostName`s.

This method can be used by a server to verify the acceptable`SNIHostName`s. For example, 

```kotlin
SNIMatcher matcher =
          SNIHostName.createSNIMatcher("www\\.example\\.com");
  
```
will accept the hostname "www.example.com". 

```kotlin
SNIMatcher matcher =
          SNIHostName.createSNIMatcher("www\\.example\\.(com|org)");
  
```
will accept hostnames "www.example.com" and "www.example.org".

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `regex` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the [regular expression pattern](https://developer.android.com//java/util/regex/Pattern.html#sum) representing the hostname(s) to match |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------|
| [SNIMatcher](SNIMatcher.md)! | a`SNIMatcher`object for`SNIHostName`s |

| Exceptions ||
|------------------------------------------|-----------------------------------------------|
| `java.lang.NullPointerException` | if`regex`is`null` |
| `java.util.regex.PatternSyntaxException` | if the regular expression's syntax is invalid |

### equals

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this server name to the specified object.

Per [RFC 6066](http://www.ietf.org/rfc/rfc6066.txt), DNS hostnames are case-insensitive. Two server hostnames are equal if, and only if, they have the same name type, and the hostnames are equal in a case-independent comparison.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the other server name object to compare with. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if, and only if, the`other`is considered equal to this instance |

### getAsciiName

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAsciiName(): String!
```

Returns the [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant hostname of this`SNIHostName`object.

Note that, per [RFC 6066](http://www.ietf.org/rfc/rfc6066.txt), the returned hostname may be an internationalized domain name that contains A-labels. See [RFC 5890](http://www.ietf.org/rfc/rfc5890.txt) for more information about the detailed A-label specification.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the [StandardCharsets.US_ASCII](../java.nio.charset/StandardCharsets.md)-compliant hostname of this`SNIHostName`object |

### hashCode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code value for this`SNIHostName`.

The hash code value is generated using the case-insensitive hostname of this`SNIHostName`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this`SNIHostName`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object, including the DNS hostname in this`SNIHostName`object.

The exact details of the representation are unspecified and subject to change, but the following may be regarded as typical: 

```kotlin
"type=host_name (0), value=<hostname>"
  
```
The "\<hostname\>" is an ASCII representation of the hostname, which may contains A-labels. For example, a returned value of an pseudo hostname may look like: 

```kotlin
"type=host_name (0), value=www.example.com"
  
```
or 

```kotlin
"type=host_name (0), value=xn--fsqu00a.xn--0zwm56d"
  
```

Please NOTE that the exact details of the representation are unspecified and subject to change.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
