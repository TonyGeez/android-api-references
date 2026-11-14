# X500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X500Principal

```
class X500Principal : Principal, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.security.auth.x500.X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#) |

This class represents an X.500`Principal`.`X500Principal`s are represented by distinguished names such as "CN=Duke, OU=JavaSoft, O=Sun Microsystems, C=US".

This class can be instantiated by using a string representation of the distinguished name, or by using the ASN.1 DER encoded byte representation of the distinguished name. The current specification for the string representation of a distinguished name is defined in [RFC 2253: Lightweight Directory Access Protocol (v3): UTF-8 String Representation of Distinguished Names](http://www.ietf.org/rfc/rfc2253.txt). This class, however, accepts string formats from both RFC 2253 and [RFC 1779: A String Representation of Distinguished Names](http://www.ietf.org/rfc/rfc1779.txt), and also recognizes attribute type keywords whose OIDs (Object Identifiers) are defined in [RFC 3280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://www.ietf.org/rfc/rfc3280.txt).

The string representation for this`X500Principal`can be obtained by calling the`getName`methods.

Note that the`getSubjectX500Principal`and`getIssuerX500Principal`methods of`X509Certificate`return X500Principals representing the issuer and subject fields of the certificate.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CANONICAL](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#CANONICAL:kotlin.String) Canonical String format of Distinguished Names. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RFC1779](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#RFC1779:kotlin.String) RFC 1779 String format of Distinguished Names. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RFC2253](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#RFC2253:kotlin.String) RFC 2253 String format of Distinguished Names. |
| --- | --- |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.ByteArray))`(`name:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an`X500Principal`from a distinguished name in ASN. |
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(java.io.InputStream))`(`is:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Creates an`X500Principal`from an`InputStream`containing the distinguished name in ASN. |
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an`X500Principal`from a string representation of an X. |
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.String,%20kotlin.collections.MutableMap))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `keywordMap:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Creates an`X500Principal`from a string representation of an X. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified`Object`with this`X500Principal`for equality. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getEncoded())`()` Returns the distinguished name in ASN. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getName())`()` Returns a string representation of the X. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getName(kotlin.String))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a string representation of the X. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getName(kotlin.String,%20kotlin.collections.MutableMap))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `oidMap:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Returns a string representation of the X. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#hashCode())`()` Return a hash code for this`X500Principal`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#toString())`()` Return a user-friendly string representation of this`X500Principal`. |

| Inherited functions ||
|---|---|
| From class [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Principal.html#implies(javax.security.auth.Subject))`(`subject:` ` [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject.html#)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

## Constants

### CANONICAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CANONICAL: String
```

Canonical String format of Distinguished Names. 

 Value: "CANONICAL"

### RFC1779

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RFC1779: String
```

RFC 1779 String format of Distinguished Names. 

 Value: "RFC1779"

### RFC2253

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RFC2253: String
```

RFC 2253 String format of Distinguished Names. 

 Value: "RFC2253"

## Public constructors

### X500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500Principal(name: ByteArray!)
```

Creates an`X500Principal`from a distinguished name in ASN.1 DER encoded form. The ASN.1 notation for this structure is as follows. 

```kotlin
<code>Name ::= CHOICE {
    RDNSequence }
 
  RDNSequence ::= SEQUENCE OF RelativeDistinguishedName
 
  RelativeDistinguishedName ::=
    SET SIZE (1 .. MAX) OF AttributeTypeAndValue
 
  AttributeTypeAndValue ::= SEQUENCE {
    type     AttributeType,
    value    AttributeValue }
 
  AttributeType ::= OBJECT IDENTIFIER
 
  AttributeValue ::= ANY DEFINED BY AttributeType
  ....
  DirectoryString ::= CHOICE {
        teletexString           TeletexString (SIZE (1..MAX)),
        printableString         PrintableString (SIZE (1..MAX)),
        universalString         UniversalString (SIZE (1..MAX)),
        utf8String              UTF8String (SIZE (1.. MAX)),
        bmpString               BMPString (SIZE (1..MAX)) }
  </code>
```

<br />

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the distinguished name in ASN.1 DER encoded form |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if an encoding error occurs (incorrect form for DN) |

### X500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500Principal(is: InputStream!)
```

Creates an`X500Principal`from an`InputStream`containing the distinguished name in ASN.1 DER encoded form. The ASN.1 notation for this structure is supplied in the documentation for[X500Principal(byte[] name)](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.ByteArray)).

