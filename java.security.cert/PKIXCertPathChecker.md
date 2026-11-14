# PKIXCertPathChecker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKIXCertPathChecker

```
abstract class PKIXCertPathChecker : CertPathChecker, Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.cert.PKIXCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#) |

| Known Direct Subclasses [PKIXRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [PKIXRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXRevocationChecker) | A`PKIXCertPathChecker`for checking the revocation status of certificates with the PKIX algorithm. | |

An abstract class that performs one or more checks on an`X509Certificate`.

A concrete implementation of the`PKIXCertPathChecker`class can be created to extend the PKIX certification path validation algorithm. For example, an implementation may check for and process a critical private extension of each certificate in a certification path.

Instances of`PKIXCertPathChecker`are passed as parameters using the [setCertPathCheckers](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#setCertPathCheckers(kotlin.collections.MutableList))or [addCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXParameters#addCertPathChecker(java.security.cert.PKIXCertPathChecker))methods of the`PKIXParameters`and`PKIXBuilderParameters`class. Each of the`PKIXCertPathChecker`s #check methods will be called, in turn, for each certificate processed by a PKIX`CertPathValidator`or`CertPathBuilder`implementation.

A`PKIXCertPathChecker`may be called multiple times on successive certificates in a certification path. Concrete subclasses are expected to maintain any internal state that may be necessary to check successive certificates. The [init](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#init(kotlin.Boolean))method is used to initialize the internal state of the checker so that the certificates of a new certification path may be checked. A stateful implementation**must** override the [clone](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#clone())method if necessary in order to allow a PKIX`CertPathBuilder`to efficiently backtrack and try other paths. In these situations, the`CertPathBuilder`is able to restore prior path validation states by restoring the cloned`PKIXCertPathChecker`s.

The order in which the certificates are presented to the`PKIXCertPathChecker`may be either in the forward direction (from target to most-trusted CA) or in the reverse direction (from most-trusted CA to target). A`PKIXCertPathChecker`implementation**must** support reverse checking (the ability to perform its checks when it is presented with certificates in the reverse direction) and**may** support forward checking (the ability to perform its checks when it is presented with certificates in the forward direction). The [isForwardCheckingSupported](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#isForwardCheckingSupported())method indicates whether forward checking is supported.

Additional input parameters required for executing the check may be specified through constructors of concrete implementations of this class.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKIXCertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#PKIXCertPathChecker())`()` Default constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [check](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#check(java.security.cert.Certificate))`(`cert:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!`)` Performs the check(s) on the specified certificate using its internal state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [check](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#check(java.security.cert.Certificate,%20kotlin.collections.MutableCollection))`(`cert:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!`, `unresolvedCritExts:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Performs the check(s) on the specified certificate using its internal state and removes any critical extensions that it processes from the specified collection of OID strings that represent the unresolved critical extensions. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#clone())`()` Returns a clone of this object. |
| abstract [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSupportedExtensions](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#getSupportedExtensions())`()` Returns an immutable`Set`of X. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#init(kotlin.Boolean))`(`forward:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Initializes the internal state of this`PKIXCertPathChecker`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isForwardCheckingSupported](https://developer.android.com/reference/kotlin/java/security/cert/PKIXCertPathChecker#isForwardCheckingSupported())`()` Indicates if forward checking is supported. |

## Protected constructors

### PKIXCertPathChecker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected PKIXCertPathChecker()
```

Default constructor.

## Public methods

### check

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun check(cert: Certificate!): Unit
```

Performs the check(s) on the specified certificate using its internal state. The certificates are presented in the order specified by the`init`method.

This implementation calls`check(cert, java.util.Collections.<String>emptySet())`.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!:the`Certificate`to be checked |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if the specified certificate does not pass the check |

### check

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun check(
    cert: Certificate!, 
    unresolvedCritExts: MutableCollection<String!>!
): Unit
```

Performs the check(s) on the specified certificate using its internal state and removes any critical extensions that it processes from the specified collection of OID strings that represent the unresolved critical extensions. The certificates are presented in the order specified by the`init`method.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cert` | [Certificate](https://developer.android.com/reference/kotlin/java/security/cert/Certificate)!:the`Certificate`to be checked |
| `unresolvedCritExts` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:a`Collection`of OID strings representing the current set of unresolved critical extensions |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if the specified certificate does not pass the check |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a clone of this object. Calls the`Object.clone()`method. All subclasses which maintain state must support and override this method, if necessary.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a copy of this`PKIXCertPathChecker` |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getSupportedExtensions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSupportedExtensions(): MutableSet<String!>!
```

Returns an immutable`Set`of X.509 certificate extensions that this`PKIXCertPathChecker`supports (i.e. recognizes, is able to process), or`null`if no extensions are supported.

Each element of the set is a`String`representing the Object Identifier (OID) of the X.509 extension that is supported. The OID is represented by a set of nonnegative integers separated by periods.

All X.509 certificate extensions that a`PKIXCertPathChecker`might possibly be able to process should be included in the set.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an immutable`Set`of X.509 extension OIDs (in`String`format) supported by this`PKIXCertPathChecker`, or`null`if no extensions are supported |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun init(forward: Boolean): Unit
```

Initializes the internal state of this`PKIXCertPathChecker`.

The`forward`flag specifies the order that certificates will be passed to the #check method (forward or reverse). A`PKIXCertPathChecker`**must** support reverse checking and**may**support forward checking.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `forward` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the order that certificates are presented to the`check`method. If`true`, certificates are presented from target to most-trusted CA (forward); if`false`, from most-trusted CA to target (reverse). |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if this`PKIXCertPathChecker`is unable to check certificates in the specified order; it should never be thrown if the forward flag is false since reverse checking must be supported |

### isForwardCheckingSupported

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isForwardCheckingSupported(): Boolean
```

Indicates if forward checking is supported. Forward checking refers to the ability of the`PKIXCertPathChecker`to perform its checks when certificates are presented to the`check`method in the forward direction (from target to most-trusted CA).

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if forward checking is supported,`false`otherwise |
