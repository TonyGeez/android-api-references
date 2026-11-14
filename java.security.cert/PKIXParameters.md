Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXParameters

```
open class PKIXParameters : CertPathParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.PKIXParameters](../java/security/cert/PKIXParameters.md) |

| Known Direct Subclasses [PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md) |---|---| | [PKIXBuilderParameters](../java/security/cert/PKIXBuilderParameters.md) | Parameters used as input for the PKIX `CertPathBuilder` algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

Parameters used as input for the PKIX `CertPathValidator` algorithm.

A PKIX `CertPathValidator` uses these parameters to validate a `CertPath` according to the PKIX certification path validation algorithm.

To instantiate a `PKIXParameters` object, an application must specify one or more *most-trusted CAs* as defined by the PKIX certification path validation algorithm. The most-trusted CAs can be specified using one of two constructors. An application can call `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#PKIXParameters(kotlin.collections.MutableSet)`, specifying a `Set` of `TrustAnchor` objects, each of which identify a most-trusted CA. Alternatively, an application can call `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#PKIXParameters(java.security.KeyStore)`, specifying a `KeyStore` instance containing trusted certificate entries, each of which will be considered as a most-trusted CA.

Once a `PKIXParameters` object has been created, other parameters can be specified (by calling `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setInitialPolicies(kotlin.collections.MutableSet)` or `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setDate(java.util.Date)`, for instance) and then the `PKIXParameters` is passed along with the `CertPath` to be validated to `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters)`.

