Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509CertSelector

```
open class X509CertSelector : CertSelector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.X509CertSelector](X509CertSelector.md) |

A `CertSelector` that selects `X509Certificates` that match all specified criteria. This class is particularly useful when selecting certificates from a `CertStore` to build a PKIX-compliant certification path.

When first constructed, an `X509CertSelector` has no criteria enabled and each of the `get` methods return a default value (`null`, or `-1` for the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getBasicConstraints()` method). Therefore, the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#match(java.security.cert.Certificate)` method would return `true` for any `X509Certificate`. Typically, several criteria are enabled (by calling #setIssuer or `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setKeyUsage(kotlin.BooleanArray)`, for instance) and then the `X509CertSelector` is passed to `https://developer.android.com/reference/kotlin/java/security/cert/CertStore#getCertificates(java.security.cert.CertSelector)` or some similar method.

Several criteria can be enabled (by calling #setIssuer and `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSerialNumber(java.math.BigInteger)`, for example) such that the `match` method usually uniquely matches a single `X509Certificate`. We say usually, since it is possible for two issuing CAs to have the same distinguished name and each issue a certificate with the same serial number. Other unique combinations include the issuer, subject, subjectKeyIdentifier and/or the subjectPublicKey criteria.

Please refer to [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280) for definitions of the X.509 certificate extensions mentioned below.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#X509CertSelector()()` Creates an `X509CertSelector`. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.ByteArray)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Adds a name to the pathToNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adds a name to the pathToNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Adds a name to the subjectAlternativeNames criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.String)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adds a name to the subjectAlternativeNames criterion. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#clone()()` Returns a copy of this object. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getAuthorityKeyIdentifier()()` Returns the authorityKeyIdentifier criterion. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getBasicConstraints()()` Returns the basic constraints constraint. |
| open [X509Certificate](X509Certificate.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getCertificate()()` Returns the certificateEquals criterion. |
| open [Date](../java.util/Date.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getCertificateValid()()` Returns the certificateValid criterion. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getExtendedKeyUsage()()` Returns the extendedKeyUsage criterion. |
| open [X500Principal](../javax.security.auth.x500/X500Principal.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getIssuer()()` Returns the issuer criterion as an `X500Principal`. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getIssuerAsBytes()()` Returns the issuer criterion as a byte array. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getIssuerAsString()()` **Denigrated** , use [getIssuer()](X509CertSelector.md)) or [getIssuerAsBytes()](X509CertSelector.md)) instead. |
| open [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getKeyUsage()()` Returns the keyUsage criterion. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getMatchAllSubjectAltNames()()` Indicates if the `X509Certificate` must contain all or at least one of the subjectAlternativeNames specified in the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)` or #addSubjectAlternativeName methods. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getNameConstraints()()` Returns the name constraints criterion. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPathToNames()()` Returns a copy of the pathToNames criterion. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPolicy()()` Returns the policy criterion. |
| --- | --- |
| open [Date](../java.util/Date.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPrivateKeyValid()()` Returns the privateKeyValid criterion. |
| open [BigInteger](../java.math/BigInteger.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSerialNumber()()` Returns the serialNumber criterion. |
| open [X500Principal](../javax.security.auth.x500/X500Principal.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubject()()` Returns the subject criterion as an `X500Principal`. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectAlternativeNames()()` Returns a copy of the subjectAlternativeNames criterion. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectAsBytes()()` Returns the subject criterion as a byte array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectAsString()()` **Denigrated** , use [getSubject()](X509CertSelector.md)) or [getSubjectAsBytes()](X509CertSelector.md)) instead. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectKeyIdentifier()()` Returns the subjectKeyIdentifier criterion. |
| open [PublicKey](../java.security/PublicKey.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectPublicKey()()` Returns the subjectPublicKey criterion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectPublicKeyAlgID()()` Returns the subjectPublicKeyAlgID criterion. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#match(java.security.cert.Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!)` Decides whether a `Certificate` should be selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setAuthorityKeyIdentifier(kotlin.ByteArray)(authorityKeyID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the authorityKeyIdentifier criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setBasicConstraints(kotlin.Int)(minMaxPathLen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the basic constraints constraint. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setCertificate(java.security.cert.X509Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!)` Sets the certificateEquals criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setCertificateValid(java.util.Date)(certValid: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Sets the certificateValid criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setExtendedKeyUsage(kotlin.collections.MutableSet)(keyPurposeSet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the extendedKeyUsage criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.ByteArray)(issuerDN: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the issuer criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.String)(issuerDN: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Denigrated** , use [setIssuer(X500Principal)](X509CertSelector.md)) or [setIssuer(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.ByteArray)) instead. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(javax.security.auth.x500.X500Principal)(issuer: https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!)` Sets the issuer criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setKeyUsage(kotlin.BooleanArray)(keyUsage: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!)` Sets the keyUsage criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setMatchAllSubjectAltNames(kotlin.Boolean)(matchAllNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables/disables matching all of the subjectAlternativeNames specified in the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)` or #addSubjectAlternativeName methods. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setNameConstraints(kotlin.ByteArray)(bytes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the name constraints criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPathToNames(kotlin.collections.MutableCollection)(names: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!)` Sets the pathToNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPolicy(kotlin.collections.MutableSet)(certPolicySet: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the policy constraint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPrivateKeyValid(java.util.Date)(privateKeyValid: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Sets the privateKeyValid criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSerialNumber(java.math.BigInteger)(serial: https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!)` Sets the serialNumber criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(kotlin.ByteArray)(subjectDN: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the subject criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(kotlin.String)(subjectDN: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` **Denigrated** , use [setSubject(X500Principal)](X509CertSelector.md)) or [setSubject(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(kotlin.ByteArray)) instead. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(javax.security.auth.x500.X500Principal)(subject: https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!)` Sets the subject criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)(names: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!)` Sets the subjectAlternativeNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectKeyIdentifier(kotlin.ByteArray)(subjectKeyID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the subjectKeyIdentifier criterion. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectPublicKey(kotlin.ByteArray)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Sets the subjectPublicKey criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectPublicKey(java.security.PublicKey)(key: https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!)` Sets the subjectPublicKey criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectPublicKeyAlgID(kotlin.String)(oid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the subjectPublicKeyAlgID criterion. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#toString()()` Return a printable representation of the `CertSelector`. |

## Public constructors

### X509CertSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
X509CertSelector()
```

Creates an `X509CertSelector`. Initially, no criteria are set so any `X509Certificate` will match.

## Public methods

### addPathToName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPathToName(
    type: Int, 
    name: ByteArray!
): Unit
```

Adds a name to the pathToNames criterion. The `X509Certificate` must not include name constraints that would prohibit building a path to the specified name.

This method allows the caller to add a name to the set of names which the `X509Certificates`'s name constraints must permit. The specified name is added to any previous value for the pathToNames criterion. If the name is a duplicate, it may be ignored.

The name is provided as a byte array. This byte array should contain the DER encoded name, as it would appear in the GeneralName structure defined in RFC 5280 and X.509. The ASN.1 definition of this structure appears in the documentation for `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)`.

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the name type (0-8, as specified in RFC 5280, section 4.2.1.6) |
| `name` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the name in ASN.1 DER encoded form |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

### addPathToName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addPathToName(
    type: Int, 
    name: String!
): Unit
```

Adds a name to the pathToNames criterion. The `X509Certificate` must not include name constraints that would prohibit building a path to the specified name.

This method allows the caller to add a name to the set of names which the `X509Certificates`'s name constraints must permit. The specified name is added to any previous value for the pathToNames criterion. If the name is a duplicate, it may be ignored.

The name is provided in string format. RFC 822, DNS, and URI names use the well-established string formats for those types (subject to the restrictions included in RFC 5280). IPv4 address names are supplied using dotted quad notation. OID address names are represented as a series of nonnegative integers separated by periods. And directory names (distinguished names) are supplied in RFC 2253 format. No standard string format is defined for otherNames, X.400 names, EDI party names, IPv6 address names, or any other type of names. They should be specified using the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.ByteArray)` method.

**Note:** for distinguished names, use [addPathToName(int,byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.ByteArray)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the name type (0-8, as specified in RFC 5280, section 4.2.1.6) |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name in string form |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

### addSubjectAlternativeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addSubjectAlternativeName(
    type: Int, 
    name: ByteArray!
): Unit
```

Adds a name to the subjectAlternativeNames criterion. The `X509Certificate` must contain all or at least one of the specified subjectAlternativeNames, depending on the value of the matchAllNames flag (see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setMatchAllSubjectAltNames(kotlin.Boolean)`).

