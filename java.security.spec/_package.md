# java.security.spec

# java.security.spec

## Interfaces

| [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec) | A (transparent) specification of cryptographic parameters. |
| [ECField](https://developer.android.com/reference/kotlin/java/security/spec/ECField) | This interface represents an elliptic curve (EC) finite field. |
| [KeySpec](https://developer.android.com/reference/kotlin/java/security/spec/KeySpec) | A (transparent) specification of the key material that constitutes a cryptographic key. |

## Classes

| [DSAGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAGenParameterSpec) | This immutable class specifies the set of parameters used for generating DSA parameters as specified in [FIPS 186-3 Digital Signature Standard (DSS)](http://csrc.nist.gov/publications/fips/fips186-3/fips_186-3.pdf). |
| [DSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAParameterSpec) | This class specifies the set of parameters used with the DSA algorithm. |
| [DSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPrivateKeySpec) | This class specifies a DSA private key with its associated parameters. |
| [DSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/DSAPublicKeySpec) | This class specifies a DSA public key with its associated parameters. |
| [ECFieldF2m](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldF2m) | This immutable class defines an elliptic curve (EC) characteristic 2 finite field. |
| [ECFieldFp](https://developer.android.com/reference/kotlin/java/security/spec/ECFieldFp) | This immutable class defines an elliptic curve (EC) prime finite field. |
| [ECGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECGenParameterSpec) | This immutable class specifies the set of parameters used for generating elliptic curve (EC) domain parameters. |
| [ECParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/ECParameterSpec) | This immutable class specifies the set of domain parameters used with elliptic curve cryptography (ECC). |
| [ECPoint](https://developer.android.com/reference/kotlin/java/security/spec/ECPoint) | This immutable class represents a point on an elliptic curve (EC) in affine coordinates. |
| [ECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPrivateKeySpec) | This immutable class specifies an elliptic curve private key with its associated parameters. |
| [ECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/ECPublicKeySpec) | This immutable class specifies an elliptic curve public key with its associated parameters. |
| [EdDSAParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/EdDSAParameterSpec) | A class used to specify EdDSA signature and verification parameters. |
| [EdECPoint](https://developer.android.com/reference/kotlin/java/security/spec/EdECPoint) | An elliptic curve point used to specify keys as defined by [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032). |
| [EdECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPrivateKeySpec) | A class representing elliptic curve private keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. |
| [EdECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EdECPublicKeySpec) | A class representing elliptic curve public keys as defined in [RFC 8032: Edwards-Curve Digital Signature Algorithm (EdDSA)](https://tools.ietf.org/html/rfc8032), including the curve and other algorithm parameters. |
| [EllipticCurve](https://developer.android.com/reference/kotlin/java/security/spec/EllipticCurve) | This immutable class holds the necessary values needed to represent an elliptic curve. |
| [EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EncodedKeySpec) | This class represents a public or private key in encoded format. |
| [MGF1ParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/MGF1ParameterSpec) | This class specifies the set of parameters used with mask generation function MGF1 in OAEP Padding and RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [NamedParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/NamedParameterSpec) | This class is used to specify any algorithm parameters that are determined by a standard name. |
| [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec) | This class represents the ASN. |
| [PSSParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/PSSParameterSpec) | This class specifies a parameter spec for RSASSA-PSS signature scheme, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [RSAKeyGenParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAKeyGenParameterSpec) | This class specifies the set of parameters used to generate an RSA key pair. |
| [RSAMultiPrimePrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAMultiPrimePrivateCrtKeySpec) | This class specifies an RSA multi-prime private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard using the Chinese Remainder Theorem (CRT) information values for efficiency. |
| [RSAOtherPrimeInfo](https://developer.android.com/reference/kotlin/java/security/spec/RSAOtherPrimeInfo) | This class represents the triplet (prime, exponent, and coefficient) inside RSA's OtherPrimeInfo structure, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard. |
| [RSAPrivateCrtKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateCrtKeySpec) | This class specifies an RSA private key, as defined in the [PKCS#1 v2.2](https://tools.ietf.org/rfc/rfc8017.txt) standard, using the Chinese Remainder Theorem (CRT) information values for efficiency. |
| [RSAPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPrivateKeySpec) | This class specifies an RSA private key. |
| [RSAPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/RSAPublicKeySpec) | This class specifies an RSA public key. |
| [X509EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec) | This class represents the ASN. |
| [XECPrivateKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/XECPrivateKeySpec) | A class representing elliptic curve private keys as defined in RFC 7748, including the curve and other algorithm parameters. |
| [XECPublicKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/XECPublicKeySpec) | A class representing elliptic curve public keys as defined in RFC 7748, including the curve and other algorithm parameters. |

## Exceptions

| [InvalidKeySpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidKeySpecException) | This is the exception for invalid key specifications. |
| [InvalidParameterSpecException](https://developer.android.com/reference/kotlin/java/security/spec/InvalidParameterSpecException) | This is the exception for invalid parameter specifications. |
