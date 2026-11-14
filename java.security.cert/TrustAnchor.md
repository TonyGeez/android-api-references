# TrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustAnchor

```
open class TrustAnchor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#) |

A trust anchor or most-trusted Certification Authority (CA).

This class represents a "most-trusted CA", which is used as a trust anchor for validating X.509 certification paths. A most-trusted CA includes the public key of the CA, the CA's name, and any constraints upon the set of paths which may be validated using this key. These parameters can be specified in the form of a trusted`X509Certificate`or as individual parameters.

**Concurrent Access**

All`TrustAnchor`objects must be immutable and thread-safe. That is, multiple threads may concurrently invoke the methods defined in this class on a single`TrustAnchor`object (or more than one) with no ill effects. Requiring`TrustAnchor`objects to be immutable and thread-safe allows them to be passed around to various pieces of code without worrying about coordinating access. This stipulation applies to all public fields and methods of this class and any added or overridden by subclasses.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(kotlin.String,%20java.security.PublicKey,%20kotlin.ByteArray))`(`caName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `pubKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!`, `nameConstraints:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an instance of`TrustAnchor`where the most-trusted CA is specified as a distinguished name and public key. |
| [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(java.security.cert.X509Certificate,%20kotlin.ByteArray))`(`trustedCert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)!`, `nameConstraints:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an instance of`TrustAnchor`with the specified`X509Certificate`and optional name constraints, which are intended to be used as additional constraints when validating an X. |
| [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(javax.security.auth.x500.X500Principal,%20java.security.PublicKey,%20kotlin.ByteArray))`(`caPrincipal:` ` [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!`, `pubKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!`, `nameConstraints:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an instance of`TrustAnchor`where the most-trusted CA is specified as an X500Principal and public key. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | [getCA](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#getCA())`()` Returns the name of the most-trusted CA as an X500Principal. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCAName](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#getCAName())`()` Returns the name of the most-trusted CA in RFC 2253`String`format. |
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)! | [getCAPublicKey](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#getCAPublicKey())`()` Returns the public key of the most-trusted CA. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getNameConstraints](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#getNameConstraints())`()` Returns the name constraints parameter. |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)! | [getTrustedCert](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#getTrustedCert())`()` Returns the most-trusted CA certificate. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#toString())`()` Returns a formatted string describing the`TrustAnchor`. |

## Public constructors

### TrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrustAnchor(
    caName: String!, 
    pubKey: PublicKey!, 
    nameConstraints: ByteArray!)
```

Creates an instance of`TrustAnchor`where the most-trusted CA is specified as a distinguished name and public key. Name constraints are an optional parameter, and are intended to be used as additional constraints when validating an X.509 certification path.

The name constraints are specified as a byte array. This byte array contains the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in RFC 5280 and X.509. The ASN.1 notation for this structure is supplied in the documentation for[TrustAnchor(X509Certificate trustedCert, byte[] nameConstraints)](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(java.security.cert.X509Certificate,%20kotlin.ByteArray)).

Note that the name constraints byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the X.500 distinguished name of the most-trusted CA in [RFC 2253](http://www.ietf.org/rfc/rfc2253.txt)`String`format |
| `pubKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!:the public key of the most-trusted CA |
| `nameConstraints` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the ASN.1 DER encoding of a NameConstraints extension to be used for checking name constraints. Only the value of the extension is included, not the OID or criticality flag. Specify`null`to omit the parameter. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified`caName`parameter is empty`(caName.length() == 0)`or incorrectly formatted or the name constraints cannot be decoded |
| `java.lang.NullPointerException` | if the specified`caName`or`pubKey`parameter is`null` |

### TrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrustAnchor(
    trustedCert: X509Certificate!, 
    nameConstraints: ByteArray!)