This method allows the caller to add a name to the set of subject alternative names. The specified name is added to any previous value for the subjectAlternativeNames criterion. If the specified name is a duplicate, it may be ignored.

The name is provided as a byte array. This byte array should contain the DER encoded name, as it would appear in the GeneralName structure defined in RFC 5280 and X.509. The encoded byte array should only contain the encoded value of the name, and should not include the tag associated with the name in the GeneralName structure. The ASN.1 definition of this structure appears below.

```kotlin
<code>GeneralName ::= CHOICE {
        otherName                       [0]     OtherName,
        rfc822Name                      [1]     IA5String,
        dNSName                         [2]     IA5String,
        x400Address                     [3]     ORAddress,
        directoryName                   [4]     Name,
        ediPartyName                    [5]     EDIPartyName,
        uniformResourceIdentifier       [6]     IA5String,
        iPAddress                       [7]     OCTET STRING,
        registeredID                    [8]     OBJECT IDENTIFIER}
  </code>
```

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the name type (0-8, as listed above) |
| `name` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the name in ASN.1 DER encoded form |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

### addSubjectAlternativeName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addSubjectAlternativeName(
    type: Int, 
    name: String!
): Unit
```

Adds a name to the subjectAlternativeNames criterion. The `X509Certificate` must contain all or at least one of the specified subjectAlternativeNames, depending on the value of the matchAllNames flag (see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setMatchAllSubjectAltNames(kotlin.Boolean)`).