The read position of the input stream is positioned to the next available byte after the encoded distinguished name.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `is` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an`InputStream`containing the distinguished name in ASN.1 DER encoded form |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if the`InputStream`is`null` |
| `java.lang.IllegalArgumentException` | if an encoding error occurs (incorrect form for DN) |

### X500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500Principal(name: String!)
```

Creates an`X500Principal`from a string representation of an X.500 distinguished name (ex: "CN=Duke, OU=JavaSoft, O=Sun Microsystems, C=US"). The distinguished name must be specified using the grammar defined in RFC 1779 or RFC 2253 (either format is acceptable).

This constructor recognizes the attribute type keywords defined in RFC 1779 and RFC 2253 (and listed in [getName(String format)](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getName(kotlin.String))), as well as the T, DNQ or DNQUALIFIER, SURNAME, GIVENNAME, INITIALS, GENERATION, EMAILADDRESS, and SERIALNUMBER keywords whose Object Identifiers (OIDs) are defined in RFC 3280 and its successor. Any other attribute type must be specified as an OID.

This implementation enforces a more restrictive OID syntax than defined in RFC 1779 and 2253. It uses the more correct syntax defined in [RFC 4512](http://www.ietf.org/rfc/rfc4512.txt), which specifies that OIDs contain at least 2 digits:

`numericoid = number 1*( DOT number ) `

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an X.500 distinguished name in RFC 1779 or RFC 2253 format |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the`name`is`null` |
| `java.lang.IllegalArgumentException` | if the`name`is improperly specified |

### X500Principal

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X500Principal(
    name: String!, 
    keywordMap: MutableMap<String!, String!>!)
```

Creates an`X500Principal`from a string representation of an X.500 distinguished name (ex: "CN=Duke, OU=JavaSoft, O=Sun Microsystems, C=US"). The distinguished name must be specified using the grammar defined in RFC 1779 or RFC 2253 (either format is acceptable).

This constructor recognizes the attribute type keywords specified in [X500Principal(java.lang.String)](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.String))and also recognizes additional keywords that have entries in the`keywordMap`parameter. Keyword entries in the keywordMap take precedence over the default keywords recognized by`X500Principal(String)`. Keywords MUST be specified in all upper-case, otherwise they will be ignored. Improperly specified keywords are ignored; however if a keyword in the name maps to an improperly specified Object Identifier (OID), an`IllegalArgumentException`is thrown. It is permissible to have 2 different keywords that map to the same OID.

