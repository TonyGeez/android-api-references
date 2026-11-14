Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509CRL

```
abstract class X509CRL : CRL, X509Extension
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.cert.CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL) ||
| | ↳ | [java.security.cert.X509CRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#) |

Abstract class for an X.509 Certificate Revocation List (CRL). A CRL is a time-stamped list identifying revoked certificates. It is signed by a Certificate Authority (CA) and made freely available in a public repository.

Each revoked certificate is identified in a CRL by its certificate serial number. When a certificate-using system uses a certificate (e.g., for verifying a remote user's digital signature), that system not only checks the certificate signature and validity but also acquires a suitably- recent CRL and checks that the certificate serial number is not on that CRL. The meaning of "suitably-recent" may vary with local policy, but it usually means the most recently-issued CRL. A CA issues a new CRL on a regular periodic basis (e.g., hourly, daily, or weekly). Entries are added to CRLs as revocations occur, and an entry may be removed when the certificate expiration date is reached.

The X.509 v2 CRL format is described below in ASN.1:

```kotlin
CertificateList  ::=  SEQUENCE  {
      tbsCertList          TBSCertList,
      signatureAlgorithm   AlgorithmIdentifier,
      signature            BIT STRING  }
  
```

More information can be found in [RFC 3280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://www.ietf.org/rfc/rfc3280.txt).

The ASN.1 definition of `tbsCertList` is:

```kotlin
TBSCertList  ::=  SEQUENCE  {
      version                 Version OPTIONAL,
                              -- if present, must be v2
      signature               AlgorithmIdentifier,
      issuer                  Name,
      thisUpdate              ChoiceOfTime,
      nextUpdate              ChoiceOfTime OPTIONAL,
      revokedCertificates     SEQUENCE OF SEQUENCE  {
          userCertificate         CertificateSerialNumber,
          revocationDate          ChoiceOfTime,
          crlEntryExtensions      Extensions OPTIONAL
                                  -- if present, must be v2
          }  OPTIONAL,
      crlExtensions           [0]  EXPLICIT Extensions OPTIONAL
                                   -- if present, must be v2
      }
  
```

CRLs are instantiated using a certificate factory. The following is an example of how to instantiate an X.509 CRL:

```kotlin
<code>try (InputStream inStream = new FileInputStream("fileName-of-crl")) {
      CertificateFactory cf = CertificateFactory.getInstance("X.509");
      X509CRL crl = (X509CRL)cf.generateCRL(inStream);
  }
  </code>