This method allows the caller to add a name to the set of subject alternative names. The specified name is added to any previous value for the subjectAlternativeNames criterion. If the specified name is a duplicate, it may be ignored.

The name is provided in string format. [RFC 822](http://www.ietf.org/rfc/rfc822.txt), DNS, and URI names use the well-established string formats for those types (subject to the restrictions included in RFC 5280). IPv4 address names are supplied using dotted quad notation. OID address names are represented as a series of nonnegative integers separated by periods. And directory names (distinguished names) are supplied in RFC 2253 format. No standard string format is defined for otherNames, X.400 names, EDI party names, IPv6 address names, or any other type of names. They should be specified using the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)` method.

**Note:** for distinguished names, use [addSubjectAlternativeName(int,byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the name type (0-8, as specified in RFC 5280, section 4.2.1.6) |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name in string form (not `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Returns a copy of this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | the copy |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### getAuthorityKeyIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAuthorityKeyIdentifier(): ByteArray!
```

Returns the authorityKeyIdentifier criterion. The `X509Certificate` must contain a AuthorityKeyIdentifier extension with the specified value. If `null`, no authorityKeyIdentifier check will be done.

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the key identifier (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setAuthorityKeyIdentifier(kotlin.ByteArray)`

### getBasicConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBasicConstraints(): Int
```

Returns the basic constraints constraint. If the value is greater than or equal to zero, the `X509Certificates` must include a basicConstraints extension with a pathLen of at least this value. If the value is -2, only end-entity certificates are accepted. If the value is -1, no basicConstraints check is done.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the value for the basic constraints constraint |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setBasicConstraints(kotlin.Int)`

### getCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertificate(): X509Certificate!
```

Returns the certificateEquals criterion. The specified `X509Certificate` must be equal to the `X509Certificate` passed to the `match` method. If `null`, this check is not applied.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!` | the `X509Certificate` to match (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setCertificate(java.security.cert.X509Certificate)`

### getCertificateValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertificateValid(): Date!
```

Returns the certificateValid criterion. The specified date must fall within the certificate validity period for the `X509Certificate`. If `null`, no certificateValid check will be done.

Note that the `Date` returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the `Date` to check (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setCertificateValid(java.util.Date)`

### getExtendedKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExtendedKeyUsage(): MutableSet<String!>!
```

Returns the extendedKeyUsage criterion. The `X509Certificate` must allow the specified key purposes in its extended key usage extension. If the `keyPurposeSet` returned is empty or `null`, no extendedKeyUsage check will be done. Note that an `X509Certificate` that has no extendedKeyUsage extension implicitly allows all key purposes.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an immutable `Set` of key purpose OIDs in string format (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setExtendedKeyUsage(kotlin.collections.MutableSet)`

### getIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuer(): X500Principal!
```

Returns the issuer criterion as an `X500Principal`. This distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null`, the issuer criterion is disabled and any issuer distinguished name will do.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!` | the required issuer distinguished name as X500Principal (or `null`) |

### getIssuerAsBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerAsBytes(): ByteArray!
```

Returns the issuer criterion as a byte array. This distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null`, the issuer criterion is disabled and any issuer distinguished name will do.

If the value returned is not `null`, it is a byte array containing a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is supplied in the documentation for `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.ByteArray)`.

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | a byte array containing the required issuer distinguished name in ASN.1 DER format (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an encoding error occurs |

### getIssuerAsString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIssuerAsString(): String!
```

**Denigrated** , use [getIssuer()](X509CertSelector.md)) or [getIssuerAsBytes()](X509CertSelector.md)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

Returns the issuer criterion as a `String`. This distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null`, the issuer criterion is disabled and any issuer distinguished name will do.

If the value returned is not `null`, it is a distinguished name, in RFC 2253 format.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the required issuer distinguished name in RFC 2253 format (or `null`) |

### getKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getKeyUsage(): BooleanArray!
```

Returns the keyUsage criterion. The `X509Certificate` must allow the specified keyUsage values. If null, no keyUsage check will be done.

Note that the boolean array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html!` | a boolean array in the same format as the boolean array returned by `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getKeyUsage()`. Or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setKeyUsage(kotlin.BooleanArray)`

### getMatchAllSubjectAltNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMatchAllSubjectAltNames(): Boolean
```

Indicates if the `X509Certificate` must contain all or at least one of the subjectAlternativeNames specified in the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)` or #addSubjectAlternativeName methods. If `true`, the `X509Certificate` must contain all of the specified subject alternative names. If `false`, the `X509Certificate` must contain at least one of the specified subject alternative names.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the flag is enabled; `false` if the flag is disabled. The flag is `true` by default. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setMatchAllSubjectAltNames(kotlin.Boolean)`

### getNameConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNameConstraints(): ByteArray!
```

Returns the name constraints criterion. The `X509Certificate` must have subject and subject alternative names that meet the specified name constraints.

The name constraints are returned as a byte array. This byte array contains the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in RFC 5280 and X.509. The ASN.1 notation for this structure is supplied in the documentation for `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setNameConstraints(kotlin.ByteArray)`.

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | a byte array containing the ASN.1 DER encoding of a NameConstraints extension used for checking name constraints. `null` if no name constraints check will be performed. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setNameConstraints(kotlin.ByteArray)`

### getPathToNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPathToNames(): MutableCollection<MutableList<*>!>!
```

Returns a copy of the pathToNames criterion. The `X509Certificate` must not include name constraints that would prohibit building a path to the specified names. If the value returned is `null`, no pathToNames check will be performed.

If the value returned is not `null`, it is a `Collection` with one entry for each name to be included in the pathToNames criterion. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively). There can be multiple names of the same type. Note that the `Collection` returned may contain duplicate names (same name and name type).

Each name in the `Collection` may be specified either as a `String` or as an ASN.1 encoded byte array. For more details about the formats used, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.ByteArray)`.

Note that a deep copy is performed on the `Collection` to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!` | a `Collection` of names (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPathToNames(kotlin.collections.MutableCollection)`

### getPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPolicy(): MutableSet<String!>!
```

Returns the policy criterion. The `X509Certificate` must include at least one of the specified policies in its certificate policies extension. If the `Set` returned is empty, then the `X509Certificate` must include at least some specified policy in its certificate policies extension. If the `Set` returned is `null`, no policy check will be performed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an immutable `Set` of certificate policy OIDs in string format (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPolicy(kotlin.collections.MutableSet)`

### getPrivateKeyValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPrivateKeyValid(): Date!
```

Returns the privateKeyValid criterion. The specified date must fall within the private key validity period for the `X509Certificate`. If `null`, no privateKeyValid check will be done.

Note that the `Date` returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the `Date` to check (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setPrivateKeyValid(java.util.Date)`

### getSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSerialNumber(): BigInteger!
```

Returns the serialNumber criterion. The specified serial number must match the certificate serial number in the `X509Certificate`. If `null`, any certificate serial number will do.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/math/BigInteger.html#!` | the certificate serial number to match (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSerialNumber(java.math.BigInteger)`

### getSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubject(): X500Principal!
```

Returns the subject criterion as an `X500Principal`. This distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, the subject criterion is disabled and any subject distinguished name will do.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#!` | the required subject distinguished name as X500Principal (or `null`) |

### getSubjectAlternativeNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectAlternativeNames(): MutableCollection<MutableList<*>!>!
```

Returns a copy of the subjectAlternativeNames criterion. The `X509Certificate` must contain all or at least one of the specified subjectAlternativeNames, depending on the value of the matchAllNames flag (see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getMatchAllSubjectAltNames()`). If the value returned is `null`, no subjectAlternativeNames check will be performed.

If the value returned is not `null`, it is a `Collection` with one entry for each name to be included in the subject alternative name criterion. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively). There can be multiple names of the same type. Note that the `Collection` returned may contain duplicate names (same name and name type).

Each subject alternative name in the `Collection` may be specified either as a `String` or as an ASN.1 encoded byte array. For more details about the formats used, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)`.

Note that a deep copy is performed on the `Collection` to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<*>!>!` | a `Collection` of names (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)`

### getSubjectAsBytes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectAsBytes(): ByteArray!
```

Returns the subject criterion as a byte array. This distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, the subject criterion is disabled and any subject distinguished name will do.

If the value returned is not `null`, it is a byte array containing a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is supplied in the documentation for `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(kotlin.ByteArray)`.

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | a byte array containing the required subject distinguished name in ASN.1 DER format (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an encoding error occurs |

### getSubjectAsString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectAsString(): String!
```

**Denigrated** , use [getSubject()](X509CertSelector.md)) or [getSubjectAsBytes()](X509CertSelector.md)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

Returns the subject criterion as a `String`. This distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, the subject criterion is disabled and any subject distinguished name will do.

If the value returned is not `null`, it is a distinguished name, in RFC 2253 format.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the required subject distinguished name in RFC 2253 format (or `null`) |

### getSubjectKeyIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectKeyIdentifier(): ByteArray!
```

Returns the subjectKeyIdentifier criterion. The `X509Certificate` must contain a SubjectKeyIdentifier extension with the specified value. If `null`, no subjectKeyIdentifier check will be done.

Note that the byte array returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!` | the key identifier (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectKeyIdentifier(kotlin.ByteArray)`

### getSubjectPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectPublicKey(): PublicKey!
```

Returns the subjectPublicKey criterion. The `X509Certificate` must contain the specified subject public key. If `null`, no subjectPublicKey check will be done.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/PublicKey.html#!` | the subject public key to check for (or `null`) |

**See Also**

### getSubjectPublicKeyAlgID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSubjectPublicKeyAlgID(): String!
```

Returns the subjectPublicKeyAlgID criterion. The `X509Certificate` must contain a subject public key with the specified algorithm. If `null`, no subjectPublicKeyAlgID check will be done.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the object identifier (OID) of the signature algorithm to check for (or `null`). An OID is represented by a set of nonnegative integers separated by periods. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectPublicKeyAlgID(kotlin.String)`

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun match(cert: Certificate!): Boolean
```

Decides whether a `Certificate` should be selected.

| Parameters ||
|---|---|
| `cert` | [Certificate](Certificate.md)!: the `Certificate` to be checked |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the `Certificate` should be selected, `false` otherwise |

### setAuthorityKeyIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAuthorityKeyIdentifier(authorityKeyID: ByteArray!): Unit
```

Sets the authorityKeyIdentifier criterion. The `X509Certificate` must contain an AuthorityKeyIdentifier extension for which the contents of the extension value matches the specified criterion value. If the criterion value is `null`, no authorityKeyIdentifier check will be done.

If `authorityKeyID` is not `null`, it should contain a single DER encoded value corresponding to the contents of the extension value (not including the object identifier, criticality setting, and encapsulating OCTET STRING) for an AuthorityKeyIdentifier extension. The ASN.1 notation for this structure follows.

```kotlin
<code>AuthorityKeyIdentifier ::= SEQUENCE {
     keyIdentifier             [0] KeyIdentifier           OPTIONAL,
     authorityCertIssuer       [1] GeneralNames            OPTIONAL,
     authorityCertSerialNumber [2] CertificateSerialNumber OPTIONAL  }
 
  KeyIdentifier ::= OCTET STRING
  </code>
```

Authority key identifiers are not parsed by the `X509CertSelector`. Instead, the values are compared using a byte-by-byte comparison.

When the `keyIdentifier` field of `AuthorityKeyIdentifier` is populated, the value is usually taken from the `SubjectKeyIdentifier` extension in the issuer's certificate. Note, however, that the result of `X509Certificate.getExtensionValue(<SubjectKeyIdentifier Object Identifier>)` on the issuer's certificate may NOT be used directly as the input to `setAuthorityKeyIdentifier`. This is because the SubjectKeyIdentifier contains only a KeyIdentifier OCTET STRING, and not a SEQUENCE of KeyIdentifier, GeneralNames, and CertificateSerialNumber. In order to use the extension value of the issuer certificate's `SubjectKeyIdentifier` extension, it will be necessary to extract the value of the embedded `KeyIdentifier` OCTET STRING, then DER encode this OCTET STRING inside a SEQUENCE. For more details on SubjectKeyIdentifier, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectKeyIdentifier(kotlin.ByteArray)`.

Note also that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `authorityKeyID` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the authority key identifier (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getAuthorityKeyIdentifier()`

### setBasicConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBasicConstraints(minMaxPathLen: Int): Unit
```

Sets the basic constraints constraint. If the value is greater than or equal to zero, `X509Certificates` must include a basicConstraints extension with a pathLen of at least this value. If the value is -2, only end-entity certificates are accepted. If the value is -1, no check is done.

This constraint is useful when building a certification path forward (from the target toward the trust anchor. If a partial path has been built, any candidate certificate must have a maxPathLen value greater than or equal to the number of certificates in the partial path.

| Parameters ||
|---|---|
| `minMaxPathLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the value for the basic constraints constraint |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the value is less than -2 |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getBasicConstraints()`

### setCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCertificate(cert: X509Certificate!): Unit
```

Sets the certificateEquals criterion. The specified `X509Certificate` must be equal to the `X509Certificate` passed to the `match` method. If `null`, then this check is not applied.

This method is particularly useful when it is necessary to match a single certificate. Although other criteria can be specified in conjunction with the certificateEquals criterion, it is usually not practical or necessary.

| Parameters ||
|---|---|
| `cert` | [X509Certificate](X509Certificate.md)!: the `X509Certificate` to match (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getCertificate()`

### setCertificateValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCertificateValid(certValid: Date!): Unit
```

Sets the certificateValid criterion. The specified date must fall within the certificate validity period for the `X509Certificate`. If `null`, no certificateValid check will be done.

Note that the `Date` supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `certValid` | [Date](../java.util/Date.md)!: the `Date` to check (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getCertificateValid()`

### setExtendedKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtendedKeyUsage(keyPurposeSet: MutableSet<String!>!): Unit
```

Sets the extendedKeyUsage criterion. The `X509Certificate` must allow the specified key purposes in its extended key usage extension. If `keyPurposeSet` is empty or `null`, no extendedKeyUsage check will be done. Note that an `X509Certificate` that has no extendedKeyUsage extension implicitly allows all key purposes.

Note that the `Set` is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `keyPurposeSet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: a `Set` of key purpose OIDs in string format (or `null`). Each OID is represented by a set of nonnegative integers separated by periods. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the OID is invalid, such as the first component being not 0, 1 or 2 or the second component being greater than 39. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getExtendedKeyUsage()`

### setIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIssuer(issuerDN: ByteArray!): Unit
```

Sets the issuer criterion. The specified distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null` is specified, the issuer criterion is disabled and any issuer distinguished name will do.

If `issuerDN` is not `null`, it should contain a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is as follows.

```kotlin
<code>Name ::= CHOICE {
    RDNSequence }
 
  RDNSequence ::= SEQUENCE OF RelativeDistinguishedName
 
  RelativeDistinguishedName ::=
    SET SIZE (1 .. MAX) OF AttributeTypeAndValue
 
  AttributeTypeAndValue ::= SEQUENCE {
    type     AttributeType,
    value    AttributeValue }
 
  AttributeType ::= OBJECT IDENTIFIER
 
  AttributeValue ::= ANY DEFINED BY AttributeType
  ....
  DirectoryString ::= CHOICE {
        teletexString           TeletexString (SIZE (1..MAX)),
        printableString         PrintableString (SIZE (1..MAX)),
        universalString         UniversalString (SIZE (1..MAX)),
        utf8String              UTF8String (SIZE (1.. MAX)),
        bmpString               BMPString (SIZE (1..MAX)) }
  </code>
```

Note that the byte array specified here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `issuerDN` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the distinguished name in ASN.1 DER encoded form (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an encoding error occurs (incorrect form for DN) |

### setIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIssuer(issuerDN: String!): Unit
```

**Denigrated** , use [setIssuer(X500Principal)](X509CertSelector.md)) or [setIssuer(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.ByteArray)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the [RFC 2253](http://www.ietf.org/rfc/rfc2253.txt) String form of some distinguished names.

Sets the issuer criterion. The specified distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null`, any issuer distinguished name will do.

If `issuerDN` is not `null`, it should contain a distinguished name, in RFC 2253 format.

| Parameters ||
|---|---|
| `issuerDN` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a distinguished name in RFC 2253 format (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs (incorrect form for DN) |

### setIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIssuer(issuer: X500Principal!): Unit
```

Sets the issuer criterion. The specified distinguished name must match the issuer distinguished name in the `X509Certificate`. If `null`, any issuer distinguished name will do.

| Parameters ||
|---|---|
| `issuer` | [X500Principal](../javax.security.auth.x500/X500Principal.md)!: a distinguished name as X500Principal (or `null`) |

### setKeyUsage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setKeyUsage(keyUsage: BooleanArray!): Unit
```

Sets the keyUsage criterion. The `X509Certificate` must allow the specified keyUsage values. If `null`, no keyUsage check will be done. Note that an `X509Certificate` that has no keyUsage extension implicitly allows all keyUsage values.

Note that the boolean array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `keyUsage` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!: a boolean array in the same format as the boolean array returned by `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate#getKeyUsage()`. Or `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getKeyUsage()`

### setMatchAllSubjectAltNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setMatchAllSubjectAltNames(matchAllNames: Boolean): Unit
```

Enables/disables matching all of the subjectAlternativeNames specified in the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubjectAlternativeNames(kotlin.collections.MutableCollection)` or #addSubjectAlternativeName methods. If enabled, the `X509Certificate` must contain all of the specified subject alternative names. If disabled, the `X509Certificate` must contain at least one of the specified subject alternative names.

The matchAllNames flag is `true` by default.

| Parameters ||
|---|---|
| `matchAllNames` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true`, the flag is enabled; if `false`, the flag is disabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getMatchAllSubjectAltNames()`

### setNameConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setNameConstraints(bytes: ByteArray!): Unit
```

Sets the name constraints criterion. The `X509Certificate` must have subject and subject alternative names that meet the specified name constraints.

The name constraints are specified as a byte array. This byte array should contain the DER encoded form of the name constraints, as they would appear in the NameConstraints structure defined in RFC 5280 and X.509. The ASN.1 definition of this structure appears below.

```kotlin
<code>NameConstraints ::= SEQUENCE {
        permittedSubtrees       [0]     GeneralSubtrees OPTIONAL,
        excludedSubtrees        [1]     GeneralSubtrees OPTIONAL }
 
   GeneralSubtrees ::= SEQUENCE SIZE (1..MAX) OF GeneralSubtree
 
   GeneralSubtree ::= SEQUENCE {
        base                    GeneralName,
        minimum         [0]     BaseDistance DEFAULT 0,
        maximum         [1]     BaseDistance OPTIONAL }
 
   BaseDistance ::= INTEGER (0..MAX)
 
   GeneralName ::= CHOICE {
        otherName                       [0]     OtherName,
        rfc822Name                      [1]     IA5String,
        dNSName                         [2]     IA5String,
        x400Address                     [3]     ORAddress,
        directoryName                   [4]     Name,
        ediPartyName                    [5]     EDIPartyName,
        uniformResourceIdentifier       [6]     IA5String,
        iPAddress                       [7]     OCTET STRING,
        registeredID                    [8]     OBJECT IDENTIFIER}
  </code>
```

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `bytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the ASN.1 DER encoding of a NameConstraints extension to be used for checking name constraints. Only the value of the extension is included, not the OID or criticality flag. Can be `null`, in which case no name constraints check will be performed. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getNameConstraints()`

### setPathToNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPathToNames(names: MutableCollection<MutableList<*>!>!): Unit
```

Sets the pathToNames criterion. The `X509Certificate` must not include name constraints that would prohibit building a path to the specified names.

This method allows the caller to specify, with a single method call, the complete set of names which the `X509Certificates`'s name constraints must permit. The specified value replaces the previous value for the pathToNames criterion.

This constraint is useful when building a certification path forward (from the target toward the trust anchor. If a partial path has been built, any candidate certificate must not include name constraints that would prohibit building a path to any of the names in the partial path.

The `names` parameter (if not `null`) is a `Collection` with one entry for each name to be included in the pathToNames criterion. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively). There can be multiple names of the same type. If `null` is supplied as the value for this argument, no pathToNames check will be performed.

Each name in the `Collection` may be specified either as a `String` or as an ASN.1 encoded byte array. For more details about the formats used, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.ByteArray)`.

**Note:** for distinguished names, specify the byte array form instead of the String form. See the note in `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addPathToName(kotlin.Int,%20kotlin.String)` for more information.

Note that the `names` parameter can contain duplicate names (same name and name type), but they may be removed from the `Collection` of names returned by the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPathToNames()` method.

Note that a deep copy is performed on the `Collection` to protect against subsequent modifications.

| Parameters ||
|---|---|
| `names` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>!: a `Collection` with one entry per name (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPathToNames()`

### setPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPolicy(certPolicySet: MutableSet<String!>!): Unit
```

Sets the policy constraint. The `X509Certificate` must include at least one of the specified policies in its certificate policies extension. If `certPolicySet` is empty, then the `X509Certificate` must include at least some specified policy in its certificate policies extension. If `certPolicySet` is `null`, no policy check will be performed.

Note that the `Set` is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `certPolicySet` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: a `Set` of certificate policy OIDs in string format (or `null`). Each OID is represented by a set of nonnegative integers separated by periods. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs on the OID such as the first component is not 0, 1 or 2 or the second component is greater than 39. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPolicy()`

### setPrivateKeyValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPrivateKeyValid(privateKeyValid: Date!): Unit
```

Sets the privateKeyValid criterion. The specified date must fall within the private key validity period for the `X509Certificate`. If `null`, no privateKeyValid check will be done.

Note that the `Date` supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `privateKeyValid` | [Date](../java.util/Date.md)!: the `Date` to check (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getPrivateKeyValid()`

### setSerialNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSerialNumber(serial: BigInteger!): Unit
```

Sets the serialNumber criterion. The specified serial number must match the certificate serial number in the `X509Certificate`. If `null`, any certificate serial number will do.

| Parameters ||
|---|---|
| `serial` | [BigInteger](../java.math/BigInteger.md)!: the certificate serial number to match (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSerialNumber()`

### setSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubject(subjectDN: ByteArray!): Unit
```

Sets the subject criterion. The specified distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, any subject distinguished name will do.

If `subjectDN` is not `null`, it should contain a single DER encoded distinguished name, as defined in X.501. For the ASN.1 notation for this structure, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setIssuer(kotlin.ByteArray)`.

| Parameters ||
|---|---|
| `subjectDN` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the distinguished name in ASN.1 DER format (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an encoding error occurs (incorrect form for DN) |

### setSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubject(subjectDN: String!): Unit
```

**Denigrated** , use [setSubject(X500Principal)](X509CertSelector.md)) or [setSubject(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setSubject(kotlin.ByteArray)) instead. This method should not be relied on as it can fail to match some certificates because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

Sets the subject criterion. The specified distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, any subject distinguished name will do.

If `subjectDN` is not `null`, it should contain a distinguished name, in RFC 2253 format.

| Parameters ||
|---|---|
| `subjectDN` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a distinguished name in RFC 2253 format (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs (incorrect form for DN) |

### setSubject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubject(subject: X500Principal!): Unit
```

Sets the subject criterion. The specified distinguished name must match the subject distinguished name in the `X509Certificate`. If `null`, any subject distinguished name will do.

| Parameters ||
|---|---|
| `subject` | [X500Principal](../javax.security.auth.x500/X500Principal.md)!: a distinguished name as X500Principal (or `null`) |

### setSubjectAlternativeNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubjectAlternativeNames(names: MutableCollection<MutableList<*>!>!): Unit
```

Sets the subjectAlternativeNames criterion. The `X509Certificate` must contain all or at least one of the specified subjectAlternativeNames, depending on the value of the matchAllNames flag (see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#setMatchAllSubjectAltNames(kotlin.Boolean)`).

This method allows the caller to specify, with a single method call, the complete set of subject alternative names for the subjectAlternativeNames criterion. The specified value replaces the previous value for the subjectAlternativeNames criterion.

The `names` parameter (if not `null`) is a `Collection` with one entry for each name to be included in the subject alternative name criterion. Each entry is a `List` whose first entry is an `Integer` (the name type, 0-8) and whose second entry is a `String` or a byte array (the name, in string or ASN.1 DER encoded form, respectively). There can be multiple names of the same type. If `null` is supplied as the value for this argument, no subjectAlternativeNames check will be performed.

Each subject alternative name in the `Collection` may be specified either as a `String` or as an ASN.1 encoded byte array. For more details about the formats used, see `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.ByteArray)`.

**Note:** for distinguished names, specify the byte array form instead of the String form. See the note in `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#addSubjectAlternativeName(kotlin.Int,%20kotlin.String)` for more information.

Note that the `names` parameter can contain duplicate names (same name and name type), but they may be removed from the `Collection` of names returned by the `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectAlternativeNames()` method.

Note that a deep copy is performed on the `Collection` to protect against subsequent modifications.

| Parameters ||
|---|---|
| `names` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<\*\>!\>!: a `Collection` of names (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if a parsing error occurs |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectAlternativeNames()`

### setSubjectKeyIdentifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubjectKeyIdentifier(subjectKeyID: ByteArray!): Unit
```

Sets the subjectKeyIdentifier criterion. The `X509Certificate` must contain a SubjectKeyIdentifier extension for which the contents of the extension matches the specified criterion value. If the criterion value is `null`, no subjectKeyIdentifier check will be done.

If `subjectKeyID` is not `null`, it should contain a single DER encoded value corresponding to the contents of the extension value (not including the object identifier, criticality setting, and encapsulating OCTET STRING) for a SubjectKeyIdentifier extension. The ASN.1 notation for this structure follows.

```kotlin
<code>SubjectKeyIdentifier ::= KeyIdentifier
 
  KeyIdentifier ::= OCTET STRING
  </code>
```

Since the format of subject key identifiers is not mandated by any standard, subject key identifiers are not parsed by the `X509CertSelector`. Instead, the values are compared using a byte-by-byte comparison.

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `subjectKeyID` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: the subject key identifier (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectKeyIdentifier()`

### setSubjectPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubjectPublicKey(key: ByteArray!): Unit
```

Sets the subjectPublicKey criterion. The `X509Certificate` must contain the specified subject public key. If `null`, no subjectPublicKey check will be done.

Because this method allows the public key to be specified as a byte array, it may be used for unknown key types.

If `key` is not `null`, it should contain a single DER encoded SubjectPublicKeyInfo structure, as defined in X.509. The ASN.1 notation for this structure is as follows.

```kotlin
<code>SubjectPublicKeyInfo  ::=  SEQUENCE  {
    algorithm            AlgorithmIdentifier,
    subjectPublicKey     BIT STRING  }
 
  AlgorithmIdentifier  ::=  SEQUENCE  {
    algorithm               OBJECT IDENTIFIER,
    parameters              ANY DEFINED BY algorithm OPTIONAL  }
                               -- contains a value of the type
                               -- registered for use with the
                               -- algorithm object identifier value
  </code>
```

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `key` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: a byte array containing the subject public key in ASN.1 DER form (or `null`) |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an encoding error occurs (incorrect form for subject public key) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectPublicKey()`

### setSubjectPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubjectPublicKey(key: PublicKey!): Unit
```

Sets the subjectPublicKey criterion. The `X509Certificate` must contain the specified subject public key. If `null`, no subjectPublicKey check will be done.

| Parameters ||
|---|---|
| `key` | [PublicKey](../java.security/PublicKey.md)!: the subject public key to check for (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectPublicKey()`

### setSubjectPublicKeyAlgID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSubjectPublicKeyAlgID(oid: String!): Unit
```

Sets the subjectPublicKeyAlgID criterion. The `X509Certificate` must contain a subject public key with the specified algorithm. If `null`, no subjectPublicKeyAlgID check will be done.

| Parameters ||
|---|---|
| `oid` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The object identifier (OID) of the algorithm to check for (or `null`). An OID is represented by a set of nonnegative integers separated by periods. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if the OID is invalid, such as the first component being not 0, 1 or 2 or the second component being greater than 39. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/X509CertSelector#getSubjectPublicKeyAlgID()`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Return a printable representation of the `CertSelector`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a `String` describing the contents of the `CertSelector` |
