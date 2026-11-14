# X509Extension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509Extension

```
interface X509Extension
```

| [java.security.cert.X509Extension](X509Extension.md) |

| Known Direct Subclasses [X509CRL](X509CRL.md), [X509CRLEntry](X509CRLEntry.md), [X509Certificate](X509Certificate.md) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------| | [X509CRL](X509CRL.md) | Abstract class for an X. | | [X509CRLEntry](X509CRLEntry.md) | Abstract class for a revoked certificate in a CRL (Certificate Revocation List). | | [X509Certificate](X509Certificate.md) | Abstract class for X. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for an X.509 extension.

The extensions defined for X.509 v3 [Certificates](X509Certificate.md) and v2 [CRLs](X509CRL.md)(Certificate Revocation Lists) provide methods for associating additional attributes with users or public keys, for managing the certification hierarchy, and for managing CRL distribution. The X.509 extensions format also allows communities to define private extensions to carry information unique to those communities.

Each extension in a certificate/CRL may be designated as critical or non-critical. A certificate/CRL-using system (an application validating a certificate/CRL) must reject the certificate/CRL if it encounters a critical extension it does not recognize. A non-critical extension may be ignored if it is not recognized.

The ASN.1 definition for this is: 

```kotlin
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
Since not all extensions are known, the`getExtensionValue`method returns the DER-encoded OCTET STRING of the extension value (i.e., the`extnValue`). This can then be handled by a*Class* that understands the extension.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getCriticalExtensionOIDs](X509Extension.md))`()` Gets a Set of the OID strings for the extension(s) marked CRITICAL in the certificate/CRL managed by the object implementing this interface. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getExtensionValue](X509Extension.md))`(`oid:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the DER-encoded OCTET string for the extension value (*extnValue* ) identified by the passed-in`oid`String. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getNonCriticalExtensionOIDs](X509Extension.md))`()` Gets a Set of the OID strings for the extension(s) marked NON-CRITICAL in the certificate/CRL managed by the object implementing this interface. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasUnsupportedCriticalExtension](X509Extension.md))`()` Check if there is a critical extension that is not supported. |

## Public methods

### getCriticalExtensionOIDs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getCriticalExtensionOIDs(): MutableSet<String!>!
```

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

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a Set (or an empty Set if none are marked critical) of the extension OID strings for extensions that are marked critical. If there are no extensions present at all, then this method returns null. |

### getExtensionValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getExtensionValue(oid: String!): ByteArray!
```

Gets the DER-encoded OCTET string for the extension value (*extnValue* ) identified by the passed-in`oid`String. The`oid`string is represented by a set of nonnegative whole numbers separated by periods.

For example: 

| OID*(Object Identifier)* | Extension Name |
| --- | --- |
| 2.5.29.14 | SubjectKeyIdentifier |
| 2.5.29.15 | KeyUsage |
| 2.5.29.16 | PrivateKeyUsage |
| --- | --- |
| 2.5.29.17 | SubjectAlternativeName |
| 2.5.29.18 | IssuerAlternativeName |
| 2.5.29.19 | BasicConstraints |
| --- | --- |
| 2.5.29.30 | NameConstraints |
| 2.5.29.33 | PolicyMappings |
| 2.5.29.35 | AuthorityKeyIdentifier |
| --- | --- |
| 2.5.29.36 | PolicyConstraints |
|--------------------------|------------------------|

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `oid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Object Identifier value for the extension. |

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the DER-encoded octet string of the extension value or null if it is not present. |

### getNonCriticalExtensionOIDs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNonCriticalExtensionOIDs(): MutableSet<String!>!
```

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

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | a Set (or an empty Set if none are marked non-critical) of the extension OID strings for extensions that are marked non-critical. If there are no extensions present at all, then this method returns null. |

### hasUnsupportedCriticalExtension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasUnsupportedCriticalExtension(): Boolean
```

Check if there is a critical extension that is not supported.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if a critical extension is found that is not supported, otherwise`false`. |
