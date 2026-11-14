# CertificateFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertificateFactorySpi

```
abstract class CertificateFactorySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.CertificateFactorySpi](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`CertificateFactory`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a certificate factory for a particular certificate type, e.g., X.509.

Certificate factories are used to generate certificate, certification path (`CertPath`) and certificate revocation list (CRL) objects from their encodings.

A certificate factory for X.509 must return certificates that are an instance of`java.security.cert.X509Certificate`, and CRLs that are an instance of`java.security.cert.X509CRL`.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertificateFactorySpi](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#CertificateFactorySpi())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)! | [engineGenerateCRL](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCRL(java.io.InputStream))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Generates a certificate revocation list (CRL) object and initializes it with the data read from the input stream`inStream`. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)!\>! | [engineGenerateCRLs](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCRLs(java.io.InputStream))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Returns a (possibly empty) collection view of the CRLs read from the given input stream`inStream`. |
| open [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | [engineGenerateCertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCertPath(java.io.InputStream))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. |
| open [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | [engineGenerateCertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCertPath(java.io.InputStream,%20kotlin.String))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. |
| open [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | [engineGenerateCertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCertPath(kotlin.collections.MutableList))`(`certificates:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<out` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!>!`)` Generates a`CertPath`object and initializes it with a`List`of`Certificate`s. |
| abstract [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)! | [engineGenerateCertificate](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCertificate(java.io.InputStream))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Generates a certificate object and initializes it with the data read from the input stream`inStream`. |
| abstract [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>! | [engineGenerateCertificates](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGenerateCertificates(java.io.InputStream))`(`inStream:` ` [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!`)` Returns a (possibly empty) collection view of the certificates read from the given input stream`inStream`. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [engineGetCertPathEncodings](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi#engineGetCertPathEncodings())`()` Returns an iteration of the`CertPath`encodings supported by this certificate factory, with the default encoding first. |

## Public constructors

### CertificateFactorySpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CertificateFactorySpi()
```

## Public methods

### engineGenerateCRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGenerateCRL(inStream: InputStream!): CRL!
```

Generates a certificate revocation list (CRL) object and initializes it with the data read from the input stream`inStream`.

In order to take advantage of the specialized CRL format supported by this certificate factory, the returned CRL object can be typecast to the corresponding CRL class. For example, if this certificate factory implements X.509 CRLs, the returned CRL object can be typecast to the`X509CRL`class.

Note that if the given input stream does not support [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))and [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()), this method will consume the entire input stream. Otherwise, each call to this method consumes one CRL and the read position of the input stream is positioned to the next available byte after the inherent end-of-CRL marker. If the data in the input stream does not contain an inherent end-of-CRL marker (other than EOF) and there is trailing data after the CRL is parsed, a`CRLException`is thrown.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an input stream with the CRL data. |

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)! | a CRL object initialized with the data from the input stream. |

| Exceptions ||
|-----------------------------------|--------------------|
| `java.security.cert.CRLException` | on parsing errors. |

### engineGenerateCRLs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGenerateCRLs(inStream: InputStream!): MutableCollection<out CRL!>!
```

Returns a (possibly empty) collection view of the CRLs read from the given input stream`inStream`.

In order to take advantage of the specialized CRL format supported by this certificate factory, each element in the returned collection view can be typecast to the corresponding CRL class. For example, if this certificate factory implements X.509 CRLs, the elements in the returned collection can be typecast to the`X509CRL`class.

In the case of a certificate factory for X.509 CRLs,`inStream`may contain a single DER-encoded CRL. In addition,`inStream`may contain a PKCS#7 CRL set. This is a PKCS#7*SignedData* object, with the only significant field being*crls*. In particular, the signature and the contents are ignored. This format allows multiple CRLs to be downloaded at once. If no CRLs are present, an empty collection is returned.

Note that if the given input stream does not support [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))and [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()), this method will consume the entire input stream.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream with the CRLs. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)!>! | a (possibly empty) collection view of java.security.cert.CRL objects initialized with the data from the input stream. |

| Exceptions ||
|-----------------------------------|--------------------|
| `java.security.cert.CRLException` | on parsing errors. |

### engineGenerateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGenerateCertPath(inStream: InputStream!): CertPath!
```

Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. The data is assumed to be in the default encoding.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be`abstract`and by default throws an`UnsupportedOperationException`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an`InputStream`containing the data |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | a`CertPath`initialized with the data from the`InputStream` |

| Exceptions ||
|-------------------------------------------|---------------------------------------|
| `java.security.cert.CertificateException` | if an exception occurs while decoding |
| `java.lang.UnsupportedOperationException` | if the method is not supported |

### engineGenerateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGenerateCertPath(
    inStream: InputStream!, 
    encoding: String!
): CertPath!
```

Generates a`CertPath`object and initializes it with the data read from the`InputStream`inStream. The data is assumed to be in the specified encoding.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be`abstract`and by default throws an`UnsupportedOperationException`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an`InputStream`containing the data |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the encoding used for the data |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | a`CertPath`initialized with the data from the`InputStream` |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.security.cert.CertificateException` | if an exception occurs while decoding or the encoding requested is not supported |
| `java.lang.UnsupportedOperationException` | if the method is not supported |

### engineGenerateCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGenerateCertPath(certificates: MutableList<out Certificate!>!): CertPath!
```

Generates a`CertPath`object and initializes it with a`List`of`Certificate`s.

The certificates supplied must be of a type supported by the`CertificateFactory`. They will be copied out of the supplied`List`object.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be`abstract`and by default throws an`UnsupportedOperationException`.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certificates` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<out [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!\>!:a`List`of`Certificate`s |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | a`CertPath`initialized with the supplied list of certificates |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.security.cert.CertificateException` | if an exception occurs |
| `java.lang.UnsupportedOperationException` | if the method is not supported |

### engineGenerateCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGenerateCertificate(inStream: InputStream!): Certificate!
```

Generates a certificate object and initializes it with the data read from the input stream`inStream`.

In order to take advantage of the specialized certificate format supported by this certificate factory, the returned certificate object can be typecast to the corresponding certificate class. For example, if this certificate factory implements X.509 certificates, the returned certificate object can be typecast to the`X509Certificate`class.

In the case of a certificate factory for X.509 certificates, the certificate provided in`inStream`must be DER-encoded and may be supplied in binary or printable (Base64) encoding. If the certificate is provided in Base64 encoding, it must be bounded at the beginning by -----BEGIN CERTIFICATE-----, and must be bounded at the end by -----END CERTIFICATE-----.

Note that if the given input stream does not support [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))and [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()), this method will consume the entire input stream. Otherwise, each call to this method consumes one certificate and the read position of the input stream is positioned to the next available byte after the inherent end-of-certificate marker. If the data in the input stream does not contain an inherent end-of-certificate marker (other than EOF) and there is trailing data after the certificate is parsed, a`CertificateException`is thrown.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:an input stream with the certificate data. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)! | a certificate object initialized with the data from the input stream. |

