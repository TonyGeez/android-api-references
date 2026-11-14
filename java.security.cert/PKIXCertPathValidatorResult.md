# PKIXCertPathValidatorResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXCertPathValidatorResult

```
open class PKIXCertPathValidatorResult : CertPathValidatorResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md) |

| Known Direct Subclasses [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| | [PKIXCertPathBuilderResult](PKIXCertPathBuilderResult.md) | This class represents the successful result of the PKIX certification path builder algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

This class represents the successful result of the PKIX certification path validation algorithm.

Instances of`PKIXCertPathValidatorResult`are returned by the [validate](CertPathValidator.md))method of`CertPathValidator`objects implementing the PKIX algorithm.

All`PKIXCertPathValidatorResult`objects contain the valid policy tree and subject public key resulting from the validation algorithm, as well as a`TrustAnchor`describing the certification authority (CA) that served as a trust anchor for the certification path.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXCertPathValidatorResult](PKIXCertPathValidatorResult.md))`(`trustAnchor:` ` [TrustAnchor](TrustAnchor.md)!`, `policyTree:` ` [PolicyNode](PolicyNode.md)!`, `subjectPublicKey:` ` [PublicKey](../java.security/PublicKey.md)!`)` Creates an instance of`PKIXCertPathValidatorResult`containing the specified parameters. |

| Public methods ||
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](PKIXCertPathValidatorResult.md))`()` Returns a copy of this object. |
| open [PolicyNode](PolicyNode.md)! | [getPolicyTree](PKIXCertPathValidatorResult.md))`()` Returns the root node of the valid policy tree resulting from the PKIX certification path validation algorithm. |
| open [PublicKey](../java.security/PublicKey.md)! | [getPublicKey](PKIXCertPathValidatorResult.md))`()` Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable. |
| --- | --- |
| open [TrustAnchor](TrustAnchor.md)! | [getTrustAnchor](PKIXCertPathValidatorResult.md))`()` Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PKIXCertPathValidatorResult.md))`()` Return a printable representation of this`PKIXCertPathValidatorResult`. |

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
| `trustAnchor` | [TrustAnchor](TrustAnchor.md)!:a`TrustAnchor`describing the CA that served as a trust anchor for the certification path |
| `policyTree` | [PolicyNode](PolicyNode.md)!:the immutable valid policy tree, or`null`if there are no valid policies |
| `subjectPublicKey` | [PublicKey](../java.security/PublicKey.md)!:the public key of the subject |
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

Most applications will not need to examine the valid policy tree. They can achieve their policy processing goals by setting the policy-related parameters in`PKIXParameters`. However, more sophisticated applications, especially those that process policy qualifiers, may need to traverse the valid policy tree using the [PolicyNode.getParent](PolicyNode.md))and [PolicyNode.getChildren](PolicyNode.md))methods.

| Return ||
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [PolicyNode](PolicyNode.md)! | the root node of the valid policy tree, or`null`if there are no valid policies |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicKey(): PublicKey!
```

Returns the public key of the subject (target) of the certification path, including any inherited public key parameters if applicable.

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------|
| [PublicKey](../java.security/PublicKey.md)! | the public key of the subject (never`null`) |

### getTrustAnchor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTrustAnchor(): TrustAnchor!
```

Returns the`TrustAnchor`describing the CA that served as a trust anchor for the certification path.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------|
| [TrustAnchor](TrustAnchor.md)! | the`TrustAnchor`(never`null`) |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Return a printable representation of this`PKIXCertPathValidatorResult`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a`String`describing the contents of this`PKIXCertPathValidatorResult` |
