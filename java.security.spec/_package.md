# java.security.spec

# java.security.spec

## Interfaces

| [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md) | A (transparent) specification of cryptographic parameters. |
| --- | --- |
| [ECField](../java/security/spec/ECField.md) | This interface represents an elliptic curve (EC) finite field. |
| [KeySpec](../java/security/spec/KeySpec.md) | A (transparent) specification of the key material that constitutes a cryptographic key. |

## Classes

| [DSAGenParameterSpec](../java/security/spec/DSAGenParameterSpec.md) | This immutable class specifies the set of parameters used for generating DSA parameters as specified in [FIPS 186-3 Digital Signature Standard (DSS)](http://csrc.nist.gov/publications/fips/fips186-3/fips_186-3.pdf). |
| --- | --- |
| [DSAParameterSpec](../java/security/spec/DSAParameterSpec.md) | This class specifies the set of parameters used with the DSA algorithm. |
| [DSAPrivateKeySpec](../java/security/spec/DSAPrivateKeySpec.md) | This class specifies a DSA private key with its associated parameters. |
| [DSAPublicKeySpec](../java/security/spec/DSAPublicKeySpec.md) | This class specifies a DSA public key with its associated parameters. |
| --- | --- |
| [ECFieldF2m](../java/security/spec/ECFieldF2m.md) | This immutable class defines an elliptic curve (EC) characteristic 2 finite field. |
| [ECFieldFp](../java/security/spec/ECFieldFp.md) | This immutable class defines an elliptic curve (EC) prime finite field. |
| [ECGenParameterSpec](../java/security/spec/ECGenParameterSpec.md) | This immutable class specifies the set of parameters used for generating elliptic curve (EC) domain parameters. |
| --- | --- |
| [ECParameterSpec](../java/security/spec/ECParameterSpec.md) | This immutable class specifies the set of domain parameters used with elliptic curve cryptography (ECC). |
| [ECPoint](../java/security/spec/ECPoint.md) | This immutable class represents a point on an elliptic curve (EC) in affine coordinates. |
| [ECPrivateKeySpec](../java/security/spec/ECPrivateKeySpec.md) | This immutable class specifies an elliptic curve private key with its associated parameters. |
| --- | --- |
| [ECPublicKeySpec](../java/security/spec/ECPublicKeySpec.md) | This immutable class specifies an elliptic curve public key with its associated parameters. |
| [EdDSAParameterSpec](../java/security/spec/EdDSAParameterSpec.md) | A class used to specify EdDSA signature and verification parameters. |
| [EdECPoint](../java/security/spec/EdECPoint.md) | An elliptic curve point used to specify keys as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). |
| --- | --- |
| [EdECPrivateKeySpec](../java/security/spec/EdECPrivateKeySpec.md) | A class representing elliptic curve private keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. |
| [EdECPublicKeySpec](../java/security/spec/EdECPublicKeySpec.md) | A class representing elliptic curve public keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. |
| [EllipticCurve](../java/security/spec/EllipticCurve.md) | This immutable class holds the necessary values needed to represent an elliptic curve. |
| --- | --- |
| [EncodedKeySpec](../java/security/spec/EncodedKeySpec.md) | This class represents a public or private key in encoded format. |
| [MGF1ParameterSpec](../java/security/spec/MGF1ParameterSpec.md) | This class specifies the set of parameters used with mask generation function MGF1 in OAEP Padding and RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [NamedParameterSpec](../java/security/spec/NamedParameterSpec.md) | This class is used to specify any algorithm parameters that are determined by a standard name. |
| --- | --- |
| [PKCS8EncodedKeySpec](../java/security/spec/PKCS8EncodedKeySpec.md) | This class represents the ASN. |
| [PSSParameterSpec](../java/security/spec/PSSParameterSpec.md) | This class specifies a parameter spec for RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [RSAKeyGenParameterSpec](../java/security/spec/RSAKeyGenParameterSpec.md) | This class specifies the set of parameters used to generate an RSA key pair. |
| --- | --- |
| [RSAMultiPrimePrivateCrtKeySpec](../java/security/spec/RSAMultiPrimePrivateCrtKeySpec.md) | This class specifies an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard using the Chinese Remainder Theorem (CRT) information values for efficiency. |
| [RSAOtherPrimeInfo](../java/security/spec/RSAOtherPrimeInfo.md) | This class represents the triplet (prime, exponent, and coefficient) inside RSA's OtherPrimeInfo structure, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [RSAPrivateCrtKeySpec](../java/security/spec/RSAPrivateCrtKeySpec.md) | This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency. |
| --- | --- |
| [RSAPrivateKeySpec](../java/security/spec/RSAPrivateKeySpec.md) | This class specifies an RSA private key. |
| [RSAPublicKeySpec](../java/security/spec/RSAPublicKeySpec.md) | This class specifies an RSA public key. |
| [X509EncodedKeySpec](../java/security/spec/X509EncodedKeySpec.md) | This class represents the ASN. |
| --- | --- |
| [XECPrivateKeySpec](../java/security/spec/XECPrivateKeySpec.md) | A class representing elliptic curve private keys as defined in RFC 7748, including the curve and other algorithm parameters. |
| [XECPublicKeySpec](../java/security/spec/XECPublicKeySpec.md) | A class representing elliptic curve public keys as defined in RFC 7748, including the curve and other algorithm parameters. |

## Exceptions

| [InvalidKeySpecException](../java/security/spec/InvalidKeySpecException.md) | This is the exception for invalid key specifications. |
| --- | --- |
| [InvalidParameterSpecException](../java/security/spec/InvalidParameterSpecException.md) | This is the exception for invalid parameter specifications. |