| Exceptions ||
|-------------------------------------------|--------------------|
| `java.security.cert.CertificateException` | on parsing errors. |

### engineGenerateCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun engineGenerateCertificates(inStream: InputStream!): MutableCollection<out Certificate!>!
```

Returns a (possibly empty) collection view of the certificates read from the given input stream`inStream`.

In order to take advantage of the specialized certificate format supported by this certificate factory, each element in the returned collection view can be typecast to the corresponding certificate class. For example, if this certificate factory implements X.509 certificates, the elements in the returned collection can be typecast to the`X509Certificate`class.

In the case of a certificate factory for X.509 certificates,`inStream`may contain a single DER-encoded certificate in the formats described for [generateCertificate](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactory#generateCertificate(java.io.InputStream)). In addition,`inStream`may contain a PKCS#7 certificate chain. This is a PKCS#7*SignedData* object, with the only significant field being*certificates*. In particular, the signature and the contents are ignored. This format allows multiple certificates to be downloaded at once. If no certificates are present, an empty collection is returned.

Note that if the given input stream does not support [mark](https://developer.android.com/reference/kotlin/java/io/InputStream.html#mark(kotlin.Int))and [reset](https://developer.android.com/reference/kotlin/java/io/InputStream.html#reset()), this method will consume the entire input stream.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------|
| `inStream` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)!:the input stream with the certificates. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!>! | a (possibly empty) collection view of java.security.cert.Certificate objects initialized with the data from the input stream. |

| Exceptions ||
|-------------------------------------------|--------------------|
| `java.security.cert.CertificateException` | on parsing errors. |

### engineGetCertPathEncodings

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun engineGetCertPathEncodings(): MutableIterator<String!>!
```

Returns an iteration of the`CertPath`encodings supported by this certificate factory, with the default encoding first. See the CertPath Encodings section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpath-encodings) for information about standard encoding names.

Attempts to modify the returned`Iterator`via its`remove`method result in an`UnsupportedOperationException`.

This method was added to version 1.4 of the Java 2 Platform Standard Edition. In order to maintain backwards compatibility with existing service providers, this method cannot be`abstract`and by default throws an`UnsupportedOperationException`.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an`Iterator`over the names of the supported`CertPath`encodings (as`String`s) |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.lang.UnsupportedOperationException` | if the method is not supported |
