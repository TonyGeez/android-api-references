# PKIXBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXBuilderParameters

```
open class PKIXBuilderParameters : PKIXParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.cert.PKIXParameters](../java/security/cert/PKIXParameters.md) ||
| | ↳ | [java.security.cert.PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md) |

Parameters used as input for the PKIX`CertPathBuilder`algorithm.

A PKIX`CertPathBuilder`uses these parameters to [build](../java/security/cert/CertPathBuilder.md))a`CertPath`which has been validated according to the PKIX certification path validation algorithm.

To instantiate a`PKIXBuilderParameters`object, an application must specify one or more*most-trusted CAs* as defined by the PKIX certification path validation algorithm. The most-trusted CA can be specified using one of two constructors. An application can call [PKIXBuilderParameters(Set, CertSelector)](../java/security/cert/PKIXBuilderParameters.md)), specifying a`Set`of`TrustAnchor`objects, each of which identifies a most-trusted CA. Alternatively, an application can call [PKIXBuilderParameters(KeyStore, CertSelector)](../java/security/cert/PKIXBuilderParameters.md)), specifying a`KeyStore`instance containing trusted certificate entries, each of which will be considered as a most-trusted CA.

In addition, an application must specify constraints on the target certificate that the`CertPathBuilder`will attempt to build a path to. The constraints are specified as a`CertSelector`object. These constraints should provide the`CertPathBuilder`with enough search criteria to find the target certificate. Minimal criteria for an`X509Certificate`usually include the subject name and/or one or more subject alternative names. If enough criteria is not specified, the`CertPathBuilder`may throw a`CertPathBuilderException`.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md))`(`keystore:` ` [KeyStore](../java/security/KeyStore.md)!`, `targetConstraints:` ` [CertSelector](../java/security/cert/CertSelector.md)!`)` Creates an instance of`PKIXBuilderParameters`that populates the set of most-trusted CAs from the trusted certificate entries contained in the specified`KeyStore`. |
| [PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md))`(`trustAnchors:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TrustAnchor](../java/security/cert/TrustAnchor.md)!>!`, `targetConstraints:` ` [CertSelector](../java/security/cert/CertSelector.md)!`)` Creates an instance of`PKIXBuilderParameters`with the specified`Set`of most-trusted CAs. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxPathLength](../java/security/cert/PKIXBuilderParameters.md))`()` Returns the value of the maximum number of intermediate non-self-issued certificates that may exist in a certification path. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMaxPathLength](../java/security/cert/PKIXBuilderParameters.md))`(`maxPathLength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of the maximum number of non-self-issued intermediate certificates that may exist in a certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/cert/PKIXBuilderParameters.md))`()` Returns a formatted string describing the parameters. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [PKIXParameters](../java/security/cert/PKIXParameters.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertPathChecker](../java/security/cert/PKIXParameters.md))`(`checker:` ` [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!`)` <br /> Adds a`PKIXCertPathChecker`to the list of certification path checkers. See the [setCertPathCheckers](../java/security/cert/PKIXParameters.md))method for more details. Note that the`PKIXCertPathChecker`is cloned to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertStore](../java/security/cert/PKIXParameters.md))`(`store:` ` [CertStore](../java/security/cert/CertStore.md)!`)` <br /> Adds a`CertStore`to the end of the list of`CertStore`s used in finding certificates and CRLs. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/security/cert/PKIXParameters.md))`()` <br /> Makes a copy of this`PKIXParameters`object. Changes to the copy will not affect the original and vice versa. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!>! | [getCertPathCheckers](../java/security/cert/PKIXParameters.md))`()` <br /> Returns the`List`of certification path checkers. The returned`List`is immutable, and each`PKIXCertPathChecker`in the`List`is cloned to protect against subsequent modifications. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CertStore](../java/security/cert/CertStore.md)!>! | [getCertStores](../java/security/cert/PKIXParameters.md))`()` <br /> Returns an immutable`List`of`CertStore`s that are used to find certificates and CRLs. <br /> | | [Date](../java/util/Date.md)! | [getDate](../java/security/cert/PKIXParameters.md))`()` <br /> Returns the time for which the validity of the certification path should be determined. If`null`, the current time is used. Note that the`Date`returned is copied to protect against subsequent modifications. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getInitialPolicies](../java/security/cert/PKIXParameters.md))`()` <br /> Returns an immutable`Set`of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. The default return value is an empty`Set`, which is interpreted as meaning that any policy would be acceptable. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPolicyQualifiersRejected](../java/security/cert/PKIXParameters.md))`()` <br /> Gets the PolicyQualifiersRejected flag. If this flag is true, certificates that include policy qualifiers in a certificate policies extension that is marked critical are rejected. If the flag is false, certificates are not rejected on this basis. When a`PKIXParameters`object is created, this flag is set to true. This setting reflects the most common (and simplest) strategy for processing policy qualifiers. Applications that want to use a more sophisticated policy must set this flag to false. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSigProvider](../java/security/cert/PKIXParameters.md))`()` <br /> Returns the signature provider's name, or`null`if not set. <br /> | | [CertSelector](../java/security/cert/CertSelector.md)! | [getTargetCertConstraints](../java/security/cert/PKIXParameters.md))`()` <br /> Returns the required constraints on the target certificate. The constraints are returned as an instance of`CertSelector`. If`null`, no constraints are defined. Note that the`CertSelector`returned is cloned to protect against subsequent modifications. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TrustAnchor](../java/security/cert/TrustAnchor.md)!>! | [getTrustAnchors](../java/security/cert/PKIXParameters.md))`()` <br /> Returns an immutable`Set`of the most-trusted CAs. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnyPolicyInhibited](../java/security/cert/PKIXParameters.md))`()` <br /> Checks whether the any policy OID should be processed if it is included in a certificate. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isExplicitPolicyRequired](../java/security/cert/PKIXParameters.md))`()` <br /> Checks if explicit policy is required. If this flag is true, an acceptable policy needs to be explicitly identified in every certificate. By default, the ExplicitPolicyRequired flag is false. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPolicyMappingInhibited](../java/security/cert/PKIXParameters.md))`()` <br /> Checks if policy mapping is inhibited. If this flag is true, policy mapping is inhibited. By default, policy mapping is not inhibited (the flag is false). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRevocationEnabled](../java/security/cert/PKIXParameters.md))`()` <br /> Checks the RevocationEnabled flag. If this flag is true, the default revocation checking mechanism of the underlying PKIX service provider will be used. If this flag is false, the default revocation checking mechanism will be disabled (not used). See the [setRevocationEnabled](../java/security/cert/PKIXParameters.md))method for more details on setting the value of this flag. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnyPolicyInhibited](../java/security/cert/PKIXParameters.md))`(`val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets state to determine if the any policy OID should be processed if it is included in a certificate. By default, the any policy OID is not inhibited ([isAnyPolicyInhibited()](../java/security/cert/PKIXParameters.md))returns`false`). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertPathCheckers](../java/security/cert/PKIXParameters.md))`(`checkers:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!>!`)` <br /> Sets a`List`of additional certification path checkers. If the specified`List`contains an object that is not a`PKIXCertPathChecker`, it is ignored. Each`PKIXCertPathChecker`specified implements additional checks on a certificate. Typically, these are checks to process and verify private extensions contained in certificates. Each`PKIXCertPathChecker`should be instantiated with any initialization parameters needed to execute the check. This method allows sophisticated applications to extend a PKIX`CertPathValidator`or`CertPathBuilder`. Each of the specified`PKIXCertPathChecker`s will be called, in turn, by a PKIX`CertPathValidator`or`CertPathBuilder`for each certificate processed or validated. Regardless of whether these additional`PKIXCertPathChecker`s are set, a PKIX`CertPathValidator`or`CertPathBuilder`must perform all of the required PKIX checks on each certificate. The one exception to this rule is if the RevocationEnabled flag is set to false (see the [setRevocationEnabled](../java/security/cert/PKIXParameters.md))method). Note that the`List`supplied here is copied and each`PKIXCertPathChecker`in the list is cloned to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCertStores](../java/security/cert/PKIXParameters.md))`(`stores:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CertStore](../java/security/cert/CertStore.md)!>!`)` <br /> Sets the list of`CertStore`s to be used in finding certificates and CRLs. May be`null`, in which case no`CertStore`s will be used. The first`CertStore`s in the list may be preferred to those that appear later. Note that the`List`is copied to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDate](../java/security/cert/PKIXParameters.md))`(`date:` ` [Date](../java/util/Date.md)!`)` <br /> Sets the time for which the validity of the certification path should be determined. If`null`, the current time is used. Note that the`Date`supplied here is copied to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setExplicitPolicyRequired](../java/security/cert/PKIXParameters.md))`(`val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the ExplicitPolicyRequired flag. If this flag is true, an acceptable policy needs to be explicitly identified in every certificate. By default, the ExplicitPolicyRequired flag is false. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInitialPolicies](../java/security/cert/PKIXParameters.md))`(`initialPolicies:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Sets the`Set`of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. By default, any policy is acceptable (i.e. all policies), so a user that wants to allow any policy as acceptable does not need to call this method, or can call it with an empty`Set`(or`null`). Note that the`Set`is copied to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPolicyMappingInhibited](../java/security/cert/PKIXParameters.md))`(`val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the PolicyMappingInhibited flag. If this flag is true, policy mapping is inhibited. By default, policy mapping is not inhibited (the flag is false). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPolicyQualifiersRejected](../java/security/cert/PKIXParameters.md))`(`qualifiersRejected:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the PolicyQualifiersRejected flag. If this flag is true, certificates that include policy qualifiers in a certificate policies extension that is marked critical are rejected. If the flag is false, certificates are not rejected on this basis. When a`PKIXParameters`object is created, this flag is set to true. This setting reflects the most common (and simplest) strategy for processing policy qualifiers. Applications that want to use a more sophisticated policy must set this flag to false. Note that the PKIX certification path validation algorithm specifies that any policy qualifier in a certificate policies extension that is marked critical must be processed and validated. Otherwise the certification path must be rejected. If the policyQualifiersRejected flag is set to false, it is up to the application to validate all policy qualifiers in this manner in order to be PKIX compliant. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRevocationEnabled](../java/security/cert/PKIXParameters.md))`(`val:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets the RevocationEnabled flag. If this flag is true, the default revocation checking mechanism of the underlying PKIX service provider will be used. If this flag is false, the default revocation checking mechanism will be disabled (not used). When a`PKIXParameters`object is created, this flag is set to true. This setting reflects the most common strategy for checking revocation, since each service provider must support revocation checking to be PKIX compliant. Sophisticated applications should set this flag to false when it is not practical to use a PKIX service provider's default revocation checking mechanism or when an alternative revocation checking mechanism is to be substituted (by also calling the [addCertPathChecker](../java/security/cert/PKIXParameters.md))or [setCertPathCheckers](../java/security/cert/PKIXParameters.md))methods). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSigProvider](../java/security/cert/PKIXParameters.md))`(`sigProvider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the signature provider's name. The specified provider will be preferred when creating [Signature](../java/security/Signature.md) objects. If`null`or not set, the first provider found supporting the algorithm will be used. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTargetCertConstraints](../java/security/cert/PKIXParameters.md))`(`selector:` ` [CertSelector](../java/security/cert/CertSelector.md)!`)` <br /> Sets the required constraints on the target certificate. The constraints are specified as an instance of`CertSelector`. If`null`, no constraints are defined. Note that the`CertSelector`specified is cloned to protect against subsequent modifications. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTrustAnchors](../java/security/cert/PKIXParameters.md))`(`trustAnchors:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [TrustAnchor](../java/security/cert/TrustAnchor.md)!>!`)` <br /> Sets the`Set`of most-trusted CAs. Note that the`Set`is copied to protect against subsequent modifications. <br /> | ||

## Public constructors

### PKIXBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKIXBuilderParameters(
    keystore: KeyStore!, 
    targetConstraints: CertSelector!)
```

Creates an instance of`PKIXBuilderParameters`that populates the set of most-trusted CAs from the trusted certificate entries contained in the specified`KeyStore`. Only keystore entries that contain trusted`X509Certificate`s are considered; all other certificate types are ignored.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keystore` | [KeyStore](../java/security/KeyStore.md)!:a`KeyStore`from which the set of most-trusted CAs will be populated |
| `targetConstraints` | [CertSelector](../java/security/cert/CertSelector.md)!:a`CertSelector`specifying the constraints on the target certificate |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------------------------|
| `java.security.KeyStoreException` | if`keystore`has not been initialized |
| `java.security.InvalidAlgorithmParameterException` | if`keystore`does not contain at least one trusted certificate entry |
| `java.lang.NullPointerException` | if`keystore`is`null` |
| --- | --- |

### PKIXBuilderParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKIXBuilderParameters(
    trustAnchors: MutableSet<TrustAnchor!>!, 
    targetConstraints: CertSelector!)
```

Creates an instance of`PKIXBuilderParameters`with the specified`Set`of most-trusted CAs. Each element of the set is a [TrustAnchor](../java/security/cert/TrustAnchor.md).

Note that the`Set`is copied to protect against subsequent modifications.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trustAnchors` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TrustAnchor](../java/security/cert/TrustAnchor.md)!\>!:a`Set`of`TrustAnchor`s |
| `targetConstraints` | [CertSelector](../java/security/cert/CertSelector.md)!:a`CertSelector`specifying the constraints on the target certificate |

| Exceptions ||
|----------------------------------------------------|----------------------------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if`trustAnchors`is empty`(trustAnchors.isEmpty() == true)` |
| `java.lang.NullPointerException` | if`trustAnchors`is`null` |
| `java.lang.ClassCastException` | if any of the elements of`trustAnchors`are not of type`java.security.cert.TrustAnchor` |
| --- | --- |

## Public methods

### getMaxPathLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxPathLength(): Int
```

Returns the value of the maximum number of intermediate non-self-issued certificates that may exist in a certification path. See the [setMaxPathLength](../java/security/cert/PKIXBuilderParameters.md))method for more details.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of non-self-issued intermediate certificates that may exist in a certification path, or -1 if there is no limit |

**See Also**

- [#setMaxPathLength](../java/security/cert/PKIXBuilderParameters.md)) 

### setMaxPathLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMaxPathLength(maxPathLength: Int): Unit
```

Sets the value of the maximum number of non-self-issued intermediate certificates that may exist in a certification path. A certificate is self-issued if the DNs that appear in the subject and issuer fields are identical and are not empty. Note that the last certificate in a certification path is not an intermediate certificate, and is not included in this limit. Usually the last certificate is an end entity certificate, but it can be a CA certificate. A PKIX`CertPathBuilder`instance must not build paths longer than the length specified.

A value of 0 implies that the path can only contain a single certificate. A value of -1 implies that the path length is unconstrained (i.e. there is no maximum). The default maximum path length, if not specified, is 5. Setting a value less than -1 will cause an exception to be thrown.

If any of the CA certificates contain the`BasicConstraintsExtension`, the value of the`pathLenConstraint`field of the extension overrides the maximum path length parameter whenever the result is a certification path of smaller length.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `maxPathLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of non-self-issued intermediate certificates that may exist in a certification path |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------|
| `java.security.InvalidParameterException` | if`maxPathLength`is set to a value less than -1 |

**See Also**

- [#getMaxPathLength](../java/security/cert/PKIXBuilderParameters.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a formatted string describing the parameters.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the parameters |
