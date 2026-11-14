# X509Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509Certificate

```
abstract class X509Certificate : Certificate
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [javax.security.cert.Certificate](Certificate.md) ||
| | ↳ | [javax.security.cert.X509Certificate](X509Certificate.md) |

Abstract class for X.509 v1 certificates. This provides a standard way to access all the version 1 attributes of an X.509 certificate. Attributes that are specific to X.509 v2 or v3 are not available through this interface. Future API evolution will provide full access to complete X.509 v3 attributes.

The basic X.509 format was defined by ISO/IEC and ANSI X9 and is described below in ASN.1: 

```kotlin
Certificate  ::=  SEQUENCE  {
      tbsCertificate       TBSCertificate,
      signatureAlgorithm   AlgorithmIdentifier,
      signature            BIT STRING  }
  
```

These certificates are widely used to support authentication and other functionality in Internet security systems. Common applications include Privacy Enhanced Mail (PEM), Transport Layer Security (SSL), code signing for trusted software distribution, and Secure Electronic Transactions (SET).

These certificates are managed and vouched for by*Certificate Authorities*(CAs). CAs are services which create certificates by placing data in the X.509 standard format and then digitally signing that data. CAs act as trusted third parties, making introductions between principals who have no direct knowledge of each other. CA certificates are either signed by themselves, or by some other CA such as a "root" CA.

The ASN.1 definition of`tbsCertificate`is: 

```kotlin
TBSCertificate  ::=  SEQUENCE  {
      version         [0]  EXPLICIT Version DEFAULT v1,
      serialNumber         CertificateSerialNumber,
      signature            AlgorithmIdentifier,
      issuer               Name,
      validity             Validity,
      subject              Name,
      subjectPublicKeyInfo SubjectPublicKeyInfo,
      }
  
```

Here is sample code to instantiate an X.509 certificate: 

```kotlin
InputStream inStream = new FileInputStream("fileName-of-cert");
  X509Certificate cert = X509Certificate.getInstance(inStream);
  inStream.close();
  
```
OR 

```kotlin
byte[] certData = <certificate read from a file, say>
  X509Certificate cert = X509Certificate.getInstance(certData);
  
```

In either case, the code that instantiates an X.509 certificate consults the value of the`cert.provider.x509v1`security property to locate the actual implementation or instantiates a default implementation.

The`cert.provider.x509v1`property is set to a default implementation for X.509 such as: 

```kotlin
cert.provider.x509v1=com.sun.security.cert.internal.x509.X509V1CertImpl
  
