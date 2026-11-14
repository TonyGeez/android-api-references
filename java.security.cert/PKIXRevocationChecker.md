Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXRevocationChecker

```
abstract class PKIXRevocationChecker : PKIXCertPathChecker
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.cert.PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md) ||
| | ↳ | [java.security.cert.PKIXRevocationChecker](../java/security/cert/PKIXRevocationChecker.md) |

A `PKIXCertPathChecker` for checking the revocation status of certificates with the PKIX algorithm.

A `PKIXRevocationChecker` checks the revocation status of certificates with the Online Certificate Status Protocol (OCSP) or Certificate Revocation Lists (CRLs). OCSP is described in RFC 2560 and is a network protocol for determining the status of a certificate. A CRL is a time-stamped list identifying revoked certificates, and RFC 5280 describes an algorithm for determining the revocation status of certificates using CRLs.

Each `PKIXRevocationChecker` must be able to check the revocation status of certificates with OCSP and CRLs. By default, OCSP is the preferred mechanism for checking revocation status, with CRLs as the fallback mechanism. However, this preference can be switched to CRLs with the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option` option. In addition, the fallback mechanism can be disabled with the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option` option.

A `PKIXRevocationChecker` is obtained by calling the `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getRevocationChecker()` method of a PKIX `CertPathValidator`. Additional parameters and options specific to revocation can be set (by calling the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOcspResponder(java.net.URI)` method for instance). The `PKIXRevocationChecker` is added to a `PKIXParameters` object using the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#addCertPathChecker(java.security.cert.PKIXCertPathChecker)` or `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList)` method, and then the `PKIXParameters` is passed along with the `CertPath` to be validated to the `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters)` method of a PKIX `CertPathValidator`. When supplying a revocation checker in this manner, it will be used to check revocation irrespective of the setting of the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isRevocationEnabled()` flag. Similarly, a `PKIXRevocationChecker` may be added to a `PKIXBuilderParameters` object for use with a PKIX `CertPathBuilder`.

Note that when a `PKIXRevocationChecker` is added to `PKIXParameters`, it clones the `PKIXRevocationChecker`; thus any subsequent modifications to the `PKIXRevocationChecker` have no effect.

Any parameter that is not set (or is set to `null`) will be set to the default value for that parameter.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option` Various revocation options that can be specified for the revocation checking mechanism. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#PKIXRevocationChecker()()` Default constructor. |