This implementation enforces a more restrictive OID syntax than defined in RFC 1779 and 2253. It uses the more correct syntax defined in [RFC 4512](http://www.ietf.org/rfc/rfc4512.txt), which specifies that OIDs contain at least 2 digits:

`numericoid = number 1*( DOT number ) `

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:an X.500 distinguished name in RFC 1779 or RFC 2253 format |
| `keywordMap` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an attribute type keyword map, where each key is a keyword String that maps to a corresponding object identifier in String form (a sequence of nonnegative integers separated by periods). The map may be empty but never`null`. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`name`or`keywordMap`is`null` |
| `java.lang.IllegalArgumentException` | if the`name`is improperly specified or a keyword in the`name`maps to an OID that is not in the correct form |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares the specified`Object`with this`X500Principal`for equality.

Specifically, this method returns`true`if the`Object`*o* is an`X500Principal`and if the respective canonical string representations (obtained via the`getName(X500Principal.CANONICAL)`method) of this object and*o*are equal.

This implementation is compliant with the requirements of RFC 3280.

| Parameters ||
|-----------|-------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `another` | principal to compare with. |
| `o` | Object to be compared for equality with this`X500Principal` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified`Object`is equal to this`X500Principal`,`false`otherwise |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(): ByteArray!
```

Returns the distinguished name in ASN.1 DER encoded form. The ASN.1 notation for this structure is supplied in the documentation for[X500Principal(byte[] name)](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#X500Principal(kotlin.ByteArray)).

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the distinguished name in ASN.1 DER encoded form |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns a string representation of the X.500 distinguished name using the format defined in RFC 2253.

This method is equivalent to calling`getName(X500Principal.RFC2253)`.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the distinguished name of this`X500Principal` |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(format: String!): String!
```

Returns a string representation of the X.500 distinguished name using the specified format. Valid values for the format are "RFC1779", "RFC2253", and "CANONICAL" (case insensitive).

If "RFC1779" is specified as the format, this method emits the attribute type keywords defined in RFC 1779 (CN, L, ST, O, OU, C, STREET). Any other attribute type is emitted as an OID.

If "RFC2253" is specified as the format, this method emits the attribute type keywords defined in RFC 2253 (CN, L, ST, O, OU, C, STREET, DC, UID). Any other attribute type is emitted as an OID. Under a strict reading, RFC 2253 only specifies a UTF-8 string representation. The String returned by this method is the Unicode string achieved by decoding this UTF-8 representation.

If "CANONICAL" is specified as the format, this method returns an RFC 2253 conformant string representation with the following additional canonicalizations:

1. Leading zeros are removed from attribute types that are encoded as dotted decimal OIDs
2. DirectoryString attribute values of type PrintableString and UTF8String are not output in hexadecimal format
3. DirectoryString attribute values of types other than PrintableString and UTF8String are output in hexadecimal format
4. Leading and trailing white space characters are removed from non-hexadecimal attribute values (unless the value consists entirely of white space characters)
5. Internal substrings of one or more white space characters are converted to a single space in non-hexadecimal attribute values
6. Relative Distinguished Names containing more than one Attribute Value Assertion (AVA) are output in the following order: an alphabetical ordering of AVAs containing standard keywords, followed by a numeric ordering of AVAs containing OID keywords.
7. The only characters in attribute values that are escaped are those which section 2.4 of RFC 2253 states must be escaped (they are escaped using a preceding backslash character)
8. The entire name is converted to upper case using`String.toUpperCase(Locale.US)`
9. The entire name is converted to lower case using`String.toLowerCase(Locale.US)`
10. The name is finally normalized using normalization form KD, as described in the Unicode Standard and UAX #15

Additional standard formats may be introduced in the future.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the format to use |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of this`X500Principal`using the specified format |

| Exceptions ||
|--------------------------------------|--------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified format is invalid or null |

### getName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(
    format: String!, 
    oidMap: MutableMap<String!, String!>!
): String!
```

Returns a string representation of the X.500 distinguished name using the specified format. Valid values for the format are "RFC1779" and "RFC2253" (case insensitive). "CANONICAL" is not permitted and an`IllegalArgumentException`will be thrown.

This method returns Strings in the format as specified in [getName(java.lang.String)](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal#getName(kotlin.String))and also emits additional attribute type keywords for OIDs that have entries in the`oidMap`parameter. OID entries in the oidMap take precedence over the default OIDs recognized by`getName(String)`. Improperly specified OIDs are ignored; however if an OID in the name maps to an improperly specified keyword, an`IllegalArgumentException`is thrown.

Additional standard formats may be introduced in the future.

Warning: additional attribute type keywords may not be recognized by other implementations; therefore do not use this method if you are unsure if these keywords will be recognized by other implementations.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the format to use |
| `oidMap` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:an OID map, where each key is an object identifier in String form (a sequence of nonnegative integers separated by periods) that maps to a corresponding attribute type keyword String. The map may be empty but never`null`. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of this`X500Principal`using the specified format |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified format is invalid, null, or an OID in the name maps to an improperly specified keyword |
| `java.lang.NullPointerException` | if`oidMap`is`null` |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Return a hash code for this`X500Principal`.

The hash code is calculated via:`getName(X500Principal.CANONICAL).hashCode()`

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code for this`X500Principal` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Return a user-friendly string representation of this`X500Principal`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this`X500Principal` |
