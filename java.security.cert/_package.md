# java.security.cert

# java.security.cert

## Interfaces

| [CertPathBuilderResult](../java/security/cert/CertPathBuilderResult.md) | A specification of the result of a certification path builder algorithm. |
| --- | --- |
| [CertPathChecker](../java/security/cert/CertPathChecker.md) | Performs one or more checks on each`Certificate`of a`CertPath`. |
| [CertPathParameters](../java/security/cert/CertPathParameters.md) | A specification of certification path algorithm parameters. |
| [CertPathValidatorResult](../java/security/cert/CertPathValidatorResult.md) | A specification of the result of a certification path validator algorithm. |
| --- | --- |
| [CertSelector](../java/security/cert/CertSelector.md) | A selector that defines a set of criteria for selecting`Certificate`s. |
| [CertStoreParameters](../java/security/cert/CertStoreParameters.md) | A specification of`CertStore`parameters. |
| [CRLSelector](../java/security/cert/CRLSelector.md) | A selector that defines a set of criteria for selecting`CRL`s. |
| --- | --- |
| [Extension](../java/security/cert/Extension.md) | This interface represents an X. |
| [PolicyNode](../java/security/cert/PolicyNode.md) | An immutable valid policy tree node as defined by the PKIX certification path validation algorithm. |
| [X509Extension](../java/security/cert/X509Extension.md) | Interface for an X. |
| --- | --- |

## Classes

| [Certificate](../java/security/cert/Certificate.md) | Abstract class for managing a variety of identity certificates. |
| --- | --- |
| [CertificateFactory](../java/security/cert/CertificateFactory.md) | This class defines the functionality of a certificate factory, which is used to generate certificate, certification path () and certificate revocation list (CRL) objects from their encodings. |
| [CertificateFactorySpi](../java/security/cert/CertificateFactorySpi.md) | This class defines the*Service Provider Interface* (**SPI** ) for the`CertificateFactory`class. |
| [CertPath](../java/security/cert/CertPath.md) | An immutable sequence of certificates (a certification path). |
| --- | --- |
| [CertPathBuilder](../java/security/cert/CertPathBuilder.md) | A class for building certification paths (also known as certificate chains). |
| [CertPathBuilderSpi](../java/security/cert/CertPathBuilderSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertPathBuilder](../java/security/cert/CertPathBuilder.md) class. |
| [CertPathValidator](../java/security/cert/CertPathValidator.md) | A class for validating certification paths (also known as certificate chains). |
| --- | --- |
| [CertPathValidatorSpi](../java/security/cert/CertPathValidatorSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertPathValidator](../java/security/cert/CertPathValidator.md) class. |
| [CertStore](../java/security/cert/CertStore.md) | A class for retrieving`Certificate`s and`CRL`s from a repository. |
| [CertStoreSpi](../java/security/cert/CertStoreSpi.md) | The*Service Provider Interface* (**SPI** ) for the [CertStore](../java/security/cert/CertStore.md) class. |
| --- | --- |
| [CollectionCertStoreParameters](../java/security/cert/CollectionCertStoreParameters.md) | Parameters used as input for the Collection`CertStore`algorithm. |
| [CRL](../java/security/cert/CRL.md) | This class is an abstraction of certificate revocation lists (CRLs) that have different formats but important common uses. |
| [LDAPCertStoreParameters](../java/security/cert/LDAPCertStoreParameters.md) | Parameters used as input for the LDAP`CertStore`algorithm. |
| --- | --- |
| [PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md) | Parameters used as input for the PKIX`CertPathBuilder`algorithm. |
| [PKIXCertPathBuilderResult](../java/security/cert/PKIXCertPathBuilderResult.md) | This class represents the successful result of the PKIX certification path builder algorithm. |
| [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md) | An abstract class that performs one or more checks on an`X509Certificate`. |
| --- | --- |
| [PKIXCertPathValidatorResult](../java/security/cert/PKIXCertPathValidatorResult.md) | This class represents the successful result of the PKIX certification path validation algorithm. |
| [PKIXParameters](../java/security/cert/PKIXParameters.md) | Parameters used as input for the PKIX`CertPathValidator`algorithm. |
| [PKIXRevocationChecker](../java/security/cert/PKIXRevocationChecker.md) | A`PKIXCertPathChecker`for checking the revocation status of certificates with the PKIX algorithm. |
| --- | --- |
| [PolicyQualifierInfo](../java/security/cert/PolicyQualifierInfo.md) | An immutable policy qualifier represented by the ASN. |
| [TrustAnchor](../java/security/cert/TrustAnchor.md) | A trust anchor or most-trusted Certification Authority (CA). |
| [URICertStoreParameters](../java/security/cert/URICertStoreParameters.md) | Parameters used as input for`CertStore`algorithms which use information contained in a URI to retrieve certificates and CRLs. |
| --- | --- |
| [X509Certificate](../java/security/cert/X509Certificate.md) | Abstract class for X. |
| [X509CertSelector](../java/security/cert/X509CertSelector.md) | A`CertSelector`that selects`X509Certificates`that match all specified criteria. |
| [X509CRL](../java/security/cert/X509CRL.md) | Abstract class for an X. |
| --- | --- |
| [X509CRLEntry](../java/security/cert/X509CRLEntry.md) | Abstract class for a revoked certificate in a CRL (Certificate Revocation List). |
| [X509CRLSelector](../java/security/cert/X509CRLSelector.md) | A`CRLSelector`that selects`X509CRLs`that match all specified criteria. |

## Exceptions

| [CertificateEncodingException](../java/security/cert/CertificateEncodingException.md) | Certificate Encoding Exception. |
| --- | --- |
| [CertificateException](../java/security/cert/CertificateException.md) | This exception indicates one of a variety of certificate problems. |
| [CertificateExpiredException](../java/security/cert/CertificateExpiredException.md) | Certificate Expired Exception. |
| [CertificateNotYetValidException](../java/security/cert/CertificateNotYetValidException.md) | Certificate is not yet valid exception. |
| --- | --- |
| [CertificateParsingException](../java/security/cert/CertificateParsingException.md) | Certificate Parsing Exception. |
| [CertificateRevokedException](../java/security/cert/CertificateRevokedException.md) | An exception that indicates an X. |
| [CertPathBuilderException](../java/security/cert/CertPathBuilderException.md) | An exception indicating one of a variety of problems encountered when building a certification path with a`CertPathBuilder`. |
| --- | --- |
| [CertPathValidatorException](../java/security/cert/CertPathValidatorException.md) | An exception indicating one of a variety of problems encountered when validating a certification path. |
| [CertStoreException](../java/security/cert/CertStoreException.md) | An exception indicating one of a variety of problems retrieving certificates and CRLs from a`CertStore`. |
| [CRLException](../java/security/cert/CRLException.md) | CRL (Certificate Revocation List) Exception. |
| --- | --- |

## Enums

| [CRLReason](../java/security/cert/CRLReason.md) | The CRLReason enumeration specifies the reason that a certificate is revoked, as defined in [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280). |
| --- | --- |
| [PKIXReason](../java/security/cert/PKIXReason.md) | The`PKIXReason`enumerates the potential PKIX-specific reasons that an X. |
