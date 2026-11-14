Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509Certificate

```
abstract class X509Certificate : Certificate, X509Extension
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.cert.Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate) ||
| | ↳ | [java.security.cert.X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#) |

Abstract class for X.509 certificates. This provides a standard way to access all the attributes of an X.509 certificate.

In June of 1996, the basic X.509 v3 format was completed by ISO/IEC and ANSI X9, which is described below in ASN.1:

```kotlin
Certificate  ::=  SEQUENCE  {
      tbsCertificate       TBSCertificate,
      signatureAlgorithm   AlgorithmIdentifier,
      signature            BIT STRING  }
  
```

These certificates are widely used to support authentication and other functionality in Internet security systems. Common applications include Privacy Enhanced Mail (PEM), Transport Layer Security (SSL), code signing for trusted software distribution, and Secure Electronic Transactions (SET).

These certificates are managed and vouched for by *Certificate Authorities* (CAs). CAs are services which create certificates by placing data in the X.509 standard format and then digitally signing that data. CAs act as trusted third parties, making introductions between principals who have no direct knowledge of each other. CA certificates are either signed by themselves, or by some other CA such as a "root" CA.

More information can be found in [RFC 3280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://www.ietf.org/rfc/rfc3280.txt).

The ASN.1 definition of `tbsCertificate` is:

```kotlin
TBSCertificate  ::=  SEQUENCE  {
      version         [0]  EXPLICIT Version DEFAULT v1,
      serialNumber         CertificateSerialNumber,
      signature            AlgorithmIdentifier,
      issuer               Name,
      validity             Validity,
      subject              Name,
      subjectPublicKeyInfo SubjectPublicKeyInfo,
      issuerUniqueID  [1]  IMPLICIT UniqueIdentifier OPTIONAL,
                           -- If present, version must be v2 or v3
      subjectUniqueID [2]  IMPLICIT UniqueIdentifier OPTIONAL,
                           -- If present, version must be v2 or v3
      extensions      [3]  EXPLICIT Extensions OPTIONAL
                           -- If present, version must be v3
      }
  
```

Certificates are instantiated using a certificate factory. The following is an example of how to instantiate an X.509 certificate:

```kotlin
try (InputStream inStream = new FileInputStream("fileName-of-cert")) {
      CertificateFactory cf = CertificateFactory.getInstance("X.509");
      X509Certificate cert = (X509Certificate)cf.generateCertificate(inStream);
  }
  
