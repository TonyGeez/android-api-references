# CertPathChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathChecker

```
interface CertPathChecker
```

| [java.security.cert.CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker#) |

| Known Direct Subclasses [PKIXCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker) |--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------| | [PKIXCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker) | An abstract class that performs one or more checks on an`X509Certificate`. | |

| Known Indirect Subclasses [PKIXRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [PKIXRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker) | A`PKIXCertPathChecker`for checking the revocation status of certificates with the PKIX algorithm. | |

Performs one or more checks on each`Certificate`of a`CertPath`.

A`CertPathChecker`implementation is typically created to extend a certification path validation algorithm. For example, an implementation may check for and process a critical private extension of each certificate in a certification path.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [check](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker#check(java.security.cert.Certificate))`(`cert:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!`)` Performs the check(s) on the specified certificate using its internal state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker#init(kotlin.Boolean))`(`forward:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initializes the internal state of this`CertPathChecker`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForwardCheckingSupported](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker#isForwardCheckingSupported())`()` Indicates if forward checking is supported. |

## Public methods

### check

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun check(cert: Certificate!): Unit
```

Performs the check(s) on the specified certificate using its internal state. The certificates are presented in the order specified by the`init`method.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!:the`Certificate`to be checked |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if the specified certificate does not pass the check |

### init

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun init(forward: Boolean): Unit
```

Initializes the internal state of this`CertPathChecker`.

The`forward`flag specifies the order that certificates will be passed to the [check](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker#check(java.security.cert.Certificate))method (forward or reverse).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `forward` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the order that certificates are presented to the`check`method. If`true`, certificates are presented from target to trust anchor (forward); if`false`, from trust anchor to target (reverse). |

| Exceptions ||
|-------------------------------------------------|--------------------------------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if this`CertPathChecker`is unable to check certificates in the specified order |

### isForwardCheckingSupported

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isForwardCheckingSupported(): Boolean
```

Indicates if forward checking is supported. Forward checking refers to the ability of the`CertPathChecker`to perform its checks when certificates are presented to the`check`method in the forward direction (from target to trust anchor).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if forward checking is supported,`false`otherwise |