| Public methods ||
|---|---|
| open [PKIXRevocationChecker](../java/security/cert/PKIXRevocationChecker.md) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#clone()()` Returns a clone of this object. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Extension](../java/security/cert/Extension.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getOcspExtensions()()` Gets the optional OCSP request extensions. |
| open [URI](../java/net/URI.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getOcspResponder()()` Gets the URI that identifies the location of the OCSP responder. |
| --- | --- |
| open [X509Certificate](../java/security/cert/X509Certificate.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getOcspResponderCert()()` Gets the OCSP responder's certificate. |
| open [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getOcspResponses()()` Gets the OCSP responses. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PKIXRevocationChecker.Option](../java/security/cert/PKIXRevocationChecker.Option.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getOptions()()` Gets the revocation options. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CertPathValidatorException](../java/security/cert/CertPathValidatorException.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#getSoftFailExceptions()()` Returns a list containing the exceptions that are ignored by the revocation checker when the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option` option is set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOcspExtensions(kotlin.collections.MutableList)(extensions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Extension!>!)` Sets the optional OCSP request extensions. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOcspResponder(java.net.URI)(uri: https://developer.android.com/reference/kotlin/java/net/URI.html#!)` Sets the URI that identifies the location of the OCSP responder. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOcspResponderCert(java.security.cert.X509Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!)` Sets the OCSP responder's certificate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOcspResponses(kotlin.collections.MutableMap)(responses: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!>!)` Sets the OCSP responses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#setOptions(kotlin.collections.MutableSet)(options: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option!>!)` Sets the revocation options. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#check(java.security.cert.Certificate)(cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!)` Performs the check(s) on the specified certificate using its internal state. The certificates are presented in the order specified by the `init` method. This implementation calls `check(cert, java.util.Collections.<String>emptySet())`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#check(java.security.cert.Certificate,%20kotlin.collections.MutableCollection)(cert: https://developer.android.com/reference/kotlin/java/security/cert/Certificate!, unresolvedCritExts: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Performs the check(s) on the specified certificate using its internal state and removes any critical extensions that it processes from the specified collection of OID strings that represent the unresolved critical extensions. The certificates are presented in the order specified by the `init` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#getSupportedExtensions()()` Returns an immutable `Set` of X.509 certificate extensions that this `PKIXCertPathChecker` supports (i.e. recognizes, is able to process), or `null` if no extensions are supported. Each element of the set is a `String` representing the Object Identifier (OID) of the X.509 extension that is supported. The OID is represented by a set of nonnegative integers separated by periods. All X.509 certificate extensions that a `PKIXCertPathChecker` might possibly be able to process should be included in the set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#init(kotlin.Boolean)(forward: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Initializes the internal state of this `PKIXCertPathChecker`. The `forward` flag specifies the order that certificates will be passed to the #check method (forward or reverse). A `PKIXCertPathChecker` **must** support reverse checking and **may** support forward checking. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#isForwardCheckingSupported()()` Indicates if forward checking is supported. Forward checking refers to the ability of the `PKIXCertPathChecker` to perform its checks when certificates are presented to the `check` method in the forward direction (from target to most-trusted CA). <br /> | ||

## Protected constructors

### PKIXRevocationChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected PKIXRevocationChecker()
```

Default constructor.

## Public methods

### clone

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): PKIXRevocationChecker
```

Returns a clone of this object. Calls the `Object.clone()` method. All subclasses which maintain state must support and override this method, if necessary.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker#` | a copy of this `PKIXCertPathChecker` |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### getOcspExtensions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOcspExtensions(): MutableList<Extension!>!
```

Gets the optional OCSP request extensions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Extension!>!` | an unmodifiable list of extensions. The list is empty if no extensions have been specified. |

### getOcspResponder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOcspResponder(): URI!
```

Gets the URI that identifies the location of the OCSP responder. This overrides the `ocsp.responderURL` security property. If this parameter or the `ocsp.responderURL` property is not set, the location is determined from the certificate's Authority Information Access Extension, as defined in RFC 5280.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URI.html#!` | the responder URI, or `null` if not set |

### getOcspResponderCert

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOcspResponderCert(): X509Certificate!
```

Gets the OCSP responder's certificate. This overrides the `ocsp.responderCertSubjectName`, `ocsp.responderCertIssuerName`, and `ocsp.responderCertSerialNumber` security properties. If this parameter or the aforementioned properties are not set, then the responder's certificate is determined as specified in RFC 2560.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!` | the responder's certificate, or `null` if not set |

### getOcspResponses

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOcspResponses(): MutableMap<X509Certificate!, ByteArray!>!
```

Gets the OCSP responses. These responses are used to determine the revocation status of the specified certificates when OCSP is used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://developer.android.com/reference/kotlin/java/security/cert/X509Certificate!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!>!` | a map of OCSP responses. Each key is an `X509Certificate` that maps to the corresponding DER-encoded OCSP response for that certificate. A deep copy of the map is returned to protect against subsequent modification. Returns an empty map if no responses have been specified. |

### getOptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOptions(): MutableSet<PKIXRevocationChecker.Option!>!
```

Gets the revocation options.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option!>!` | an unmodifiable set of revocation options. The set is empty if no options have been specified. |

### getSoftFailExceptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getSoftFailExceptions(): MutableList<CertPathValidatorException!>!
```

Returns a list containing the exceptions that are ignored by the revocation checker when the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker.Option` option is set. The list is cleared each time `https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#init(kotlin.Boolean)` is called. The list is ordered in ascending order according to the certificate index returned by `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getIndex()` method of each entry.

An implementation of `PKIXRevocationChecker` is responsible for adding the ignored exceptions to the list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException!>!` | an unmodifiable list containing the ignored exceptions. The list is empty if no exceptions have been ignored. |

### setOcspExtensions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOcspExtensions(extensions: MutableList<Extension!>!): Unit
```

Sets the optional OCSP request extensions.

| Parameters ||
|---|---|
| `extensions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Extension](../java/security/cert/Extension.md)!\>!: a list of extensions. The list is copied to protect against subsequent modification. |

### setOcspResponder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOcspResponder(uri: URI!): Unit
```

Sets the URI that identifies the location of the OCSP responder. This overrides the `ocsp.responderURL` security property and any responder specified in a certificate's Authority Information Access Extension, as defined in RFC 5280.

| Parameters ||
|---|---|
| `uri` | [URI](../java/net/URI.md)!: the responder URI |

### setOcspResponderCert

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOcspResponderCert(cert: X509Certificate!): Unit
```

Sets the OCSP responder's certificate. This overrides the `ocsp.responderCertSubjectName`, `ocsp.responderCertIssuerName`, and `ocsp.responderCertSerialNumber` security properties.

| Parameters ||
|---|---|
| `cert` | [X509Certificate](../java/security/cert/X509Certificate.md)!: the responder's certificate |

### setOcspResponses

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOcspResponses(responses: MutableMap<X509Certificate!, ByteArray!>!): Unit
```

Sets the OCSP responses. These responses are used to determine the revocation status of the specified certificates when OCSP is used.

| Parameters ||
|---|---|
| `responses` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [X509Certificate](../java/security/cert/X509Certificate.md)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>!: a map of OCSP responses. Each key is an `X509Certificate` that maps to the corresponding DER-encoded OCSP response for that certificate. A deep copy of the map is performed to protect against subsequent modification. |

### setOptions

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOptions(options: MutableSet<PKIXRevocationChecker.Option!>!): Unit
```

Sets the revocation options.

| Parameters ||
|---|---|
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PKIXRevocationChecker.Option](../java/security/cert/PKIXRevocationChecker.Option.md)!\>!: a set of revocation options. The set is copied to protect against subsequent modification. |