```

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#X509Certificate()()` Constructor for X. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#checkValidity()()` Checks that the certificate is currently valid. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#checkValidity(java.util.Date)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Checks that the given date is within the certificate's validity period. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getBasicConstraints()()` Gets the certificate constraints path length from the critical `BasicConstraints` extension, (OID = 2.5.29.19). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getExtendedKeyUsage()()` Gets an unmodifiable list of Strings representing the OBJECT IDENTIFIERs of the `ExtKeyUsageSyntax` field of the extended key usage extension, (OID = 2.5.29.37). |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerAlternativeNames()()` Gets an immutable collection of issuer alternative names from the `IssuerAltName` extension, (OID = 2.5.29.18). |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerDN()()` **Denigrated** , replaced by [getIssuerX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerX500Principal()). |
| abstract [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerUniqueID()()` Gets the `issuerUniqueID` value from the certificate. |
| open [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerX500Principal()()` Returns the issuer (issuer distinguished name) value from the certificate as an `X500Principal`. |
| abstract [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getKeyUsage()()` Gets a boolean array representing bits of the `KeyUsage` extension, (OID = 2.5.29.15). |
| abstract [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getNotAfter()()` Gets the `notAfter` date from the validity period of the certificate. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getNotBefore()()` Gets the `notBefore` date from the validity period of the certificate. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSerialNumber()()` Gets the `serialNumber` value from the certificate. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgName()()` Gets the signature algorithm name for the certificate signature algorithm. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgOID()()` Gets the signature algorithm OID string from the certificate. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgParams()()` Gets the DER-encoded signature algorithm parameters from this certificate's signature algorithm. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSignature()()` Gets the `signature` value (the raw signature bits) from the certificate. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectAlternativeNames()()` Gets an immutable collection of subject alternative names from the `SubjectAltName` extension, (OID = 2.5.29.17). |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectDN()()` **Denigrated** , replaced by [getSubjectX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectX500Principal()). |
| abstract [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectUniqueID()()` Gets the `subjectUniqueID` value from the certificate. |
| open [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectX500Principal()()` Returns the subject (subject distinguished name) value from the certificate as an `X500Principal`. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getTBSCertificate()()` Gets the DER-encoded certificate information, the `tbsCertificate` from this certificate. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getVersion()()` Gets the `version` (version number) value from the certificate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#verify(java.security.PublicKey,%20java.security.Provider)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!, sigProvider: https://developer.android.com/reference/kotlin/java/security/Provider.html#!)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/cert/Certificate` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this certificate for equality with the specified object. If the `other` object is an `instanceof` `Certificate`, then its encoded form is retrieved and compared with the encoded form of this certificate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#getEncoded()()` Returns the encoded form of this certificate. It is assumed that each certificate type would have only a single form of encoding; for example, X.509 certificates would be encoded as ASN.1 DER. <br /> | | `https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#getPublicKey()()` Gets the public key from this certificate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#getType()()` Returns the type of this certificate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#hashCode()()` Returns a hashcode value for this certificate from its encoded form. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#toString()()` Returns a string representation of this certificate. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#verify(java.security.PublicKey)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#verify(java.security.PublicKey,%20kotlin.String)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!, sigProvider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Verifies that this certificate was signed using the private key that corresponds to the specified public key. This method uses the signature verification engine supplied by the specified provider. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/security/cert/Certificate#writeReplace()()` Replace the Certificate to be serialized. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getCriticalExtensionOIDs()()` Gets a Set of the OID strings for the extension(s) marked CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of critical extensions from an X509Certificate and print the OIDs: ```kotlin <code>X509Certificate cert = null; try (InputStream inStrm = new FileInputStream("DER-encoded-Cert")) { CertificateFactory cf = CertificateFactory.getInstance("X.509"); cert = (X509Certificate)cf.generateCertificate(inStrm); } Set&lt;String&gt; critSet = cert.getCriticalExtensionOIDs(); if (critSet != null &amp;&amp; !critSet.isEmpty()) { System.out.println("Set of critical extensions:"); for (String oid : critSet) { System.out.println(oid); } } </code> ``` <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getExtensionValue(kotlin.String)(oid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Gets the DER-encoded OCTET string for the extension value (*extnValue* ) identified by the passed-in `oid` String. The `oid` string is represented by a set of nonnegative whole numbers separated by periods. For example: | OID *(Object Identifier)* | Extension Name | | 2.5.29.14 | SubjectKeyIdentifier | | 2.5.29.15 | KeyUsage | | 2.5.29.16 | PrivateKeyUsage | | 2.5.29.17 | SubjectAlternativeName | | 2.5.29.18 | IssuerAlternativeName | | 2.5.29.19 | BasicConstraints | | 2.5.29.30 | NameConstraints | | 2.5.29.33 | PolicyMappings | | 2.5.29.35 | AuthorityKeyIdentifier | | 2.5.29.36 | PolicyConstraints | |---|---| <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getNonCriticalExtensionOIDs()()` Gets a Set of the OID strings for the extension(s) marked NON-CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of non-critical extensions from an X509CRL revoked certificate entry and print the OIDs: ```kotlin <code>CertificateFactory cf = null; X509CRL crl = null; try (InputStream inStrm = new FileInputStream("DER-encoded-CRL")) { cf = CertificateFactory.getInstance("X.509"); crl = (X509CRL)cf.generateCRL(inStrm); } byte[] certData = &lt;DER-encoded certificate data&gt; ByteArrayInputStream bais = new ByteArrayInputStream(certData); X509Certificate cert = (X509Certificate)cf.generateCertificate(bais); X509CRLEntry badCert = crl.getRevokedCertificate(cert.getSerialNumber()); if (badCert != null) { Set&lt;String&gt; nonCritSet = badCert.getNonCriticalExtensionOIDs(); if (nonCritSet != null) for (String oid : nonCritSet) { System.out.println(oid); } } </code> ``` <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#hasUnsupportedCriticalExtension()()` Check if there is a critical extension that is not supported. <br /> | ||

## Protected constructors

### X509Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected X509Certificate()
```

Constructor for X.509 certificates.

## Public methods

### checkValidity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun checkValidity(): Unit
```

Checks that the certificate is currently valid. It is if the current date and time are within the validity period given in the certificate.

The validity period consists of two date/time values: the first and last dates (and times) on which the certificate is valid. It is defined in ASN.1 as:

```kotlin
validity             Validity
 
  Validity ::= SEQUENCE {
      notBefore      CertificateValidityDate,
      notAfter       CertificateValidityDate }
 
  CertificateValidityDate ::= CHOICE {
      utcTime        UTCTime,
      generalTime    GeneralizedTime }
  
```

| Exceptions ||
|---|---|
| `java.security.cert.CertificateExpiredException` | if the certificate has expired. |
| `java.security.cert.CertificateNotYetValidException` | if the certificate is not yet valid. |

### checkValidity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun checkValidity(date: Date!): Unit
```

Checks that the given date is within the certificate's validity period. In other words, this determines whether the certificate would be valid at the given date/time.

| Parameters ||
|---|---|
| `date` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!: the Date to check against to see if this certificate is valid at that date/time. |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateExpiredException` | if the certificate has expired with respect to the `date` supplied. |
| `java.security.cert.CertificateNotYetValidException` | if the certificate is not yet valid with respect to the `date` supplied. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#checkValidity()`

### getBasicConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getBasicConstraints(): Int
```

Gets the certificate constraints path length from the critical `BasicConstraints` extension, (OID = 2.5.29.19).

The basic constraints extension identifies whether the subject of the certificate is a Certificate Authority (CA) and how deep a certification path may exist through that CA. The `pathLenConstraint` field (see below) is meaningful only if `cA` is set to TRUE. In this case, it gives the maximum number of CA certificates that may follow this certificate in a certification path. A value of zero indicates that only an end-entity certificate may follow in the path.

The ASN.1 definition for this is:

```kotlin
BasicConstraints ::= SEQUENCE {
      cA                  BOOLEAN DEFAULT FALSE,
      pathLenConstraint   INTEGER (0..MAX) OPTIONAL }
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value of `pathLenConstraint` if the BasicConstraints extension is present in the certificate and the subject of the certificate is a CA, otherwise -1. If the subject of the certificate is a CA and `pathLenConstraint` does not appear, `Integer.MAX_VALUE` is returned to indicate that there is no limit to the allowed length of the certification path. |

### getExtendedKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtendedKeyUsage(): MutableList<String!>!
```

Gets an unmodifiable list of Strings representing the OBJECT IDENTIFIERs of the `ExtKeyUsageSyntax` field of the extended key usage extension, (OID = 2.5.29.37). It indicates one or more purposes for which the certified public key may be used, in addition to or in place of the basic purposes indicated in the key usage extension field. The ASN.1 definition for this is:

```kotlin
ExtKeyUsageSyntax ::= SEQUENCE SIZE (1..MAX) OF KeyPurposeId
 
  KeyPurposeId ::= OBJECT IDENTIFIER
  
```
Key purposes may be defined by any organization with a need. Object identifiers used to identify key purposes shall be assigned in accordance with IANA or ITU-T Rec. X.660 | ISO/IEC/ITU 9834-1.

<br />

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method is not `abstract` and it provides a default implementation. Subclasses should override this method with a correct implementation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | the ExtendedKeyUsage extension of this certificate, as an unmodifiable list of object identifiers represented as Strings. Returns null if this certificate does not contain an ExtendedKeyUsage extension. |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateParsingException` | if the extension cannot be decoded |

### getIssuerAlternativeNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerAlternativeNames(): MutableCollection<MutableList<*>!>!
```

Gets an immutable collection of issuer alternative names from the `IssuerAltName` extension, (OID = 2.5.29.18).

The ASN.1 definition of the `IssuerAltName` extension is:

```kotlin
IssuerAltName ::= GeneralNames
  
```
The ASN.1 definition of `GeneralNames` is defined in `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectAlternativeNames()`.

If this certificate does not contain an `IssuerAltName` extension, `null` is returned. Otherwise, a `Collection` is returned with an entry representing each `GeneralName` included in the extension. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively). For more details about the formats used for each name type, see the `getSubjectAlternativeNames` method.

Note that the `Collection` returned may contain more than one name of the same type. Also, note that the returned `Collection` is immutable and any entries containing byte arrays are cloned to protect against subsequent modifications.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method is not `abstract` and it provides a default implementation. Subclasses should override this method with a correct implementation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!` | an immutable `Collection` of issuer alternative names (or `null`) |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateParsingException` | if the extension cannot be decoded |

### getIssuerDN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIssuerDN(): Principal!
```

**Denigrated** , replaced by [getIssuerX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerX500Principal()). This method returns the `issuer` as an implementation specific Principal object, which should not be relied upon by portable code.

Gets the `issuer` (issuer distinguished name) value from the certificate. The issuer name identifies the entity that signed (and issued) the certificate.

The issuer name field contains an X.500 distinguished name (DN). The ASN.1 definition for this is:

```kotlin
issuer    Name
 
  Name ::= CHOICE { RDNSequence }
  RDNSequence ::= SEQUENCE OF RelativeDistinguishedName
  RelativeDistinguishedName ::=
      SET OF AttributeValueAssertion
 
  AttributeValueAssertion ::= SEQUENCE {
                                AttributeType,
                                AttributeValue }
  AttributeType ::= OBJECT IDENTIFIER
  AttributeValue ::= ANY
  
```
The `Name` describes a hierarchical name composed of attributes, such as country name, and corresponding values, such as US. The type of the `AttributeValue` component is determined by the `AttributeType`; in general it will be a `directoryString`. A `directoryString` is usually one of `PrintableString`, `TeletexString` or `UniversalString`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal.html#!` | a Principal whose name is the issuer distinguished name. |

### getIssuerUniqueID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIssuerUniqueID(): BooleanArray!
```

Gets the `issuerUniqueID` value from the certificate. The issuer unique identifier is present in the certificate to handle the possibility of reuse of issuer names over time. RFC 3280 recommends that names not be reused and that conforming certificates not make use of unique identifiers. Applications conforming to that profile should be capable of parsing unique identifiers and making comparisons.

The ASN.1 definition for this is:

```kotlin
issuerUniqueID  [1]  IMPLICIT UniqueIdentifier OPTIONAL
 
  UniqueIdentifier  ::=  BIT STRING
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!` | the issuer unique identifier or null if it is not present in the certificate. |

### getIssuerX500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerX500Principal(): X500Principal!
```

Returns the issuer (issuer distinguished name) value from the certificate as an `X500Principal`.

It is recommended that subclasses override this method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!` | an `X500Principal` representing the issuer distinguished name |

### getKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getKeyUsage(): BooleanArray!
```

Gets a boolean array representing bits of the `KeyUsage` extension, (OID = 2.5.29.15). The key usage extension defines the purpose (e.g., encipherment, signature, certificate signing) of the key contained in the certificate. The ASN.1 definition for this is:

```kotlin
KeyUsage ::= BIT STRING {
      digitalSignature        (0),
      nonRepudiation          (1),
      keyEncipherment         (2),
      dataEncipherment        (3),
      keyAgreement            (4),
      keyCertSign             (5),
      cRLSign                 (6),
      encipherOnly            (7),
      decipherOnly            (8) }
  
```
RFC 3280 recommends that when used, this be marked as a critical extension.

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!` | the KeyUsage extension of this certificate, represented as an array of booleans. The order of KeyUsage values in the array is the same as in the above ASN.1 definition. The array will contain a value for each KeyUsage defined above. If the KeyUsage list encoded in the certificate is longer than the above list, it will not be truncated. Returns null if this certificate does not contain a KeyUsage extension. |

### getNotAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNotAfter(): Date!
```

Gets the `notAfter` date from the validity period of the certificate. See `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getNotBefore()` for relevant ASN.1 definitions.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the end date of the validity period. |

**See Also**

### getNotBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNotBefore(): Date!
```

Gets the `notBefore` date from the validity period of the certificate. The relevant ASN.1 definitions are:

```kotlin
validity             Validity
 
  Validity ::= SEQUENCE {
      notBefore      CertificateValidityDate,
      notAfter       CertificateValidityDate }
 
  CertificateValidityDate ::= CHOICE {
      utcTime        UTCTime,
      generalTime    GeneralizedTime }
  
```

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the start date of the validity period. |

**See Also**

### getSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSerialNumber(): BigInteger!
```

Gets the `serialNumber` value from the certificate. The serial number is an integer assigned by the certification authority to each certificate. It must be unique for each certificate issued by a given CA (i.e., the issuer name and serial number identify a unique certificate). The ASN.1 definition for this is:

```kotlin
serialNumber     CertificateSerialNumber
 
  CertificateSerialNumber  ::=  INTEGER
  
```

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | the serial number. |

### getSigAlgName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSigAlgName(): String!
```

Gets the signature algorithm name for the certificate signature algorithm. An example is the string "SHA256withRSA". The ASN.1 definition for this is:

```kotlin
signatureAlgorithm   AlgorithmIdentifier
 
  AlgorithmIdentifier  ::=  SEQUENCE  {
      algorithm               OBJECT IDENTIFIER,
      parameters              ANY DEFINED BY algorithm OPTIONAL  }
                              -- contains a value of the type
                              -- registered for use with the
                              -- algorithm object identifier value
  
```

<br />

The algorithm name is determined from the `algorithm` OID string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the signature algorithm name. |

### getSigAlgOID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSigAlgOID(): String!
```

Gets the signature algorithm OID string from the certificate. An OID is represented by a set of nonnegative whole numbers separated by periods. For example, the string "1.2.840.10040.4.3" identifies the SHA-1 with DSA signature algorithm defined in [RFC 3279: Algorithms and Identifiers for the Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://www.ietf.org/rfc/rfc3279.txt).

See `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgName()` for relevant ASN.1 definitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the signature algorithm OID string. |

### getSigAlgParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSigAlgParams(): ByteArray!
```

Gets the DER-encoded signature algorithm parameters from this certificate's signature algorithm. In most cases, the signature algorithm parameters are null; the parameters are usually supplied with the certificate's public key. If access to individual parameter values is needed then use `https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#` and instantiate with the name returned by `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgName()`.

See `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSigAlgName()` for relevant ASN.1 definitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the DER-encoded signature algorithm parameters, or null if no parameters are present. |

### getSignature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSignature(): ByteArray!
```

Gets the `signature` value (the raw signature bits) from the certificate. The ASN.1 definition for this is:

```kotlin
signature     BIT STRING
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the signature. |

### getSubjectAlternativeNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectAlternativeNames(): MutableCollection<MutableList<*>!>!
```

Gets an immutable collection of subject alternative names from the `SubjectAltName` extension, (OID = 2.5.29.17).

The ASN.1 definition of the `SubjectAltName` extension is:

```kotlin
SubjectAltName ::= GeneralNames
 
  GeneralNames :: = SEQUENCE SIZE (1..MAX) OF GeneralName
 
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
  
```

If this certificate does not contain a `SubjectAltName` extension, `null` is returned. Otherwise, a `Collection` is returned with an entry representing each `GeneralName` included in the extension. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively).

[RFC 822](http://www.ietf.org/rfc/rfc822.txt), DNS, and URI names are returned as `String`s, using the well-established string formats for those types (subject to the restrictions included in RFC 3280). IPv4 address names are returned using dotted quad notation. IPv6 address names are returned in the form "a1:a2:...:a8", where a1-a8 are hexadecimal values representing the eight 16-bit pieces of the address. OID names are returned as `String`s represented as a series of nonnegative integers separated by periods. And directory names (distinguished names) are returned in [RFC 2253](http://www.ietf.org/rfc/rfc2253.txt) string format. No standard string format is defined for otherNames, X.400 names, EDI party names, or any other type of names. They are returned as byte arrays containing the ASN.1 DER encoded form of the name.

Note that the `Collection` returned may contain more than one name of the same type. Also, note that the returned `Collection` is immutable and any entries containing byte arrays are cloned to protect against subsequent modifications.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method is not `abstract` and it provides a default implementation. Subclasses should override this method with a correct implementation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!` | an immutable `Collection` of subject alternative names (or `null`) |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateParsingException` | if the extension cannot be decoded |

### getSubjectDN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSubjectDN(): Principal!
```

**Denigrated** , replaced by [getSubjectX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getSubjectX500Principal()). This method returns the `subject` as an implementation specific Principal object, which should not be relied upon by portable code.

Gets the `subject` (subject distinguished name) value from the certificate. If the `subject` value is empty, then the `getName()` method of the returned `Principal` object returns an empty string ("").

The ASN.1 definition for this is:

```kotlin
subject    Name
  
```

See `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getIssuerDN()` for `Name` and other relevant definitions.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal.html#!` | a Principal whose name is the subject name. |

### getSubjectUniqueID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSubjectUniqueID(): BooleanArray!
```

Gets the `subjectUniqueID` value from the certificate.

The ASN.1 definition for this is:

```kotlin
subjectUniqueID  [2]  IMPLICIT UniqueIdentifier OPTIONAL
 
  UniqueIdentifier  ::=  BIT STRING
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!` | the subject unique identifier or null if it is not present in the certificate. |

### getSubjectX500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectX500Principal(): X500Principal!
```

Returns the subject (subject distinguished name) value from the certificate as an `X500Principal`. If the subject value is empty, then the `getName()` method of the returned `X500Principal` object returns an empty string ("").

It is recommended that subclasses override this method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!` | an `X500Principal` representing the subject distinguished name |

### getTBSCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTBSCertificate(): ByteArray!
```

Gets the DER-encoded certificate information, the `tbsCertificate` from this certificate. This can be used to verify the signature independently.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the DER-encoded certificate information. |

| Exceptions ||
|---|---|
| `java.security.cert.CertificateEncodingException` | if an encoding error occurs. |

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getVersion(): Int
```

Gets the `version` (version number) value from the certificate. The ASN.1 definition for this is:

```kotlin
version  [0] EXPLICIT Version DEFAULT v1
 
  Version ::=  INTEGER  {  v1(0), v2(1), v3(2)  }
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the version number, i.e. 1, 2 or 3. |

### verify

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun verify(
    key: PublicKey!, 
    sigProvider: Provider!
): Unit
```

Verifies that this certificate was signed using the private key that corresponds to the specified public key. This method uses the signature verification engine supplied by the specified provider. Note that the specified Provider object does not have to be registered in the provider list. This method was added to version 1.8 of the Java Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method is not `abstract` and it provides a default implementation.

| Parameters ||
|---|---|
| `key` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!: the PublicKey used to carry out the verification. |
| `sigProvider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!: the signature provider. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the method is not supported |
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CertificateException` | on encoding errors. |
