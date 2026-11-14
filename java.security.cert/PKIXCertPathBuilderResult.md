# PKIXCertPathBuilderResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXCertPathBuilderResult

```
open class PKIXCertPathBuilderResult : PKIXCertPathValidatorResult, CertPathBuilderResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.cert.PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult) ||
| | ↳ | [java.security.cert.PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult#) |

This class represents the successful result of the PKIX certification path builder algorithm. All certification paths that are built and returned using this algorithm are also validated according to the PKIX certification path validation algorithm.

Instances of`PKIXCertPathBuilderResult`are returned by the`build`method of`CertPathBuilder`objects implementing the PKIX algorithm.

All`PKIXCertPathBuilderResult`objects contain the certification path constructed by the build algorithm, the valid policy tree and subject public key resulting from the build algorithm, and a`TrustAnchor`describing the certification authority (CA) that served as a trust anchor for the certification path.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult#PKIXCertPathBuilderResult(java.security.cert.CertPath,%20java.security.cert.TrustAnchor,%20java.security.cert.PolicyNode,%20java.security.PublicKey))`(`certPath:` ` [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!`, `trustAnchor:` ` [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)!`, `policyTree:` ` [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)!`, `subjectPublicKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!`)` Creates an instance of`PKIXCertPathBuilderResult`containing the specified parameters. |

| Public methods ||
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | [getCertPath](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult#getCertPath())`()` Returns the built and validated certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult#toString())`()` Return a printable representation of this`PKIXCertPathBuilderResult`. |

| Inherited functions ||
|---|---|
| From class [PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult) |-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#clone())`()` <br /> Returns a copy of this object. <br /> | | [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)! | [getPolicyTree](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getPolicyTree())`()` <br /> Returns the root node of the valid policy tree resulting from the PKIX certification path validation algorithm. The`PolicyNode`object that is returned and any objects that it returns through public methods are immutable. Most applications will not need to examine the valid policy tree. They can achieve their policy processing goals by setting the policy-related parameters in`PKIXParameters`. However, more sophisticated applications, especially those that process policy qualifiers, may need to traverse the valid policy tree using the [PolicyNode.getParent](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode#getParent())and [PolicyNode.getChildren](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode#getChildren())methods. <br /> | | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)! | [getPublicKey](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getPublicKey())`()` <br /> Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable. <br /> | | [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)! | [getTrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getTrustAnchor())`()` <br /> Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path. <br /> | ||

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
| `certPath` | [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!:the validated`CertPath` |
| `trustAnchor` | [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)!:a`TrustAnchor`describing the CA that served as a trust anchor for the certification path |
| `policyTree` | [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)!:the immutable valid policy tree, or`null`if there are no valid policies |
| --- | --- |
| `subjectPublicKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!:the public key of the subject |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the`certPath`,`trustAnchor`or`subjectPublicKey`parameters are`null` |

## Public methods

### getCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCertPath(): CertPath!
```

Returns the built and validated certification path. The`CertPath`object does not include the trust anchor. Instead, use the [getTrustAnchor()](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getTrustAnchor())method to obtain the`TrustAnchor`that served as the trust anchor for the certification path.

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------|
| [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | the built and validated`CertPath`(never`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a printable representation of this`PKIXCertPathBuilderResult`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of this`PKIXCertPathBuilderResult` |