Any parameter that is not set (or is set to `null`) will be set to the default value for that parameter. The default value for the `date` parameter is `null`, which indicates the current time when the path is validated. The default for the remaining parameters is the least constrained.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#PKIXParameters(java.security.KeyStore)(keystore: https://developer.android.com/reference/kotlin/java/security/KeyStore.html#!)` Creates an instance of `PKIXParameters` that populates the set of most-trusted CAs from the trusted certificate entries contained in the specified `KeyStore`. |
| `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#PKIXParameters(kotlin.collections.MutableSet)(trustAnchors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor!>!)` Creates an instance of `PKIXParameters` with the specified `Set` of most-trusted CAs. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#addCertPathChecker(java.security.cert.PKIXCertPathChecker)(checker: https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker!)` Adds a `PKIXCertPathChecker` to the list of certification path checkers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#addCertStore(java.security.cert.CertStore)(store: https://developer.android.com/reference/kotlin/java/security/cert/CertStore!)` Adds a `CertStore` to the end of the list of `CertStore`s used in finding certificates and CRLs. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#clone()()` Makes a copy of this `PKIXParameters` object. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getCertPathCheckers()()` Returns the `List` of certification path checkers. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CertStore](../java/security/cert/CertStore.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getCertStores()()` Returns an immutable `List` of `CertStore`s that are used to find certificates and CRLs. |
| open [Date](../java/util/Date.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getDate()()` Returns the time for which the validity of the certification path should be determined. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getInitialPolicies()()` Returns an immutable `Set` of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getPolicyQualifiersRejected()()` Gets the PolicyQualifiersRejected flag. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getSigProvider()()` Returns the signature provider's name, or `null` if not set. |
| --- | --- |
| open [CertSelector](../java/security/cert/CertSelector.md)! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getTargetCertConstraints()()` Returns the required constraints on the target certificate. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TrustAnchor](../java/security/cert/TrustAnchor.md)!\>! | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getTrustAnchors()()` Returns an immutable `Set` of the most-trusted CAs. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isAnyPolicyInhibited()()` Checks whether the any policy OID should be processed if it is included in a certificate. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isExplicitPolicyRequired()()` Checks if explicit policy is required. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isPolicyMappingInhibited()()` Checks if policy mapping is inhibited. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isRevocationEnabled()()` Checks the RevocationEnabled flag. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setAnyPolicyInhibited(kotlin.Boolean)(val: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets state to determine if the any policy OID should be processed if it is included in a certificate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList)(checkers: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker!>!)` Sets a `List` of additional certification path checkers. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertStores(kotlin.collections.MutableList)(stores: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/CertStore!>!)` Sets the list of `CertStore`s to be used in finding certificates and CRLs. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setDate(java.util.Date)(date: https://developer.android.com/reference/kotlin/java/util/Date.html#!)` Sets the time for which the validity of the certification path should be determined. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setExplicitPolicyRequired(kotlin.Boolean)(val: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the ExplicitPolicyRequired flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setInitialPolicies(kotlin.collections.MutableSet)(initialPolicies: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Sets the `Set` of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setPolicyMappingInhibited(kotlin.Boolean)(val: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the PolicyMappingInhibited flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setPolicyQualifiersRejected(kotlin.Boolean)(qualifiersRejected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the PolicyQualifiersRejected flag. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setRevocationEnabled(kotlin.Boolean)(val: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the RevocationEnabled flag. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setSigProvider(kotlin.String)(sigProvider: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the signature provider's name. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setTargetCertConstraints(java.security.cert.CertSelector)(selector: https://developer.android.com/reference/kotlin/java/security/cert/CertSelector!)` Sets the required constraints on the target certificate. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setTrustAnchors(kotlin.collections.MutableSet)(trustAnchors: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor!>!)` Sets the `Set` of most-trusted CAs. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#toString()()` Returns a formatted string describing the parameters. |

## Public constructors

### PKIXParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PKIXParameters(keystore: KeyStore!)
```

Creates an instance of `PKIXParameters` that populates the set of most-trusted CAs from the trusted certificate entries contained in the specified `KeyStore`. Only keystore entries that contain trusted `X509Certificates` are considered; all other certificate types are ignored.

| Parameters ||
|---|---|
| `keystore` | [KeyStore](../java/security/KeyStore.md)!: a `KeyStore` from which the set of most-trusted CAs will be populated |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the keystore is `null` |
| `java.security.InvalidAlgorithmParameterException` | if the keystore does not contain at least one trusted certificate entry |
| `java.security.KeyStoreException` | if the keystore has not been initialized |
| --- | --- |

### PKIXParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PKIXParameters(trustAnchors: MutableSet<TrustAnchor!>!)
```

Creates an instance of `PKIXParameters` with the specified `Set` of most-trusted CAs. Each element of the set is a `https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor`.

Note that the `Set` is copied to protect against subsequent modifications.

| Parameters ||
|---|---|
| `trustAnchors` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TrustAnchor](../java/security/cert/TrustAnchor.md)!\>!: a `Set` of `TrustAnchor`s |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any of the elements in the `Set` are not of type `java.security.cert.TrustAnchor` |
| `java.lang.NullPointerException` | if the specified `Set` is `null` |
| `java.security.InvalidAlgorithmParameterException` | if the specified `Set` is empty `(trustAnchors.isEmpty() == true)` |
| --- | --- |

## Public methods

### addCertPathChecker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCertPathChecker(checker: PKIXCertPathChecker!): Unit
```

Adds a `PKIXCertPathChecker` to the list of certification path checkers. See the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList)` method for more details.

Note that the `PKIXCertPathChecker` is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `checker` | [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!: a `PKIXCertPathChecker` to add to the list of checks. If `null`, the checker is ignored (not added to list). |

### addCertStore

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addCertStore(store: CertStore!): Unit
```

Adds a `CertStore` to the end of the list of `CertStore`s used in finding certificates and CRLs.

| Parameters ||
|---|---|
| `store` | [CertStore](../java/security/cert/CertStore.md)!: the `CertStore` to add. If `null`, the store is ignored (not added to list). |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Makes a copy of this `PKIXParameters` object. Changes to the copy will not affect the original and vice versa.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a copy of this `PKIXParameters` object |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### getCertPathCheckers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertPathCheckers(): MutableList<PKIXCertPathChecker!>!
```

Returns the `List` of certification path checkers. The returned `List` is immutable, and each `PKIXCertPathChecker` in the `List` is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker!>!` | an immutable `List` of `PKIXCertPathChecker`s (may be empty, but not `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList)`

### getCertStores

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertStores(): MutableList<CertStore!>!
```

Returns an immutable `List` of `CertStore`s that are used to find certificates and CRLs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/security/cert/CertStore!>!` | an immutable `List` of `CertStore`s (may be empty, but never `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertStores(kotlin.collections.MutableList)`

### getDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDate(): Date!
```

Returns the time for which the validity of the certification path should be determined. If `null`, the current time is used.

Note that the `Date` returned is copied to protect against subsequent modifications.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Date.html#!` | the `Date`, or `null` if not set |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setDate(java.util.Date)`

### getInitialPolicies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialPolicies(): MutableSet<String!>!
```

Returns an immutable `Set` of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. The default return value is an empty `Set`, which is interpreted as meaning that any policy would be acceptable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | an immutable `Set` of initial policy OIDs in `String` format, or an empty `Set` (implying any policy is acceptable). Never returns `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setInitialPolicies(kotlin.collections.MutableSet)`

### getPolicyQualifiersRejected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPolicyQualifiersRejected(): Boolean
```

Gets the PolicyQualifiersRejected flag. If this flag is true, certificates that include policy qualifiers in a certificate policies extension that is marked critical are rejected. If the flag is false, certificates are not rejected on this basis.

When a `PKIXParameters` object is created, this flag is set to true. This setting reflects the most common (and simplest) strategy for processing policy qualifiers. Applications that want to use a more sophisticated policy must set this flag to false.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the current value of the PolicyQualifiersRejected flag |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setPolicyQualifiersRejected(kotlin.Boolean)`

### getSigProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSigProvider(): String!
```

Returns the signature provider's name, or `null` if not set.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the signature provider's name (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setSigProvider(kotlin.String)`

### getTargetCertConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTargetCertConstraints(): CertSelector!
```

Returns the required constraints on the target certificate. The constraints are returned as an instance of `CertSelector`. If `null`, no constraints are defined.

Note that the `CertSelector` returned is cloned to protect against subsequent modifications.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertSelector!` | a `CertSelector` specifying the constraints on the target certificate (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setTargetCertConstraints(java.security.cert.CertSelector)`

### getTrustAnchors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTrustAnchors(): MutableSet<TrustAnchor!>!
```

Returns an immutable `Set` of the most-trusted CAs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor!>!` | an immutable `Set` of `TrustAnchor`s (never `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setTrustAnchors(kotlin.collections.MutableSet)`

### isAnyPolicyInhibited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAnyPolicyInhibited(): Boolean
```

Checks whether the any policy OID should be processed if it is included in a certificate.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the any policy OID is inhibited, `false` otherwise |

### isExplicitPolicyRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isExplicitPolicyRequired(): Boolean
```

Checks if explicit policy is required. If this flag is true, an acceptable policy needs to be explicitly identified in every certificate. By default, the ExplicitPolicyRequired flag is false.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if explicit policy is required, `false` otherwise |

### isPolicyMappingInhibited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isPolicyMappingInhibited(): Boolean
```

Checks if policy mapping is inhibited. If this flag is true, policy mapping is inhibited. By default, policy mapping is not inhibited (the flag is false).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if policy mapping is inhibited, false otherwise |

### isRevocationEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRevocationEnabled(): Boolean
```

Checks the RevocationEnabled flag. If this flag is true, the default revocation checking mechanism of the underlying PKIX service provider will be used. If this flag is false, the default revocation checking mechanism will be disabled (not used). See the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setRevocationEnabled(kotlin.Boolean)` method for more details on setting the value of this flag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the current value of the RevocationEnabled flag |

### setAnyPolicyInhibited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAnyPolicyInhibited(val: Boolean): Unit
```

Sets state to determine if the any policy OID should be processed if it is included in a certificate. By default, the any policy OID is not inhibited (`https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#isAnyPolicyInhibited()` returns `false`).

| Parameters ||
|---|---|
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the any policy OID is to be inhibited, `false` otherwise |

### setCertPathCheckers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCertPathCheckers(checkers: MutableList<PKIXCertPathChecker!>!): Unit
```

Sets a `List` of additional certification path checkers. If the specified `List` contains an object that is not a `PKIXCertPathChecker`, it is ignored.

Each `PKIXCertPathChecker` specified implements additional checks on a certificate. Typically, these are checks to process and verify private extensions contained in certificates. Each `PKIXCertPathChecker` should be instantiated with any initialization parameters needed to execute the check.

This method allows sophisticated applications to extend a PKIX `CertPathValidator` or `CertPathBuilder`. Each of the specified `PKIXCertPathChecker`s will be called, in turn, by a PKIX `CertPathValidator` or `CertPathBuilder` for each certificate processed or validated.

Regardless of whether these additional `PKIXCertPathChecker`s are set, a PKIX `CertPathValidator` or `CertPathBuilder` must perform all of the required PKIX checks on each certificate. The one exception to this rule is if the RevocationEnabled flag is set to false (see the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setRevocationEnabled(kotlin.Boolean)` method).

Note that the `List` supplied here is copied and each `PKIXCertPathChecker` in the list is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `checkers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PKIXCertPathChecker](../java/security/cert/PKIXCertPathChecker.md)!\>!: a `List` of `PKIXCertPathChecker`s. May be `null`, in which case no additional checkers will be used. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any of the elements in the list are not of type `java.security.cert.PKIXCertPathChecker` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getCertPathCheckers()`

### setCertStores

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setCertStores(stores: MutableList<CertStore!>!): Unit
```

Sets the list of `CertStore`s to be used in finding certificates and CRLs. May be `null`, in which case no `CertStore`s will be used. The first `CertStore`s in the list may be preferred to those that appear later.

Note that the `List` is copied to protect against subsequent modifications.

| Parameters ||
|---|---|
| `stores` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CertStore](../java/security/cert/CertStore.md)!\>!: a `List` of `CertStore`s (or `null`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any of the elements in the list are not of type `java.security.cert.CertStore` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getCertStores()`

### setDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDate(date: Date!): Unit
```

Sets the time for which the validity of the certification path should be determined. If `null`, the current time is used.

Note that the `Date` supplied here is copied to protect against subsequent modifications.

| Parameters ||
|---|---|
| `date` | [Date](../java/util/Date.md)!: the `Date`, or `null` for the current time |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getDate()`

### setExplicitPolicyRequired

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExplicitPolicyRequired(val: Boolean): Unit
```

Sets the ExplicitPolicyRequired flag. If this flag is true, an acceptable policy needs to be explicitly identified in every certificate. By default, the ExplicitPolicyRequired flag is false.

| Parameters ||
|---|---|
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if explicit policy is to be required, `false` otherwise |

### setInitialPolicies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInitialPolicies(initialPolicies: MutableSet<String!>!): Unit
```

Sets the `Set` of initial policy identifiers (OID strings), indicating that any one of these policies would be acceptable to the certificate user for the purposes of certification path processing. By default, any policy is acceptable (i.e. all policies), so a user that wants to allow any policy as acceptable does not need to call this method, or can call it with an empty `Set` (or `null`).

Note that the `Set` is copied to protect against subsequent modifications.

| Parameters ||
|---|---|
| `initialPolicies` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: a `Set` of initial policy OIDs in `String` format (or `null`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any of the elements in the set are not of type `String` |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getInitialPolicies()`

### setPolicyMappingInhibited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPolicyMappingInhibited(val: Boolean): Unit
```

Sets the PolicyMappingInhibited flag. If this flag is true, policy mapping is inhibited. By default, policy mapping is not inhibited (the flag is false).

| Parameters ||
|---|---|
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if policy mapping is to be inhibited, `false` otherwise |

### setPolicyQualifiersRejected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setPolicyQualifiersRejected(qualifiersRejected: Boolean): Unit
```

Sets the PolicyQualifiersRejected flag. If this flag is true, certificates that include policy qualifiers in a certificate policies extension that is marked critical are rejected. If the flag is false, certificates are not rejected on this basis.

When a `PKIXParameters` object is created, this flag is set to true. This setting reflects the most common (and simplest) strategy for processing policy qualifiers. Applications that want to use a more sophisticated policy must set this flag to false.

Note that the PKIX certification path validation algorithm specifies that any policy qualifier in a certificate policies extension that is marked critical must be processed and validated. Otherwise the certification path must be rejected. If the policyQualifiersRejected flag is set to false, it is up to the application to validate all policy qualifiers in this manner in order to be PKIX compliant.

| Parameters ||
|---|---|
| `qualifiersRejected` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the new value of the PolicyQualifiersRejected flag |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getPolicyQualifiersRejected()`
- `https://developer.android.com/reference/kotlin/java/security/cert/PolicyQualifierInfo`

### setRevocationEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRevocationEnabled(val: Boolean): Unit
```

Sets the RevocationEnabled flag. If this flag is true, the default revocation checking mechanism of the underlying PKIX service provider will be used. If this flag is false, the default revocation checking mechanism will be disabled (not used).

When a `PKIXParameters` object is created, this flag is set to true. This setting reflects the most common strategy for checking revocation, since each service provider must support revocation checking to be PKIX compliant. Sophisticated applications should set this flag to false when it is not practical to use a PKIX service provider's default revocation checking mechanism or when an alternative revocation checking mechanism is to be substituted (by also calling the `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#addCertPathChecker(java.security.cert.PKIXCertPathChecker)` or `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList)` methods).

| Parameters ||
|---|---|
| `val` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the new value of the RevocationEnabled flag |

### setSigProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSigProvider(sigProvider: String!): Unit
```

Sets the signature provider's name. The specified provider will be preferred when creating `https://developer.android.com/reference/kotlin/java/security/Signature.html#` objects. If `null` or not set, the first provider found supporting the algorithm will be used.

| Parameters ||
|---|---|
| `sigProvider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the signature provider's name (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getSigProvider()`

### setTargetCertConstraints

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTargetCertConstraints(selector: CertSelector!): Unit
```

Sets the required constraints on the target certificate. The constraints are specified as an instance of `CertSelector`. If `null`, no constraints are defined.

Note that the `CertSelector` specified is cloned to protect against subsequent modifications.

| Parameters ||
|---|---|
| `selector` | [CertSelector](../java/security/cert/CertSelector.md)!: a `CertSelector` specifying the constraints on the target certificate (or `null`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getTargetCertConstraints()`

### setTrustAnchors

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setTrustAnchors(trustAnchors: MutableSet<TrustAnchor!>!): Unit
```

Sets the `Set` of most-trusted CAs.

Note that the `Set` is copied to protect against subsequent modifications.

| Parameters ||
|---|---|
| `trustAnchors` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [TrustAnchor](../java/security/cert/TrustAnchor.md)!\>!: a `Set` of `TrustAnchor`s |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if any of the elements in the set are not of type `java.security.cert.TrustAnchor` |
| `java.lang.NullPointerException` | if the specified `Set` is `null` |
| `java.security.InvalidAlgorithmParameterException` | if the specified `Set` is empty `(trustAnchors.isEmpty() == true)` |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#getTrustAnchors()`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a formatted string describing the parameters.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a formatted string describing the parameters. |
