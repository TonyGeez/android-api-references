# java.security.cert

# java.security.cert

## Interfaces

| [CertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderResult) | A specification of the result of a certification path builder algorithm. |
| --- | --- |
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker) | Performs one or more checks on each`Certificate`of a`CertPath`. |
| [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters) | A specification of certification path algorithm parameters. |
| [CertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult) | A specification of the result of a certification path validator algorithm. |
| --- | --- |
| [CertSelector](https://developer.android.com/reference/kotlin/java/security/cert/CertSelector) | A selector that defines a set of criteria for selecting`Certificate`s. |
| [CertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreParameters) | A specification of`CertStore`parameters. |
| [CRLSelector](https://developer.android.com/reference/kotlin/java/security/cert/CRLSelector) | A selector that defines a set of criteria for selecting`CRL`s. |
| --- | --- |
| [Extension](https://developer.android.com/reference/kotlin/java/security/cert/Extension) | This interface represents an X. |
| [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode) | An immutable valid policy tree node as defined by the PKIX certification path validation algorithm. |
| [X509Extension](https://developer.android.com/reference/kotlin/java/security/cert/X509Extension) | Interface for an X. |
| --- | --- |

## Classes

| [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate) | Abstract class for managing a variety of identity certificates. |
| --- | --- |
| [CertificateFactory](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactory) | This class defines the functionality of a certificate factory, which is used to generate certificate, certification path () and certificate revocation list (CRL) objects from their encodings. |
| [CertificateFactorySpi](https://developer.android.com/reference/kotlin/java/security/cert/CertificateFactorySpi) | This class defines the*Service Provider Interface* (**SPI** ) for the`CertificateFactory`class. |
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath) | An immutable sequence of certificates (a certification path). |
| --- | --- |
| [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder) | A class for building certification paths (also known as certificate chains). |
| [CertPathBuilderSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi) | The*Service Provider Interface* (**SPI** ) for the [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder) class. |
| [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator) | A class for validating certification paths (also known as certificate chains). |
| --- | --- |
| [CertPathValidatorSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi) | The*Service Provider Interface* (**SPI** ) for the [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator) class. |
| [CertStore](https://developer.android.com/reference/kotlin/java/security/cert/CertStore) | A class for retrieving`Certificate`s and`CRL`s from a repository. |
| [CertStoreSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreSpi) | The*Service Provider Interface* (**SPI** ) for the [CertStore](https://developer.android.com/reference/kotlin/java/security/cert/CertStore) class. |
| --- | --- |
| [CollectionCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/CollectionCertStoreParameters) | Parameters used as input for the Collection`CertStore`algorithm. |
| [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL) | This class is an abstraction of certificate revocation lists (CRLs) that have different formats but important common uses. |
| [LDAPCertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/LDAPCertStoreParameters) | Parameters used as input for the LDAP`CertStore`algorithm. |
| --- | --- |
| [PKIXBuilderParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXBuilderParameters) | Parameters used as input for the PKIX`CertPathBuilder`algorithm. |
| [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult) | This class represents the successful result of the PKIX certification path builder algorithm. |
| [PKIXCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker) | An abstract class that performs one or more checks on an`X509Certificate`. |
| --- | --- |
| [PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult) | This class represents the successful result of the PKIX certification path validation algorithm. |
| [PKIXParameters](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters) | Parameters used as input for the PKIX`CertPathValidator`algorithm. |
| [PKIXRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker) | A`PKIXCertPathChecker`for checking the revocation status of certificates with the PKIX algorithm. |
| --- | --- |
| [PolicyQualifierInfo](https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo) | An immutable policy qualifier represented by the ASN. |
| [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor) | A trust anchor or most-trusted Certification Authority (CA). |
| [URICertStoreParameters](https://developer.android.com/reference/kotlin/java/security/cert/URICertStoreParameters) | Parameters used as input for`CertStore`algorithms which use information contained in a URI to retrieve certificates and CRLs. |
| --- | --- |
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate) | Abstract class for X. |
| [X509CertSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector) | A`CertSelector`that selects`X509Certificates`that match all specified criteria. |
| [X509CRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRL) | Abstract class for an X. |
| --- | --- |
| [X509CRLEntry](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLEntry) | Abstract class for a revoked certificate in a CRL (Certificate Revocation List). |
| [X509CRLSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector) | A`CRLSelector`that selects`X509CRLs`that match all specified criteria. |

## Exceptions

| [CertificateEncodingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateEncodingException) | Certificate Encoding Exception. |
| --- | --- |
| [CertificateException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateException) | This exception indicates one of a variety of certificate problems. |
| [CertificateExpiredException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateExpiredException) | Certificate Expired Exception. |
| [CertificateNotYetValidException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateNotYetValidException) | Certificate is not yet valid exception. |
| --- | --- |
| [CertificateParsingException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateParsingException) | Certificate Parsing Exception. |
| [CertificateRevokedException](https://developer.android.com/reference/kotlin/java/security/cert/CertificateRevokedException) | An exception that indicates an X. |
| [CertPathBuilderException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderException) | An exception indicating one of a variety of problems encountered when building a certification path with a`CertPathBuilder`. |
| --- | --- |
| [CertPathValidatorException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException) | An exception indicating one of a variety of problems encountered when validating a certification path. |
| [CertStoreException](https://developer.android.com/reference/kotlin/java/security/cert/CertStoreException) | An exception indicating one of a variety of problems retrieving certificates and CRLs from a`CertStore`. |
| [CRLException](https://developer.android.com/reference/kotlin/java/security/cert/CRLException) | CRL (Certificate Revocation List) Exception. |
| --- | --- |

## Enums

| [CRLReason](https://developer.android.com/reference/kotlin/java/security/cert/CRLReason) | The CRLReason enumeration specifies the reason that a certificate is revoked, as defined in [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280). |
| --- | --- |
| [PKIXReason](https://developer.android.com/reference/kotlin/java/security/cert/PKIXReason) | The`PKIXReason`enumerates the potential PKIX-specific reasons that an X. |
