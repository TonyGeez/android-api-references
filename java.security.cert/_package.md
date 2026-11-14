# java.security.cert

# java.security.cert

## Interfaces

| [CertPathBuilderResult](CertPathBuilderResult.md) | A specification of the result of a certification path builder algorithm. |
| --- | --- |
| [CertPathChecker](CertPathChecker.md) | Performs one or more checks on each`Certificate`of a`CertPath`. |
| [CertPathParameters](CertPathParameters.md) | A specification of certification path algorithm parameters. |
| [CertPathValidatorResult](CertPathValidatorResult.md) | A specification of the result of a certification path validator algorithm. |
| --- | --- |
| [CertSelector](CertSelector.md) | A selector that defines a set of criteria for selecting`Certificate`s. |
| [CertStoreParameters](CertStoreParameters.md) | A specification of`CertStore`parameters. |
| [CRLSelector](CRLSelector.md) | A selector that defines a set of criteria for selecting`CRL`s. |
| --- | --- |
| [Extension](Extension.md) | This interface represents an X. |
| [PolicyNode](PolicyNode.md) | An immutable valid policy tree node as defined by the PKIX certification path validation algorithm. |
| [X509Extension](X509Extension.md) | Interface for an X. |
| --- | --- |

## Classes

| [Certificate](Certificate.md) | Abstract class for managing a variety of identity certificates. |
| --- | --- |
| [CertificateFactory](CertificateFactory.md) | This class defines the functionality of a certificate factory, which is used to generate certificate, certification path () and certificate revocation list (CRL) objects from their encodings. |
| [CertificateFactorySpi](CertificateFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`CertificateFactory`class. |
| [CertPath](CertPath.md) | An immutable sequence of certificates (a certification path). |
| --- | --- |
| [CertPathBuilder](CertPathBuilder.md) | A class for building certification paths (also known as certificate chains). |
| [CertPathBuilderSpi](CertPathBuilderSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertPathBuilder](CertPathBuilder.md) class. |
| [CertPathValidator](CertPathValidator.md) | A class for validating certification paths (also known as certificate chains). |
| --- | --- |
| [CertPathValidatorSpi](CertPathValidatorSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertPathValidator](CertPathValidator.md) class. |
| [CertStore](CertStore.md) | A class for retrieving`Certificate`s and`CRL`s from a repository. |
| [CertStoreSpi](CertStoreSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertStore](CertStore.md) class. |
| --- | --- |
| [CollectionCertStoreParameters](CollectionCertStoreParameters.md) | Parameters used as input for the Collection`CertStore`algorithm. |
| [CRL](CRL.md) | This class is an abstraction of certificate revocation lists (CRLs) that have different formats but important common uses. |
| [LDAPCertStoreParameters](LDAPCertStoreParameters.md) | Parameters used as input for the LDAP`CertStore`algorithm. |
| --- | --- |
| [PKIXBuilderParameters](PKIXBuilderParameters.md) | Parameters used as input for the PKIX`CertPathBuilder`algorithm. |
| [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) | This class represents the successful result of the PKIX certification path builder algorithm. |
| [PKIXCertPathChecker](PKIXCertPathChecker.md) | An abstract class that performs one or more checks on an`X509Certificate`. |
| --- | --- |
| [PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) | This class represents the successful result of the PKIX certification path validation algorithm. |
| [PKIXParameters](PKIXParameters.md) | Parameters used as input for the PKIX`CertPathValidator`algorithm. |
| [PKIXRevocationChecker](PKIXRevocationChecker.md) | A`PKIXCertPathChecker`for checking the revocation status of certificates with the PKIX algorithm. |
| --- | --- |
| [PolicyQualifierInfo](PolicyQualifierInfo.md) | An immutable policy qualifier represented by the ASN. |
| [TrustAnchor](TrustAnchor.md) | A trust anchor or most-trusted Certification Authority (CA). |
| [URICertStoreParameters](URICertStoreParameters.md) | Parameters used as input for`CertStore`algorithms which use information contained in a URI to retrieve certificates and CRLs. |
| --- | --- |
| [X509Certificate](X509Certificate.md) | Abstract class for X. |
| [X509CertSelector](X509CertSelector.md) | A`CertSelector`that selects`X509Certificates`that match all specified criteria. |
| [X509CRL](X509CRL.md) | Abstract class for an X. |
| --- | --- |
| [X509CRLEntry](X509CRLEntry.md) | Abstract class for a revoked certificate in a CRL (Certificate Revocation List). |
| [X509CRLSelector](X509CRLSelector.md) | A`CRLSelector`that selects`X509CRLs`that match all specified criteria. |

## Exceptions

| [CertificateEncodingException](CertificateEncodingException.md) | Certificate Encoding Exception. |
| --- | --- |
| [CertificateException](CertificateException.md) | This exception indicates one of a variety of certificate problems. |
| [CertificateExpiredException](CertificateExpiredException.md) | Certificate Expired Exception. |
| [CertificateNotYetValidException](CertificateNotYetValidException.md) | Certificate is not yet valid exception. |
| --- | --- |
| [CertificateParsingException](CertificateParsingException.md) | Certificate Parsing Exception. |
| [CertificateRevokedException](CertificateRevokedException.md) | An exception that indicates an X. |
| [CertPathBuilderException](CertPathBuilderException.md) | An exception indicating one of a variety of problems encountered when building a certification path with a`CertPathBuilder`. |
| --- | --- |
| [CertPathValidatorException](CertPathValidatorException.md) | An exception indicating one of a variety of problems encountered when validating a certification path. |
| [CertStoreException](CertStoreException.md) | An exception indicating one of a variety of problems retrieving certificates and CRLs from a`CertStore`. |
| [CRLException](CRLException.md) | CRL (Certificate Revocation List) Exception. |
| --- | --- |

## Enums

| [CRLReason](CRLReason.md) | The CRLReason enumeration specifies the reason that a certificate is revoked, as defined in [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280). |
| --- | --- |
| [PKIXReason](PKIXReason.md) | The`PKIXReason`enumerates the potential PKIX-specific reasons that an X. |
