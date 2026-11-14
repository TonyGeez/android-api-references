# CertificateFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateFactory

```
open class CertificateFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertificateFactory](CertificateFactory.md) |

This class defines the functionality of a certificate factory, which is used to generate certificate, certification path () and certificate revocation list (CRL) objects from their encodings.

For encodings consisting of multiple certificates, use`generateCertificates`when you want to parse a collection of possibly unrelated certificates. Otherwise, use`generateCertPath`when you want to generate a`CertPath`(a certificate chain) and subsequently validate it with a`CertPathValidator`.

A certificate factory for X.509 must return certificates that are an instance of`java.security.cert.X509Certificate`, and CRLs that are an instance of`java.security.cert.X509CRL`.

The following example reads a file with Base64 encoded certificates, which are each bounded at the beginning by -----BEGIN CERTIFICATE-----, and bounded at the end by -----END CERTIFICATE-----. We convert the`FileInputStream`(which does not support`mark`and`reset`) to a`BufferedInputStream`(which supports those methods), so that each call to`generateCertificate`consumes only one certificate, and the read position of the input stream is positioned to the next certificate in the file: 

```kotlin
<code>FileInputStream fis = new FileInputStream(filename);
  BufferedInputStream bis = new BufferedInputStream(fis);
 
  CertificateFactory cf = CertificateFactory.getInstance("X.509");
 
  while (bis.available() &gt; 0) {
     Certificate cert = cf.generateCertificate(bis);
     System.out.println(cert.toString());
  }
  </code>
```

The following example parses a PKCS#7-formatted certificate reply stored in a file and extracts all the certificates from it: 

```kotlin
FileInputStream fis = new FileInputStream(filename);
  CertificateFactory cf = CertificateFactory.getInstance("X.509");
  Collection c = cf.generateCertificates(fis);
  Iterator i = c.iterator();
  while (i.hasNext()) {
     Certificate cert = (Certificate)i.next();
     System.out.println(cert);
  }
  
```

Android provides the following`CertificateFactory`types:

| Algorithm | Supported API Levels |
|-----------|----------------------|
| X.509 | 1+ |

and the following`CertPath`encodings:

| Name | Supported (API Levels) |
|---------|------------------------|
| PKCS7 | 1+ |
| PkiPath | 1+ |

The type and encodings are described in the [CertificateFactory section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertificateFactory) and the [CertPath Encodings section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertPathEncodings) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateFactory](CertificateFactory.md))`(`certFacSpi:` ` [CertificateFactorySpi](CertificateFactorySpi.md)!`, `provider:` ` [Provider](../java.security/Provider.md)!`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a CertificateFactory object of the given type, and encapsulates the given provider implementation (SPI object) in it. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CRL](CRL.md)! | [generateCRL](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Generates a certificate revocation list (CRL) object and initializes it with the data read from the input stream`inStream`. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [CRL](CRL.md)!\>! | [generateCRLs](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Returns a (possibly empty) collection view of the CRLs read from the given input stream`inStream`. |
| [CertPath](CertPath.md)! | [generateCertPath](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. |
| --- | --- |
| [CertPath](CertPath.md)! | [generateCertPath](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. |
| [CertPath](CertPath.md)! | [generateCertPath](CertificateFactory.md))`(`certificates:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [Certificate](Certificate.md)!>!`)` Generates a`CertPath`object and initializes it with a`List`of`Certificate`s. |
| [Certificate](Certificate.md)! | [generateCertificate](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Generates a certificate object and initializes it with the data read from the input stream`inStream`. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Certificate](Certificate.md)!\>! | [generateCertificates](CertificateFactory.md))`(`inStream:` ` [InputStream](../java.io/InputStream.md)!`)` Returns a (possibly empty) collection view of the certificates read from the given input stream`inStream`. |
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getCertPathEncodings](CertificateFactory.md))`()` Returns an iteration of the`CertPath`encodings supported by this certificate factory, with the default encoding first. |
| static [CertificateFactory](CertificateFactory.md)! | [getInstance](CertificateFactory.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a certificate factory object that implements the specified certificate type. |
| --- | --- |
| static [CertificateFactory](CertificateFactory.md)! | [getInstance](CertificateFactory.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a certificate factory object for the specified certificate type. |
| static [CertificateFactory](CertificateFactory.md)! | [getInstance](CertificateFactory.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java.security/Provider.md)!`)` Returns a certificate factory object for the specified certificate type. |
| [Provider](../java.security/Provider.md)! | [getProvider](CertificateFactory.md))`()` Returns the provider of this certificate factory. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getType](CertificateFactory.md))`()` Returns the name of the certificate type associated with this certificate factory. |