```

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#X509CRL()()` Constructor for X. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares this CRL for equality with the given object. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getEncoded()()` Returns the ASN. |
| abstract [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getIssuerDN()()` **Denigrated** , replaced by [getIssuerX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getIssuerX500Principal()). |
| open [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getIssuerX500Principal()()` Returns the issuer (issuer distinguished name) value from the CRL as an `X500Principal`. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getNextUpdate()()` Gets the `nextUpdate` date from the CRL. |
| abstract [X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getRevokedCertificate(java.math.BigInteger)(serialNumber: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!)` Gets the CRL entry, if any, with the given certificate serialNumber. |
| open [X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getRevokedCertificate(java.security.cert.X509Certificate)(certificate: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!)` Get the CRL entry, if any, for the given certificate. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getRevokedCertificates()()` Gets all the entries from this CRL. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgName()()` Gets the signature algorithm name for the CRL signature algorithm. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgOID()()` Gets the signature algorithm OID string from the CRL. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgParams()()` Gets the DER-encoded signature algorithm parameters from this CRL's signature algorithm. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSignature()()` Gets the `signature` value (the raw signature bits) from the CRL. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getTBSCertList()()` Gets the DER-encoded CRL information, the `tbsCertList` from this CRL. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getThisUpdate()()` Gets the `thisUpdate` date from the CRL. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getVersion()()` Gets the `version` (version number) value from the CRL. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#hashCode()()` Returns a hashcode value for this CRL from its encoded form. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#verify(java.security.PublicKey)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!)` Verifies that this CRL was signed using the private key that corresponds to the given public key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#verify(java.security.PublicKey,%20kotlin.String)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!, sigProvider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Verifies that this CRL was signed using the private key that corresponds to the given public key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#verify(java.security.PublicKey,%20java.security.Provider)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!, sigProvider: https://developer.android.com/reference/kotlin/java/security/Provider.html#!)` Verifies that this CRL was signed using the private key that corresponds to the given public key. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getCriticalExtensionOIDs()()`

Gets a Set of the OID strings for the extension(s) marked CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of critical extensions from an X509Certificate and print the OIDs:

```kotlin
<code>X509Certificate cert = null;
  try (InputStream inStrm = new FileInputStream("DER-encoded-Cert")) {
      CertificateFactory cf = CertificateFactory.getInstance("X.509");
      cert = (X509Certificate)cf.generateCertificate(inStrm);
  }
 
  Set&lt;String&gt; critSet = cert.getCriticalExtensionOIDs();
  if (critSet != null &amp;&amp; !critSet.isEmpty()) {
      System.out.println("Set of critical extensions:");
      for (String oid : critSet) {
          System.out.println(oid);
      }
  }
  </code>
```

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getExtensionValue(kotlin.String)(oid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Gets the DER-encoded OCTET string for the extension value (*extnValue* ) identified by the passed-in `oid` String. The `oid` string is represented by a set of nonnegative whole numbers separated by periods.

For example: 
OID *(Object Identifier)* Extension Name 2.5.29.14 SubjectKeyIdentifier 2.5.29.15 KeyUsage 2.5.29.16 PrivateKeyUsage 2.5.29.17 SubjectAlternativeName 2.5.29.18 IssuerAlternativeName 2.5.29.19 BasicConstraints 2.5.29.30 NameConstraints 2.5.29.33 PolicyMappings 2.5.29.35 AuthorityKeyIdentifier 2.5.29.36 PolicyConstraints

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getNonCriticalExtensionOIDs()()`

Gets a Set of the OID strings for the extension(s) marked NON-CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of non-critical extensions from an X509CRL revoked certificate entry and print the OIDs:

```kotlin
<code>CertificateFactory cf = null;
  X509CRL crl = null;
  try (InputStream inStrm = new FileInputStream("DER-encoded-CRL")) {
      cf = CertificateFactory.getInstance("X.509");
      crl = (X509CRL)cf.generateCRL(inStrm);
  }
 
  byte[] certData = &lt;DER-encoded certificate data&gt;
  ByteArrayInputStream bais = new ByteArrayInputStream(certData);
  X509Certificate cert = (X509Certificate)cf.generateCertificate(bais);
  X509CRLEntry badCert =
               crl.getRevokedCertificate(cert.getSerialNumber());
 
  if (badCert != null) {
      Set&lt;String&gt; nonCritSet = badCert.getNonCriticalExtensionOIDs();
      if (nonCritSet != null)
          for (String oid : nonCritSet) {
              System.out.println(oid);
          }
  }
  </code>
```

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#hasUnsupportedCriticalExtension()()`

Check if there is a critical extension that is not supported.

<br />

From class `https://developer.android.com/reference/kotlin/java/security/cert/CRL` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/java/security/cert/CRL#getType()()`

Returns the type of this CRL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/java/security/cert/CRL#isRevoked(java.security.cert.Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!)`

Checks whether the given certificate is on this CRL.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` `https://developer.android.com/reference/kotlin/java/security/cert/CRL#toString()()`

Returns a string representation of this CRL.

<br />

## Protected constructors

### X509CRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected X509CRL()
```

Constructor for X.509 CRLs.

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares this CRL for equality with the given object. If the `other` object is an `instanceof` `X509CRL`, then its encoded form is retrieved and compared with the encoded form of this CRL.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the object to test for equality with this CRL. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true iff the encoded forms of the two CRLs match, false otherwise. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getEncoded(): ByteArray!
```

Returns the ASN.1 DER-encoded form of this CRL.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the encoded form of this certificate |

| Exceptions ||
|---|---|
| `java.security.cert.CRLException` | if an encoding error occurs. |

### getIssuerDN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getIssuerDN(): Principal!
```

**Denigrated** , replaced by [getIssuerX500Principal()](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getIssuerX500Principal()). This method returns the `issuer` as an implementation specific Principal object, which should not be relied upon by portable code.

Gets the `issuer` (issuer distinguished name) value from the CRL. The issuer name identifies the entity that signed (and issued) the CRL.

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

### getIssuerX500Principal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerX500Principal(): X500Principal!
```

Returns the issuer (issuer distinguished name) value from the CRL as an `X500Principal`.

It is recommended that subclasses override this method.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!` | an `X500Principal` representing the issuer distinguished name |

### getNextUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getNextUpdate(): Date!
```

Gets the `nextUpdate` date from the CRL.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the `nextUpdate` date from the CRL, or null if not present. |

### getRevokedCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRevokedCertificate(serialNumber: BigInteger!): X509CRLEntry!
```

Gets the CRL entry, if any, with the given certificate serialNumber.

| Parameters ||
|---|---|
| `serialNumber` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!: the serial number of the certificate for which a CRL entry is to be looked up |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry!` | the entry with the given serial number, or null if no such entry exists in this CRL. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry`

### getRevokedCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRevokedCertificate(certificate: X509Certificate!): X509CRLEntry!
```

Get the CRL entry, if any, for the given certificate.

This method can be used to lookup CRL entries in indirect CRLs, that means CRLs that contain entries from issuers other than the CRL issuer. The default implementation will only return entries for certificates issued by the CRL issuer. Subclasses that wish to support indirect CRLs should override this method.

| Parameters ||
|---|---|
| `certificate` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)!: the certificate for which a CRL entry is to be looked up |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry!` | the entry for the given certificate, or null if no such entry exists in this CRL. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if certificate is null |

### getRevokedCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRevokedCertificates(): MutableSet<out X509CRLEntry!>!
```

Gets all the entries from this CRL. This returns a Set of X509CRLEntry objects.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<out https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry!>!` | all the entries or null if there are none present. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry`

### getSigAlgName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSigAlgName(): String!
```

Gets the signature algorithm name for the CRL signature algorithm. An example is the string "SHA256withRSA". The ASN.1 definition for this is:

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

Gets the signature algorithm OID string from the CRL. An OID is represented by a set of nonnegative whole numbers separated by periods. For example, the string "1.2.840.10040.4.3" identifies the SHA-1 with DSA signature algorithm defined in [RFC 3279: Algorithms and Identifiers for the Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://www.ietf.org/rfc/rfc3279.txt).

See `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgName()` for relevant ASN.1 definitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the signature algorithm OID string. |

### getSigAlgParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSigAlgParams(): ByteArray!
```

Gets the DER-encoded signature algorithm parameters from this CRL's signature algorithm. In most cases, the signature algorithm parameters are null; the parameters are usually supplied with the public key. If access to individual parameter values is needed then use `https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#` and instantiate with the name returned by `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgName()`.

See `https://developer.android.com/reference/kotlin/java/security/cert/X509CRL#getSigAlgName()` for relevant ASN.1 definitions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the DER-encoded signature algorithm parameters, or null if no parameters are present. |

### getSignature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSignature(): ByteArray!
```

Gets the `signature` value (the raw signature bits) from the CRL. The ASN.1 definition for this is:

```kotlin
signature     BIT STRING
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the signature. |

### getTBSCertList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTBSCertList(): ByteArray!
```

Gets the DER-encoded CRL information, the `tbsCertList` from this CRL. This can be used to verify the signature independently.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the DER-encoded CRL information. |

| Exceptions ||
|---|---|
| `java.security.cert.CRLException` | if an encoding error occurs. |

### getThisUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getThisUpdate(): Date!
```

Gets the `thisUpdate` date from the CRL. The ASN.1 definition for this is:

```kotlin
thisUpdate   ChoiceOfTime
  ChoiceOfTime ::= CHOICE {
      utcTime        UTCTime,
      generalTime    GeneralizedTime }
  
```

<br />

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the `thisUpdate` date from the CRL. |

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getVersion(): Int
```

Gets the `version` (version number) value from the CRL. The ASN.1 definition for this is:

```kotlin
version    Version OPTIONAL,
              -- if present, must be v2
 
  Version  ::=  INTEGER  {  v1(0), v2(1), v3(2)  }
              -- v3 does not apply to CRLs but appears for consistency
              -- with definition of Version for certs
  
```

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the version number, i.e. 1 or 2. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hashcode value for this CRL from its encoded form.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hashcode value. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(key: PublicKey!): Unit
```

Verifies that this CRL was signed using the private key that corresponds to the given public key.

| Parameters ||
|---|---|
| `key` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!: the PublicKey used to carry out the verification. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.NoSuchProviderException` | if there's no default provider. |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CRLException` | on encoding errors. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun verify(
    key: PublicKey!, 
    sigProvider: String!
): Unit
```

Verifies that this CRL was signed using the private key that corresponds to the given public key. This method uses the signature verification engine supplied by the given provider.

| Parameters ||
|---|---|
| `key` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!: the PublicKey used to carry out the verification. |
| `sigProvider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the signature provider. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.NoSuchProviderException` | on incorrect provider. |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CRLException` | on encoding errors. |

### verify

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun verify(
    key: PublicKey!, 
    sigProvider: Provider!
): Unit
```

Verifies that this CRL was signed using the private key that corresponds to the given public key. This method uses the signature verification engine supplied by the given provider. Note that the specified Provider object does not have to be registered in the provider list. This method was added to version 1.8 of the Java Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method is not `abstract` and it provides a default implementation.

| Parameters ||
|---|---|
| `key` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!: the PublicKey used to carry out the verification. |
| `sigProvider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!: the signature provider. |

| Exceptions ||
|---|---|
| `java.security.InvalidKeyException` | on incorrect key. |
| `java.security.NoSuchAlgorithmException` | on unsupported signature algorithms. |
| `java.security.SignatureException` | on signature errors. |
| `java.security.cert.CRLException` | on encoding errors. |
