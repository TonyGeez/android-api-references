# X509CRLEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509CRLEntry

```
abstract class X509CRLEntry : X509Extension
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#) |

Abstract class for a revoked certificate in a CRL (Certificate Revocation List). The ASN.1 definition for*revokedCertificates*is: 

```kotlin
revokedCertificates    SEQUENCE OF SEQUENCE  {
      userCertificate    CertificateSerialNumber,
      revocationDate     ChoiceOfTime,
      crlEntryExtensions Extensions OPTIONAL
                         -- if present, must be v2
  }  OPTIONAL
 
  CertificateSerialNumber  ::=  INTEGER
 
  Extensions  ::=  SEQUENCE SIZE (1..MAX) OF Extension
 
  Extension  ::=  SEQUENCE  {
      extnId        OBJECT IDENTIFIER,
      critical      BOOLEAN DEFAULT FALSE,
      extnValue     OCTET STRING
                    -- contains a DER encoding of a value
                    -- of the type registered for use with
                    -- the extnId object identifier value
  }
  
```

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#X509CRLEntry())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this CRL entry for equality with the given object. |
| open [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | [getCertificateIssuer](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#getCertificateIssuer())`()` Get the issuer of the X509Certificate described by this entry. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#getEncoded())`()` Returns the ASN. |
| abstract [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getRevocationDate](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#getRevocationDate())`()` Gets the revocation date from this X509CRLEntry, the*revocationDate*. |
| open [CRLReason](https://developer.android.com/reference/kotlin/java/security/cert/CRLReason)! | [getRevocationReason](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#getRevocationReason())`()` Returns the reason the certificate has been revoked, as specified in the Reason Code extension of this CRL entry. |
| abstract [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getSerialNumber](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#getSerialNumber())`()` Gets the serial number from this X509CRLEntry, the*userCertificate*. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasExtensions](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#hasExtensions())`()` Returns true if this CRL entry has extensions. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#hashCode())`()` Returns a hashcode value for this CRL entry from its encoded form. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry#toString())`()` Returns a string representation of this CRL entry. |

| Inherited functions ||
|---|---|
| From class [X509Extension](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getCriticalExtensionOIDs](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getCriticalExtensionOIDs())`()` <br /> Gets a Set of the OID strings for the extension(s) marked CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of critical extensions from an X509Certificate and print the OIDs: ```kotlin <code>X509Certificate cert = null; try (InputStream inStrm = new FileInputStream("DER-encoded-Cert")) { CertificateFactory cf = CertificateFactory.getInstance("X.509"); cert = (X509Certificate)cf.generateCertificate(inStrm); } Set&lt;String&gt; critSet = cert.getCriticalExtensionOIDs(); if (critSet != null &amp;&amp; !critSet.isEmpty()) { System.out.println("Set of critical extensions:"); for (String oid : critSet) { System.out.println(oid); } } </code> ``` <br /> <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getExtensionValue](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getExtensionValue(kotlin.String))`(`oid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the DER-encoded OCTET string for the extension value (*extnValue* ) identified by the passed-in`oid`String. The`oid`string is represented by a set of nonnegative whole numbers separated by periods. For example: | OID*(Object Identifier)* | Extension Name | | 2.5.29.14 | SubjectKeyIdentifier | | 2.5.29.15 | KeyUsage | | 2.5.29.16 | PrivateKeyUsage | | 2.5.29.17 | SubjectAlternativeName | | 2.5.29.18 | IssuerAlternativeName | | 2.5.29.19 | BasicConstraints | | 2.5.29.30 | NameConstraints | | 2.5.29.33 | PolicyMappings | | 2.5.29.35 | AuthorityKeyIdentifier | | 2.5.29.36 | PolicyConstraints | |--------------------------|------------------------| <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getNonCriticalExtensionOIDs](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#getNonCriticalExtensionOIDs())`()` <br /> Gets a Set of the OID strings for the extension(s) marked NON-CRITICAL in the certificate/CRL managed by the object implementing this interface. Here is sample code to get a Set of non-critical extensions from an X509CRL revoked certificate entry and print the OIDs: ```kotlin <code>CertificateFactory cf = null; X509CRL crl = null; try (InputStream inStrm = new FileInputStream("DER-encoded-CRL")) { cf = CertificateFactory.getInstance("X.509"); crl = (X509CRL)cf.generateCRL(inStrm); } byte[] certData = &lt;DER-encoded certificate data&gt; ByteArrayInputStream bais = new ByteArrayInputStream(certData); X509Certificate cert = (X509Certificate)cf.generateCertificate(bais); X509CRLEntry badCert = crl.getRevokedCertificate(cert.getSerialNumber()); if (badCert != null) { Set&lt;String&gt; nonCritSet = badCert.getNonCriticalExtensionOIDs(); if (nonCritSet != null) for (String oid : nonCritSet) { System.out.println(oid); } } </code> ``` <br /> <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasUnsupportedCriticalExtension](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension#hasUnsupportedCriticalExtension())`()` <br /> Check if there is a critical extension that is not supported. <br /> | ||

## Public constructors

### X509CRLEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509CRLEntry()
```

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this CRL entry for equality with the given object. If the`other`object is an`instanceof``X509CRLEntry`, then its encoded form (the inner SEQUENCE) is retrieved and compared with the encoded form of this CRL entry.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `other` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to test for equality with this CRL entry. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the encoded forms of the two CRL entries match, false otherwise. |

### getCertificateIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertificateIssuer(): X500Principal!
```

Get the issuer of the X509Certificate described by this entry. If the certificate issuer is also the CRL issuer, this method returns null.

This method is used with indirect CRLs. The default implementation always returns null. Subclasses that wish to support indirect CRLs should override it.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)! | the issuer of the X509Certificate described by this entry or null if it is issued by the CRL issuer. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getEncoded(): ByteArray!
```

Returns the ASN.1 DER-encoded form of this CRL Entry, that is the inner SEQUENCE.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encoded form of this certificate |

| Exceptions ||
|-----------------------------------|------------------------------|
| `java.security.cert.CRLException` | if an encoding error occurs. |

### getRevocationDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRevocationDate(): Date!
```

Gets the revocation date from this X509CRLEntry, the*revocationDate*.

| Return ||
|------------------------------------------------------------------------------|----------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | the revocation date. |

### getRevocationReason

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRevocationReason(): CRLReason!
```

Returns the reason the certificate has been revoked, as specified in the Reason Code extension of this CRL entry.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [CRLReason](https://developer.android.com/reference/kotlin/java/security/cert/CRLReason)! | the reason the certificate has been revoked, or`null`if this CRL entry does not have a Reason Code extension |

### getSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSerialNumber(): BigInteger!
```

Gets the serial number from this X509CRLEntry, the*userCertificate*.

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the serial number. |

### hasExtensions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasExtensions(): Boolean
```

Returns true if this CRL entry has extensions.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this entry has extensions, false otherwise. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hashcode value for this CRL entry from its encoded form.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hashcode value. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toString(): String
```

Returns a string representation of this CRL entry.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this CRL entry. |
