# PKCS12Attribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKCS12Attribute

```
class PKCS12Attribute : KeyStore.Entry.Attribute
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.PKCS12Attribute](../java/security/PKCS12Attribute.md) |

An attribute associated with a PKCS12 keystore entry. The attribute name is an ASN.1 Object Identifier and the attribute value is a set of ASN.1 types.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKCS12Attribute](../java/security/PKCS12Attribute.md))`(`encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs a PKCS12 attribute from its ASN. |
| [PKCS12Attribute](../java/security/PKCS12Attribute.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a PKCS12 attribute from its name and value. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/security/PKCS12Attribute.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`PKCS12Attribute`and a specified object for equality. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java/security/PKCS12Attribute.md))`()` Returns the attribute's ASN. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/PKCS12Attribute.md))`()` Returns the attribute's ASN. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getValue](../java/security/PKCS12Attribute.md))`()` Returns the attribute's ASN. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/security/PKCS12Attribute.md))`()` Returns the hashcode for this`PKCS12Attribute`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/PKCS12Attribute.md))`()` Returns a string representation of this`PKCS12Attribute`. |
| --- | --- |

## Public constructors

### PKCS12Attribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKCS12Attribute(encoded: ByteArray!)
```

Constructs a PKCS12 attribute from its ASN.1 DER encoding. The DER encoding is specified by the following ASN.1 definition: 

```kotlin
Attribute ::= SEQUENCE {
      type   AttributeType,
      values SET OF AttributeValue
  }
  AttributeType ::= OBJECT IDENTIFIER
  AttributeValue ::= ANY defined by type
 
  
```

<br />

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the attribute's ASN.1 DER encoding. It is cloned to prevent subsequent modificaion. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if`encoded`is`null` |
| `java.lang.IllegalArgumentException` | if`encoded`is incorrectly formatted |

### PKCS12Attribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKCS12Attribute(
    name: String!, 
    value: String!)
```

Constructs a PKCS12 attribute from its name and value. The name is an ASN.1 Object Identifier represented as a list of dot-separated integers. A string value is represented as the string itself. A binary value is represented as a string of colon-separated pairs of hexadecimal digits. Multi-valued attributes are represented as a comma-separated list of values, enclosed in square brackets. See[Arrays.toString(java.lang.Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays.html#toString(kotlin.Array)).

A string value will be DER-encoded as an ASN.1 UTF8String and a binary value will be DER-encoded as an ASN.1 Octet String.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute's identifier |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute's value |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.NullPointerException` | if`name`or`value`is`null` |
| `java.lang.IllegalArgumentException` | if`name`or`value`is incorrectly formatted |

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`PKCS12Attribute`and a specified object for equality.

| Parameters ||
|-------|-----------------------|
| `obj` | the comparison object |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if`obj`is a`PKCS12Attribute`and their DER encodings are equal. |

### getEncoded

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(): ByteArray!
```

Returns the attribute's ASN.1 DER encoding.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a clone of the attribute's DER encoding |

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

Returns the attribute's ASN.1 Object Identifier represented as a list of dot-separated integers.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the attribute's identifier |

### getValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getValue(): String!
```

Returns the attribute's ASN.1 DER-encoded value as a string. An ASN.1 DER-encoded value is returned in one of the following`String`formats:

- the DER encoding of a basic ASN.1 type that has a natural string representation is returned as the string itself. Such types are currently limited to BOOLEAN, INTEGER, OBJECT IDENTIFIER, UTCTime, GeneralizedTime and the following six ASN.1 string types: UTF8String, PrintableString, T61String, IA5String, BMPString and GeneralString.
- the DER encoding of any other ASN.1 type is not decoded but returned as a binary string of colon-separated pairs of hexadecimal digits.

Multi-valued attributes are represented as a comma-separated list of values, enclosed in square brackets. See[Arrays.toString(java.lang.Object[])](https://developer.android.com/reference/kotlin/java/util/Arrays.html#toString(kotlin.Array)).

<br />

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the attribute value's string encoding |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hashcode for this`PKCS12Attribute`. The hash code is computed from its DER encoding.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of this`PKCS12Attribute`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a name/value pair separated by an 'equals' symbol |
