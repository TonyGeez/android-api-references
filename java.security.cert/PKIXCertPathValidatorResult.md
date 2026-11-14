# PKIXCertPathValidatorResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXCertPathValidatorResult

```
open class PKIXCertPathValidatorResult : CertPathValidatorResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#) |

| Known Direct Subclasses [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [PKIXCertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathBuilderResult) | This class represents the successful result of the PKIX certification path builder algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

This class represents the successful result of the PKIX certification path validation algorithm.

Instances of`PKIXCertPathValidatorResult`are returned by the [validate](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters))method of`CertPathValidator`objects implementing the PKIX algorithm.

All`PKIXCertPathValidatorResult`objects contain the valid policy tree and subject public key resulting from the validation algorithm, as well as a`TrustAnchor`describing the certification authority (CA) that served as a trust anchor for the certification path.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXCertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#PKIXCertPathValidatorResult(java.security.cert.TrustAnchor,%20java.security.cert.PolicyNode,%20java.security.PublicKey))`(`trustAnchor:` ` [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)!`, `policyTree:` ` [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)!`, `subjectPublicKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!`)` Creates an instance of`PKIXCertPathValidatorResult`containing the specified parameters. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#clone())`()` Returns a copy of this object. |
| open [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)! | [getPolicyTree](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getPolicyTree())`()` Returns the root node of the valid policy tree resulting from the PKIX certification path validation algorithm. |
| open [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)! | [getPublicKey](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getPublicKey())`()` Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable. |
| --- | --- |
| open [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)! | [getTrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#getTrustAnchor())`()` Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathValidatorResult#toString())`()` Return a printable representation of this`PKIXCertPathValidatorResult`. |

## Public constructors

### PKIXCertPathValidatorResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKIXCertPathValidatorResult(
    trustAnchor: TrustAnchor!, 
    policyTree: PolicyNode!, 
    subjectPublicKey: PublicKey!)
```

Creates an instance of`PKIXCertPathValidatorResult`containing the specified parameters.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trustAnchor` | [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)!:a`TrustAnchor`describing the CA that served as a trust anchor for the certification path |
| `policyTree` | [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)!:the immutable valid policy tree, or`null`if there are no valid policies |
| `subjectPublicKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)!:the public key of the subject |
| --- | --- |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the`subjectPublicKey`or`trustAnchor`parameters are`null` |

## Public methods

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

### getPolicyTree

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPolicyTree(): PolicyNode!
```

Returns the root node of the valid policy tree resulting from the PKIX certification path validation algorithm. The`PolicyNode`object that is returned and any objects that it returns through public methods are immutable.

Most applications will not need to examine the valid policy tree. They can achieve their policy processing goals by setting the policy-related parameters in`PKIXParameters`. However, more sophisticated applications, especially those that process policy qualifiers, may need to traverse the valid policy tree using the [PolicyNode.getParent](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode#getParent())and [PolicyNode.getChildren](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode#getChildren())methods.

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [PolicyNode](https://developer.android.com/reference/kotlin/java/security/cert/PolicyNode)! | the root node of the valid policy tree, or`null`if there are no valid policies |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicKey(): PublicKey!
```

Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------|
| [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey.html#)! | the public key of the subject (never`null`) |

### getTrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTrustAnchor(): TrustAnchor!
```

Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [TrustAnchor](https://developer.android.com/reference/kotlin/java/security/cert/TrustAnchor)! | the`TrustAnchor`(never`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a printable representation of this`PKIXCertPathValidatorResult`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of this`PKIXCertPathValidatorResult` |