```

The value of this`cert.provider.x509v1`property has to be changed to instantiate another implementation. If this security property is not set, a default implementation will be used. Currently, due to possible security restrictions on access to Security properties, this value is looked up and cached at class initialization time and will fallback on a default implementation if the Security property is not accessible.

*Note: The classes in the package`javax.security.cert`exist for compatibility with earlier versions of the Java Secure Sockets Extension (JSSE). New applications should instead use the standard Java SE certificate classes located in`java.security.cert`.*

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509Certificate](X509Certificate.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkValidity](X509Certificate.md))`()` Checks that the certificate is currently valid. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkValidity](X509Certificate.md))`(`date:` ` [Date](../java.util/Date.md)!`)` Checks that the specified date is within the certificate's validity period. |
| static [X509Certificate](X509Certificate.md)! | [getInstance](X509Certificate.md))`(`certData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Instantiates an X509Certificate object, and initializes it with the specified byte array. |
| --- | --- |
| static [X509Certificate](X509Certificate.md)! | [getInstance](X509Certificate.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Instantiates an X509Certificate object, and initializes it with the data read from the input stream`inStream`. |
| abstract [Principal](../java.security/Principal.md)! | [getIssuerDN](X509Certificate.md))`()` Gets the`issuer`(issuer distinguished name) value from the certificate. |
| abstract [Date](../java.util/Date.md)! | [getNotAfter](X509Certificate.md))`()` Gets the`notAfter`date from the validity period of the certificate. |
| --- | --- |
| abstract [Date](../java.util/Date.md)! | [getNotBefore](X509Certificate.md))`()` Gets the`notBefore`date from the validity period of the certificate. |
| abstract [BigInteger](../java.math/BigInteger.md)! | [getSerialNumber](X509Certificate.md))`()` Gets the`serialNumber`value from the certificate. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSigAlgName](X509Certificate.md))`()` Gets the signature algorithm name for the certificate signature algorithm. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSigAlgOID](X509Certificate.md))`()` Gets the signature algorithm OID string from the certificate. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSigAlgParams](X509Certificate.md))`()` Gets the DER-encoded signature algorithm parameters from this certificate's signature algorithm. |
| abstract [Principal](../java.security/Principal.md)! | [getSubjectDN](X509Certificate.md))`()` Gets the`subject`(subject distinguished name) value from the certificate. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](X509Certificate.md))`()` Gets the`version`(version number) value from the certificate. |

| Inherited functions ||
|---|---|
| From class [Certificate](Certificate.md) |--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Certificate.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares this certificate for equality with the specified object. If the`other`object is an`instanceof``Certificate`, then its encoded form is retrieved and compared with the encoded form of this certificate. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](Certificate.md))`()` <br /> Returns the encoded form of this certificate. It is assumed that each certificate type would have only a single form of encoding; for example, X.509 certificates would be encoded as ASN.1 DER. <br /> | | [PublicKey](../java.security/PublicKey.md)! | [getPublicKey](Certificate.md))`()` <br /> Gets the public key from this certificate. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Certificate.md))`()` <br /> Returns a hashcode value for this certificate from its encoded form. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Certificate.md))`()` <br /> Returns a string representation of this certificate. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](Certificate.md))`(`key:` ` [PublicKey](../java.security/PublicKey.md)!`)` <br /> Verifies that this certificate was signed using the private key that corresponds to the specified public key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [verify](Certificate.md))`(`key:` ` [PublicKey](../java.security/PublicKey.md)!`, `sigProvider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Verifies that this certificate was signed using the private key that corresponds to the specified public key. This method uses the signature verification engine supplied by the specified provider. <br /> | ||

## Public constructors

### X509Certificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509Certificate()
```

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
|-------------------------------------------------------|--------------------------------------|
| `javax.security.cert.CertificateExpiredException` | if the certificate has expired. |
| `javax.security.cert.CertificateNotYetValidException` | if the certificate is not yet valid. |

### checkValidity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkValidity(date: Date!): Unit
```

Checks that the specified date is within the certificate's validity period. In other words, this determines whether the certificate would be valid at the specified date/time.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `date` | [Date](../java.util/Date.md)!:the Date to check against to see if this certificate is valid at that date/time. |

| Exceptions ||
|-------------------------------------------------------|------------------------------------------------------------------------|
| `javax.security.cert.CertificateExpiredException` | if the certificate has expired with respect to the`date`supplied. |
| `javax.security.cert.CertificateNotYetValidException` | if the certificate is not yet valid with respect to the`date`supplied. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate#checkValidity()> 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(certData: ByteArray!): X509Certificate!
```

Instantiates an X509Certificate object, and initializes it with the specified byte array. The implementation (X509Certificate is an abstract class) is provided by the class specified as the value of the`cert.provider.x509v1`security property.

Note: All X509Certificate subclasses must provide a constructor of the form: 

```kotlin
<code>public &lt;subClass&gt;(InputStream inStream) ...
  </code>
```

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `certData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the DER-encoded certificate. |

| Return ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [X509Certificate](X509Certificate.md)! | an X509Certificate object initialized with the data from`certData`. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------|
| `javax.security.cert.CertificateException` | if a class initialization or certificate parsing error occurs. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(inStream: InputStream!): X509Certificate!
```

Instantiates an X509Certificate object, and initializes it with the data read from the input stream`inStream`. The implementation (X509Certificate is an abstract class) is provided by the class specified as the value of the`cert.provider.x509v1`security property.

Note: Only one DER-encoded certificate is expected to be in the input stream. Also, all X509Certificate subclasses must provide a constructor of the form: 

```kotlin
<code>public &lt;subClass&gt;(InputStream inStream) ...
  </code>
```

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:an input stream with the data to be read to initialize the certificate. |

| Return ||
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [X509Certificate](X509Certificate.md)! | an X509Certificate object initialized with the data from the input stream. |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------|
| `javax.security.cert.CertificateException` | if a class initialization or certificate parsing error occurs. |

### getIssuerDN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIssuerDN(): Principal!
```

Gets the`issuer`(issuer distinguished name) value from the certificate. The issuer name identifies the entity that signed (and issued) the certificate.

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
The`Name`describes a hierarchical name composed of attributes, such as country name, and corresponding values, such as US. The type of the`AttributeValue`component is determined by the`AttributeType`; in general it will be a`directoryString`. A`directoryString`is usually one of`PrintableString`,`TeletexString`or`UniversalString`.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Principal](../java.security/Principal.md)! | a Principal whose name is the issuer distinguished name. |

### getNotAfter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNotAfter(): Date!
```

Gets the`notAfter`date from the validity period of the certificate. See [getNotBefore](X509Certificate.md))for relevant ASN.1 definitions.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Date](../java.util/Date.md)! | the end date of the validity period. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate#checkValidity()> 