## Protected constructors

### CertificateFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CertificateFactory(
    certFacSpi: CertificateFactorySpi!, 
    provider: Provider!, 
    type: String!)
```

Creates a CertificateFactory object of the given type, and encapsulates the given provider implementation (SPI object) in it.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `certFacSpi` | [CertificateFactorySpi](CertificateFactorySpi.md)!:the provider implementation. |
| `provider` | [Provider](../java.security/Provider.md)!:the provider. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the certificate type. |
| --- | --- |

## Public methods

### generateCRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCRL(inStream: InputStream!): CRL!
```

Generates a certificate revocation list (CRL) object and initializes it with the data read from the input stream`inStream`.

In order to take advantage of the specialized CRL format supported by this certificate factory, the returned CRL object can be typecast to the corresponding CRL class. For example, if this certificate factory implements X.509 CRLs, the returned CRL object can be typecast to the`X509CRL`class.

Note that if the given input stream does not support [mark](../java.io/InputStream.md))and [reset](../java.io/InputStream.md)), this method will consume the entire input stream. Otherwise, each call to this method consumes one CRL and the read position of the input stream is positioned to the next available byte after the inherent end-of-CRL marker. If the data in the input stream does not contain an inherent end-of-CRL marker (other than EOF) and there is trailing data after the CRL is parsed, a`CRLException`is thrown.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:an input stream with the CRL data. |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CRL](CRL.md)! | a CRL object initialized with the data from the input stream. |

| Exceptions ||
|-----------------------------------|--------------------|
| `java.security.cert.CRLException` | on parsing errors. |

### generateCRLs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCRLs(inStream: InputStream!): MutableCollection<out CRL!>!
```

Returns a (possibly empty) collection view of the CRLs read from the given input stream`inStream`.

In order to take advantage of the specialized CRL format supported by this certificate factory, each element in the returned collection view can be typecast to the corresponding CRL class. For example, if this certificate factory implements X.509 CRLs, the elements in the returned collection can be typecast to the`X509CRL`class.

In the case of a certificate factory for X.509 CRLs,`inStream`may contain a sequence of DER-encoded CRLs. In addition,`inStream`may contain a PKCS#7 CRL set. This is a PKCS#7*SignedData* object, with the only significant field being*crls*. In particular, the signature and the contents are ignored. This format allows multiple CRLs to be downloaded at once. If no CRLs are present, an empty collection is returned.

Note that if the given input stream does not support [mark](../java.io/InputStream.md))and [reset](../java.io/InputStream.md)), this method will consume the entire input stream.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:the input stream with the CRLs. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [CRL](CRL.md)!>! | a (possibly empty) collection view of java.security.cert.CRL objects initialized with the data from the input stream. |

| Exceptions ||
|-----------------------------------|--------------------|
| `java.security.cert.CRLException` | on parsing errors. |

### generateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCertPath(inStream: InputStream!): CertPath!
```

Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. The data is assumed to be in the default encoding. The name of the default encoding is the first element of the`Iterator`returned by the [getCertPathEncodings](CertificateFactory.md))method.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:an`InputStream`containing the data |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [CertPath](CertPath.md)! | a`CertPath`initialized with the data from the`InputStream` |

| Exceptions ||
|-------------------------------------------|---------------------------------------|
| `java.security.cert.CertificateException` | if an exception occurs while decoding |

### generateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCertPath(
    inStream: InputStream!, 
    encoding: String!
): CertPath!
```

Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. The data is assumed to be in the specified encoding. See the CertPath Encodings section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertPathEncodings) for information about standard encoding names and their formats.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:an`InputStream`containing the data |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the encoding used for the data |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [CertPath](CertPath.md)! | a`CertPath`initialized with the data from the`InputStream` |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.security.cert.CertificateException` | if an exception occurs while decoding or the encoding requested is not supported |

### generateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCertPath(certificates: MutableList<out Certificate!>!): CertPath!
```

Generates a`CertPath`object and initializes it with a`List`of`Certificate`s.

The certificates supplied must be of a type supported by the`CertificateFactory`. They will be copied out of the supplied`List`object.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certificates` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [Certificate](Certificate.md)!\>!:a`List`of`Certificate`s |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CertPath](CertPath.md)! | a`CertPath`initialized with the supplied list of certificates |

| Exceptions ||
|-------------------------------------------|------------------------|
| `java.security.cert.CertificateException` | if an exception occurs |

### generateCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCertificate(inStream: InputStream!): Certificate!
```

Generates a certificate object and initializes it with the data read from the input stream`inStream`.

In order to take advantage of the specialized certificate format supported by this certificate factory, the returned certificate object can be typecast to the corresponding certificate class. For example, if this certificate factory implements X.509 certificates, the returned certificate object can be typecast to the`X509Certificate`class.

In the case of a certificate factory for X.509 certificates, the certificate provided in`inStream`must be DER-encoded and may be supplied in binary or printable (Base64) encoding. If the certificate is provided in Base64 encoding, it must be bounded at the beginning by -----BEGIN CERTIFICATE-----, and must be bounded at the end by -----END CERTIFICATE-----.

Note that if the given input stream does not support [mark](../java.io/InputStream.md))and [reset](../java.io/InputStream.md)), this method will consume the entire input stream. Otherwise, each call to this method consumes one certificate and the read position of the input stream is positioned to the next available byte after the inherent end-of-certificate marker. If the data in the input stream does not contain an inherent end-of-certificate marker (other than EOF) and there is trailing data after the certificate is parsed, a`CertificateException`is thrown.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:an input stream with the certificate data. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Certificate](Certificate.md)! | a certificate object initialized with the data from the input stream. |

| Exceptions ||
|-------------------------------------------|--------------------|
| `java.security.cert.CertificateException` | on parsing errors. |

### generateCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generateCertificates(inStream: InputStream!): MutableCollection<out Certificate!>!
```

Returns a (possibly empty) collection view of the certificates read from the given input stream`inStream`.

In order to take advantage of the specialized certificate format supported by this certificate factory, each element in the returned collection view can be typecast to the corresponding certificate class. For example, if this certificate factory implements X.509 certificates, the elements in the returned collection can be typecast to the`X509Certificate`class.

In the case of a certificate factory for X.509 certificates,`inStream`may contain a sequence of DER-encoded certificates in the formats described for [generateCertificate](CertificateFactory.md)). In addition,`inStream`may contain a PKCS#7 certificate chain. This is a PKCS#7*SignedData* object, with the only significant field being*certificates*. In particular, the signature and the contents are ignored. This format allows multiple certificates to be downloaded at once. If no certificates are present, an empty collection is returned.

Note that if the given input stream does not support [mark](../java.io/InputStream.md))and [reset](../java.io/InputStream.md)), this method will consume the entire input stream.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](../java.io/InputStream.md)!:the input stream with the certificates. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Certificate](Certificate.md)!>! | a (possibly empty) collection view of java.security.cert.Certificate objects initialized with the data from the input stream. |

| Exceptions ||
|-------------------------------------------|--------------------|
| `java.security.cert.CertificateException` | on parsing errors. |

### getCertPathEncodings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCertPathEncodings(): MutableIterator<String!>!
```

Returns an iteration of the`CertPath`encodings supported by this certificate factory, with the default encoding first. See the CertPath Encodings section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertPathEncodings) for information about standard encoding names and their formats.

Attempts to modify the returned`Iterator`via its`remove`method result in an`UnsupportedOperationException`.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an`Iterator`over the names of the supported`CertPath`encodings (as`String`s) |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(type: String!): CertificateFactory!
```

Returns a certificate factory object that implements the specified certificate type.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new CertificateFactory object encapsulating the CertificateFactorySpi implementation from the first Provider that supports the specified type is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested certificate type. See the CertificateFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertificateFactory) for information about standard certificate types. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [CertificateFactory](CertificateFactory.md)! | a certificate factory object for the specified type. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------|
| `java.security.cert.CertificateException` | if no Provider supports a CertificateFactorySpi implementation for the specified type. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    type: String!, 
    provider: String!
): CertificateFactory!
```

Returns a certificate factory object for the specified certificate type.

A new CertificateFactory object encapsulating the CertificateFactorySpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java.security/Security.md))method.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the certificate type. See the CertificateFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertificateFactory) for information about standard certificate types. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [CertificateFactory](CertificateFactory.md)! | a certificate factory object for the specified type. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.security.cert.CertificateException` | if a CertificateFactorySpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| --- | --- |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    type: String!, 
    provider: Provider!
): CertificateFactory!
```

Returns a certificate factory object for the specified certificate type.

A new CertificateFactory object encapsulating the CertificateFactorySpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the certificate type. See the CertificateFactory section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#CertificateFactory) for information about standard certificate types. |
| `provider` | [Provider](../java.security/Provider.md)!:the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [CertificateFactory](CertificateFactory.md)! | a certificate factory object for the specified type. |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.security.cert.CertificateException` | if a CertificateFactorySpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |

**See Also**

- [java.security.Provider](../java.security/Provider.md) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this certificate factory.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------|
| [Provider](../java.security/Provider.md)! | the provider of this certificate factory. |

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String!
```

Returns the name of the certificate type associated with this certificate factory.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the certificate type associated with this certificate factory. |
