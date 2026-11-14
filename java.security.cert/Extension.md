# Extension

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Extension

```
interface Extension
```

| [java.security.cert.Extension](Extension.md) |

This interface represents an X.509 extension.

Extensions provide a means of associating additional attributes with users or public keys and for managing a certification hierarchy. The extension format also allows communities to define private extensions to carry information unique to those communities.

Each extension contains an object identifier, a criticality setting indicating whether it is a critical or a non-critical extension, and and an ASN.1 DER-encoded value. Its ASN.1 definition is: 

```kotlin
Extension ::= SEQUENCE {
          extnId        OBJECT IDENTIFIER,
          critical      BOOLEAN DEFAULT FALSE,
          extnValue     OCTET STRING
                  -- contains a DER encoding of a value
                  -- of the type registered for use with
                  -- the extnId object identifier value
      }
 
  
```

This interface is designed to provide access to a single extension, unlike [java.security.cert.X509Extension](X509Extension.md) which is more suitable for accessing a set of extensions.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [encode](Extension.md))`(`out:` ` [OutputStream](../java.io/OutputStream.md)!`)` Generates the extension's DER encoding and writes it to the output stream. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getId](Extension.md))`()` Gets the extensions's object identifier. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getValue](Extension.md))`()` Gets the extensions's DER-encoded value. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCritical](Extension.md))`()` Gets the extension's criticality setting. |

## Public methods

### encode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun encode(out: OutputStream!): Unit
```

Generates the extension's DER encoding and writes it to the output stream.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `out` | [OutputStream](../java.io/OutputStream.md)!:the output stream |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.io.IOException` | on encoding or output error. |
| `java.lang.NullPointerException` | if`out`is`null`. |

### getId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getId(): String!
```

Gets the extensions's object identifier.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the object identifier as a String |

### getValue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(): ByteArray!
```

Gets the extensions's DER-encoded value. Note, this is the bytes that are encoded as an OCTET STRING. It does not include the OCTET STRING tag and length.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a copy of the extension's value, or`null`if no extension value is present. |

### isCritical

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCritical(): Boolean
```

Gets the extension's criticality setting.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is a critical extension. |
