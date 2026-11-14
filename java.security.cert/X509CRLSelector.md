# X509CRLSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509CRLSelector

```
open class X509CRLSelector : CRLSelector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.X509CRLSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#) |

A`CRLSelector`that selects`X509CRLs`that match all specified criteria. This class is particularly useful when selecting CRLs from a`CertStore`to check revocation status of a particular certificate.

When first constructed, an`X509CRLSelector`has no criteria enabled and each of the`get`methods return a default value (`null`). Therefore, the [match](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#match(java.security.cert.CRL))method would return`true`for any`X509CRL`. Typically, several criteria are enabled (by calling [setIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuers(kotlin.collections.MutableCollection))or [setDateAndTime](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setDateAndTime(java.util.Date)), for instance) and then the`X509CRLSelector`is passed to [CertStore.getCRLs](https://developer.android.com/reference/kotlin/java/security/cert/CertStore#getCRLs(java.security.cert.CRLSelector))or some similar method.

Please refer to [RFC 5280: Internet X.509 Public Key Infrastructure Certificate and CRL Profile](http://tools.ietf.org/html/rfc5280) for definitions of the X.509 CRL fields and extensions mentioned below.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509CRLSelector](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#X509CRLSelector())`()` Creates an`X509CRLSelector`. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIssuer](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuer(javax.security.auth.x500.X500Principal))`(`issuer:` ` [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!`)` Adds a name to the issuerNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIssuerName](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuerName(kotlin.ByteArray))`(`name:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Adds a name to the issuerNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIssuerName](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuerName(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` **Denigrated** , use [addIssuer(javax.security.auth.x500.X500Principal)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuer(javax.security.auth.x500.X500Principal))or[addIssuerName(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuerName(kotlin.ByteArray))instead. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#clone())`()` Returns a copy of this object. |
| open [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)! | [getCertificateChecking](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getCertificateChecking())`()` Returns the certificate being checked. |
| open [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | [getDateAndTime](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getDateAndTime())`()` Returns the dateAndTime criterion. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getIssuerNames](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuerNames())`()` Returns a copy of the issuerNames criterion. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!\>! | [getIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuers())`()` Returns the issuerNames criterion. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getMaxCRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getMaxCRL())`()` Returns the maxCRLNumber criterion. |
| open [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | [getMinCRL](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getMinCRL())`()` Returns the minCRLNumber criterion. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [match](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#match(java.security.cert.CRL))`(`crl:` ` [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)!`)` Decides whether a`CRL`should be selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertificateChecking](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setCertificateChecking(java.security.cert.X509Certificate))`(`cert:` ` [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)!`)` Sets the certificate being checked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDateAndTime](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setDateAndTime(java.util.Date))`(`dateAndTime:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Sets the dateAndTime criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIssuerNames](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuerNames(kotlin.collections.MutableCollection))`(`names:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<*>!`)` **Note:** use [setIssuers(java.util.Collection)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuers(kotlin.collections.MutableCollection))instead or only specify the byte array form of distinguished names when using this method. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuers(kotlin.collections.MutableCollection))`(`issuers:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!>!`)` Sets the issuerNames criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxCRLNumber](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setMaxCRLNumber(java.math.BigInteger))`(`maxCRL:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Sets the maxCRLNumber criterion. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMinCRLNumber](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setMinCRLNumber(java.math.BigInteger))`(`minCRL:` ` [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!`)` Sets the minCRLNumber criterion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#toString())`()` Returns a printable representation of the`X509CRLSelector`. |

## Public constructors

### X509CRLSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509CRLSelector()
```

Creates an`X509CRLSelector`. Initially, no criteria are set so any`X509CRL`will match.

## Public methods

### addIssuer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addIssuer(issuer: X500Principal!): Unit
```

Adds a name to the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names.

This method allows the caller to add a name to the set of issuer names which`X509CRLs`may contain. The specified name is added to any previous value for the issuerNames criterion. If the specified name is a duplicate, it may be ignored.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `issuer` | [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!:the issuer as X500Principal |

### addIssuerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addIssuerName(name: ByteArray!): Unit
```

Adds a name to the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names.

This method allows the caller to add a name to the set of issuer names which`X509CRLs`may contain. The specified name is added to any previous value for the issuerNames criterion. If the specified name is a duplicate, it may be ignored. If a name is specified as a byte array, it should contain a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is as follows.

The name is provided as a byte array. This byte array should contain a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure appears in the documentation for [setIssuerNames(java.util.Collection)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuerNames(kotlin.collections.MutableCollection)).

Note that the byte array supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:a byte array containing the name in ASN.1 DER encoded form |

| Exceptions ||
|-----------------------|---------------------------|
| `java.io.IOException` | if a parsing error occurs |

### addIssuerName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addIssuerName(name: String!): Unit
```

**Denigrated** , use [addIssuer(javax.security.auth.x500.X500Principal)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuer(javax.security.auth.x500.X500Principal))or[addIssuerName(byte\[\])](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuerName(kotlin.ByteArray))instead. This method should not be relied on as it can fail to match some CRLs because of a loss of encoding information in the RFC 2253 String form of some distinguished names.

Adds a name to the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names.

This method allows the caller to add a name to the set of issuer names which`X509CRLs`may contain. The specified name is added to any previous value for the issuerNames criterion. If the specified name is a duplicate, it may be ignored.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name in RFC 2253 form |

| Exceptions ||
|-----------------------|---------------------------|
| `java.io.IOException` | if a parsing error occurs |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a copy of this object.

| Return ||
|----------------------------------------------------------------------------|----------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | the copy |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getCertificateChecking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertificateChecking(): X509Certificate!
```

Returns the certificate being checked. This is not a criterion. Rather, it is optional information that may help a`CertStore`find CRLs that would be relevant when checking revocation for the specified certificate. If the value returned is`null`, then no such optional information is provided.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------------------------|
| [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)! | the certificate being checked (or`null`) |

**See Also**

- [#setCertificateChecking](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setCertificateChecking(java.security.cert.X509Certificate)) 

### getDateAndTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDateAndTime(): Date!
```

Returns the dateAndTime criterion. The specified date must be equal to or later than the value of the thisUpdate component of the`X509CRL`and earlier than the value of the nextUpdate component. There is no match if the`X509CRL`does not contain a nextUpdate component. If`null`, no dateAndTime check will be done.

Note that the`Date`returned is cloned to protect against subsequent modifications.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------|
| [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)! | the`Date`to match against (or`null`) |

**See Also**

- [#setDateAndTime](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setDateAndTime(java.util.Date)) 

### getIssuerNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuerNames(): MutableCollection<Any!>!
```

Returns a copy of the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names. If the value returned is`null`, any issuer distinguished name will do.

If the value returned is not`null`, it is a`Collection`of names. Each name is a`String`or a byte array representing a distinguished name (in RFC 2253 or ASN.1 DER encoded form, respectively). Note that the`Collection`returned may contain duplicate names.

If a name is specified as a byte array, it should contain a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is given in the documentation for [setIssuerNames(java.util.Collection)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuerNames(kotlin.collections.MutableCollection)).

Note that a deep copy is performed on the`Collection`to protect against subsequent modifications.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a`Collection`of names (or`null`) |

**See Also**

- [#setIssuerNames](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuerNames(kotlin.collections.MutableCollection)) 

### getIssuers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIssuers(): MutableCollection<X500Principal!>!
```

Returns the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names. If the value returned is`null`, any issuer distinguished name will do.

If the value returned is not`null`, it is a unmodifiable`Collection`of`X500Principal`s.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!>! | an unmodifiable`Collection`of names (or`null`) |

**See Also**

- [#setIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuers(kotlin.collections.MutableCollection)) 

### getMaxCRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxCRL(): BigInteger!
```

Returns the maxCRLNumber criterion. The`X509CRL`must have a CRL number extension whose value is less than or equal to the specified value. If`null`, no maxCRLNumber check will be done.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the maximum CRL number accepted (or`null`) |

### getMinCRL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMinCRL(): BigInteger!
```

Returns the minCRLNumber criterion. The`X509CRL`must have a CRL number extension whose value is greater than or equal to the specified value. If`null`, no minCRLNumber check will be done.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------|
| [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)! | the minimum CRL number accepted (or`null`) |

### match

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun match(crl: CRL!): Boolean
```

Decides whether a`CRL`should be selected.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `crl` | [CRL](https://developer.android.com/reference/kotlin/java/security/cert/CRL)!:the`CRL`to be checked |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the`CRL`should be selected,`false`otherwise |

### setCertificateChecking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCertificateChecking(cert: X509Certificate!): Unit
```

Sets the certificate being checked. This is not a criterion. Rather, it is optional information that may help a`CertStore`find CRLs that would be relevant when checking revocation for the specified certificate. If`null`is specified, then no such optional information is provided.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `cert` | [X509Certificate](https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate)!:the`X509Certificate`being checked (or`null`) |

**See Also**

- [#getCertificateChecking](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getCertificateChecking()) 

### setDateAndTime

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDateAndTime(dateAndTime: Date!): Unit
```

Sets the dateAndTime criterion. The specified date must be equal to or later than the value of the thisUpdate component of the`X509CRL`and earlier than the value of the nextUpdate component. There is no match if the`X509CRL`does not contain a nextUpdate component. If`null`, no dateAndTime check will be done.

Note that the`Date`supplied here is cloned to protect against subsequent modifications.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------|
| `dateAndTime` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:the`Date`to match against (or`null`) |

**See Also**

- [#getDateAndTime](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getDateAndTime()) 

### setIssuerNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIssuerNames(names: MutableCollection<*>!): Unit
```

**Note:** use [setIssuers(java.util.Collection)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#setIssuers(kotlin.collections.MutableCollection))instead or only specify the byte array form of distinguished names when using this method. See [addIssuerName(java.lang.String)](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#addIssuerName(kotlin.String))for more information.

Sets the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names. If`null`, any issuer distinguished name will do.

This method allows the caller to specify, with a single method call, the complete set of issuer names which`X509CRLs`may contain. The specified value replaces the previous value for the issuerNames criterion.

The`names`parameter (if not`null`) is a`Collection`of names. Each name is a`String`or a byte array representing a distinguished name (in [RFC 2253](http://www.ietf.org/rfc/rfc2253.txt) or ASN.1 DER encoded form, respectively). If`null`is supplied as the value for this argument, no issuerNames check will be performed.

Note that the`names`parameter can contain duplicate distinguished names, but they may be removed from the`Collection`of names returned by the [getIssuerNames](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuerNames())method.

If a name is specified as a byte array, it should contain a single DER encoded distinguished name, as defined in X.501. The ASN.1 notation for this structure is as follows. 

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

Note that a deep copy is performed on the`Collection`to protect against subsequent modifications.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `names` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<\*\>!:a`Collection`of names (or`null`) |

| Exceptions ||
|-----------------------|---------------------------|
| `java.io.IOException` | if a parsing error occurs |

**See Also**

- [#getIssuerNames](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuerNames()) 

### setIssuers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIssuers(issuers: MutableCollection<X500Principal!>!): Unit
```

Sets the issuerNames criterion. The issuer distinguished name in the`X509CRL`must match at least one of the specified distinguished names. If`null`, any issuer distinguished name will do.

This method allows the caller to specify, with a single method call, the complete set of issuer names which`X509CRLs`may contain. The specified value replaces the previous value for the issuerNames criterion.

The`names`parameter (if not`null`) is a`Collection`of`X500Principal`s.

Note that the`names`parameter can contain duplicate distinguished names, but they may be removed from the`Collection`of names returned by the [getIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuers())method.

Note that a copy is performed on the`Collection`to protect against subsequent modifications.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `issuers` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [X500Principal](https://developer.android.com/reference/kotlin/javax/security/auth/x500/X500Principal.html#)!\>!:a`Collection`of X500Principals (or`null`) |

**See Also**

- [#getIssuers](https://developer.android.com/reference/kotlin/java/security/cert/X509CRLSelector#getIssuers()) 

### setMaxCRLNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxCRLNumber(maxCRL: BigInteger!): Unit
```

Sets the maxCRLNumber criterion. The`X509CRL`must have a CRL number extension whose value is less than or equal to the specified value. If`null`, no maxCRLNumber check will be done.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `maxCRL` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the maximum CRL number accepted (or`null`) |

### setMinCRLNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMinCRLNumber(minCRL: BigInteger!): Unit
```

Sets the minCRLNumber criterion. The`X509CRL`must have a CRL number extension whose value is greater than or equal to the specified value. If`null`, no minCRLNumber check will be done.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `minCRL` | [BigInteger](https://developer.android.com/reference/kotlin/java/math/BigInteger.html#)!:the minimum CRL number accepted (or`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a printable representation of the`X509CRLSelector`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of the`X509CRLSelector`. |
