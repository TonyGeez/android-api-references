# PKIXCertPathBuilderResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXCertPathBuilderResult

```
open class PKIXCertPathBuilderResult : PKIXCertPathValidatorResult, CertPathBuilderResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.cert.PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) ||
| | ↳ | [java.security.cert.PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) |

This class represents the successful result of the PKIX certification path builder algorithm. All certification paths that are built and returned using this algorithm are also validated according to the PKIX certification path validation algorithm.

Instances of`PKIXCertPathBuilderResult`are returned by the`build`method of`CertPathBuilder`objects implementing the PKIX algorithm.

All`PKIXCertPathBuilderResult`objects contain the certification path constructed by the build algorithm, the valid policy tree and subject public key resulting from the build algorithm, and a`TrustAnchor`describing the certification authority (CA) that served as a trust anchor for the certification path.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md))`(`certPath:` ` [CertPath](CertPath.md)!`, `trustAnchor:` ` [TrustAnchor](TrustAnchor.md)!`, `policyTree:` ` [PolicyNode](PolicyNode.md)!`, `subjectPublicKey:` ` [PublicKey](../java.security/PublicKey.md)!`)` Creates an instance of`PKIXCertPathBuilderResult`containing the specified parameters. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CertPath](CertPath.md)! | [getCertPath](PKIXCertPathBuilderResult.md))`()` Returns the built and validated certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PKIXCertPathBuilderResult.md))`()` Return a printable representation of this`PKIXCertPathBuilderResult`. |

| Inherited functions ||
|---|---|
| From class [PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](PKIXCertPathValidatorResult.md))`()` <br /> Returns a copy of this object. <br /> | | [PolicyNode](PolicyNode.md)! | [getPolicyTree](PKIXCertPathValidatorResult.md))`()` <br /> Returns the root node of the valid policy tree resulting from the PKIX certification path validation algorithm. The`PolicyNode`object that is returned and any objects that it returns through public methods are immutable. Most applications will not need to examine the valid policy tree. They can achieve their policy processing goals by setting the policy-related parameters in`PKIXParameters`. However, more sophisticated applications, especially those that process policy qualifiers, may need to traverse the valid policy tree using the [PolicyNode.getParent](PolicyNode.md))and [PolicyNode.getChildren](PolicyNode.md))methods. <br /> | | [PublicKey](../java.security/PublicKey.md)! | [getPublicKey](PKIXCertPathValidatorResult.md))`()` <br /> Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable. <br /> | | [TrustAnchor](TrustAnchor.md)! | [getTrustAnchor](PKIXCertPathValidatorResult.md))`()` <br /> Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path. <br /> | ||

## Public constructors

### PKIXCertPathBuilderResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKIXCertPathBuilderResult(
    certPath: CertPath!, 
    trustAnchor: TrustAnchor!, 
    policyTree: PolicyNode!, 
    subjectPublicKey: PublicKey!)
```

Creates an instance of`PKIXCertPathBuilderResult`containing the specified parameters.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certPath` | [CertPath](CertPath.md)!:the validated`CertPath` |
| `trustAnchor` | [TrustAnchor](TrustAnchor.md)!:a`TrustAnchor`describing the CA that served as a trust anchor for the certification path |
| `policyTree` | [PolicyNode](PolicyNode.md)!:the immutable valid policy tree, or`null`if there are no valid policies |
| --- | --- |
| `subjectPublicKey` | [PublicKey](../java.security/PublicKey.md)!:the public key of the subject |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the`certPath`,`trustAnchor`or`subjectPublicKey`parameters are`null` |

## Public methods

### getCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertPath(): CertPath!
```

Returns the built and validated certification path. The`CertPath`object does not include the trust anchor. Instead, use the [getTrustAnchor()](PKIXCertPathValidatorResult.md))method to obtain the`TrustAnchor`that served as the trust anchor for the certification path.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------|
| [CertPath](CertPath.md)! | the built and validated`CertPath`(never`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a printable representation of this`PKIXCertPathBuilderResult`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of this`PKIXCertPathBuilderResult` |