```

Creates an instance of`TrustAnchor`with the specified`X509Certificate`and optional name constraints, which are intended to be used as additional constraints when validating an X.509 certification path.

The name constraints are specified as a byte array. This byte array should contain the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in [RFC 5280](http://tools.ietf.org/html/rfc5280) and X.509. The ASN.1 definition of this structure appears below. 

```kotlin
<code>NameConstraints ::= SEQUENCE {
        permittedSubtrees       [0]     GeneralSubtrees OPTIONAL,
        excludedSubtrees        [1]     GeneralSubtrees OPTIONAL }
 
   GeneralSubtrees ::= SEQUENCE SIZE (1..MAX) OF GeneralSubtree
 
   GeneralSubtree ::= SEQUENCE {
        base                    GeneralName,
        minimum         [0]     BaseDistance DEFAULT 0,
        maximum         [1]     BaseDistance OPTIONAL }
 
   BaseDistance ::= INTEGER (0..MAX)
 
   GeneralName ::= CHOICE {
        otherName                       [0]     OtherName,
        rfc822Name                      [1]     IA5String,
        dNSName                         [2]     IA5String,
        x400Address                     [3]     ORAddress,
        directoryName                   [4]     Name,
        ediPartyName                    [5]     EDIPartyName,
        uniformResourceIdentifier       [6]     IA5String,
        iPAddress                       [7]     OCTET STRING,
        registeredID                    [8]     OBJECT IDENTIFIER}
  </code>
```

Note that the name constraints byte array supplied is cloned to protect against subsequent modifications.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trustedCert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)!:a trusted`X509Certificate` |
| `nameConstraints` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the ASN.1 DER encoding of a NameConstraints extension to be used for checking name constraints. Only the value of the extension is included, not the OID or criticality flag. Specify`null`to omit the parameter. |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if the name constraints cannot be decoded |
| `java.lang.NullPointerException` | if the specified`X509Certificate`is`null` |

### TrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TrustAnchor(
    caPrincipal: X500Principal!, 
    pubKey: PublicKey!, 
    nameConstraints: ByteArray!)
```

Creates an instance of`TrustAnchor`where the most-trusted CA is specified as an X500Principal and public key. Name constraints are an optional parameter, and are intended to be used as additional constraints when validating an X.509 certification path.

The name constraints are specified as a byte array. This byte array contains the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in RFC 5280 and X.509. The ASN.1 notation for this structure is supplied in the documentation for[TrustAnchor(X509Certificate trustedCert, byte[] nameConstraints)](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(java.security.cert.X509Certificate,%20kotlin.ByteArray)).

Note that the name constraints byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caPrincipal` | [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!:the name of the most-trusted CA as X500Principal |
| `pubKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!:the public key of the most-trusted CA |
| `nameConstraints` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the ASN.1 DER encoding of a NameConstraints extension to be used for checking name constraints. Only the value of the extension is included, not the OID or criticality flag. Specify`null`to omit the parameter. |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified`caPrincipal`or`pubKey`parameter is`null` |

## Public methods

### getCA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCA(): X500Principal!
```

Returns the name of the most-trusted CA as an X500Principal.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | the X.500 distinguished name of the most-trusted CA, or`null`if the trust anchor was not specified as a trusted public key and name or X500Principal pair |

### getCAName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCAName(): String!
```

Returns the name of the most-trusted CA in RFC 2253`String`format.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the X.500 distinguished name of the most-trusted CA, or`null`if the trust anchor was not specified as a trusted public key and name or X500Principal pair |

### getCAPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCAPublicKey(): PublicKey!
```

Returns the public key of the most-trusted CA.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)! | the public key of the most-trusted CA, or`null`if the trust anchor was not specified as a trusted public key and name or X500Principal pair |

### getNameConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNameConstraints(): ByteArray!
```

Returns the name constraints parameter. The specified name constraints are associated with this trust anchor and are intended to be used as additional constraints when validating an X.509 certification path.

The name constraints are returned as a byte array. This byte array contains the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in RFC 5280 and X.509. The ASN.1 notation for this structure is supplied in the documentation for[TrustAnchor(X509Certificate trustedCert, byte[] nameConstraints)](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor#TrustAnchor(java.security.cert.X509Certificate,%20kotlin.ByteArray)).

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | a byte array containing the ASN.1 DER encoding of a NameConstraints extension used for checking name constraints, or`null`if not set. |

### getTrustedCert

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrustedCert(): X509Certificate!
```

Returns the most-trusted CA certificate.

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)! | a trusted`X509Certificate`or`null`if the trust anchor was not specified as a trusted certificate |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a formatted string describing the`TrustAnchor`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the`TrustAnchor` |