### getNotBefore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNotBefore(): Date!
```

Gets the`notBefore`date from the validity period of the certificate. The relevant ASN.1 definitions are: 

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
|------------------------------------------------------------------------------|----------------------------------------|
| [Date](../java.util/Date.md)! | the start date of the validity period. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate#checkValidity()> 

### getSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSerialNumber(): BigInteger!
```

Gets the`serialNumber`value from the certificate. The serial number is an integer assigned by the certification authority to each certificate. It must be unique for each certificate issued by a given CA (i.e., the issuer name and serial number identify a unique certificate). The ASN.1 definition for this is: 

```kotlin
serialNumber     CertificateSerialNumber
 
  CertificateSerialNumber  ::=  INTEGER
  
```

<br />

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [BigInteger](../java.math/BigInteger.md)! | the serial number. |

### getSigAlgName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSigAlgName(): String!
```

Gets the signature algorithm name for the certificate signature algorithm. An example is the string "SHA-1/DSA". The ASN.1 definition for this is: 

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

The algorithm name is determined from the`algorithm`OID string.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the signature algorithm name. |

### getSigAlgOID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSigAlgOID(): String!
```

Gets the signature algorithm OID string from the certificate. An OID is represented by a set of positive whole numbers separated by periods. For example, the string "1.2.840.10040.4.3" identifies the SHA-1 with DSA signature algorithm, as per the PKIX part I.

See [getSigAlgName](X509Certificate.md))for relevant ASN.1 definitions.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the signature algorithm OID string. |

### getSigAlgParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSigAlgParams(): ByteArray!
```

Gets the DER-encoded signature algorithm parameters from this certificate's signature algorithm. In most cases, the signature algorithm parameters are null; the parameters are usually supplied with the certificate's public key.

See [getSigAlgName](X509Certificate.md))for relevant ASN.1 definitions.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the DER-encoded signature algorithm parameters, or null if no parameters are present. |

### getSubjectDN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSubjectDN(): Principal!
```

Gets the`subject`(subject distinguished name) value from the certificate. The ASN.1 definition for this is: 

```kotlin
subject    Name
  
```

<br />

See [getIssuerDN](X509Certificate.md))for`Name`and other relevant definitions.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------|
| [Principal](../java.security/Principal.md)! | a Principal whose name is the subject name. |

**See Also**

- <https://developer.android.com/reference/kotlin/javax/security/cert/X509Certificate#getIssuerDN()> 

### getVersion

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getVersion(): Int
```

Gets the`version`(version number) value from the certificate. The ASN.1 definition for this is: 

```kotlin
version         [0]  EXPLICIT Version DEFAULT v1
 
  Version  ::=  INTEGER  {  v1(0), v2(1), v3(2)  }
  
```

<br />

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the version number from the ASN.1 encoding, i.e. 0, 1 or 2. |
