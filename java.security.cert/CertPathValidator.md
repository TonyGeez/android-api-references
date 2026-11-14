# CertPathValidator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathValidator

```
open class CertPathValidator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#) |

A class for validating certification paths (also known as certificate chains).

This class uses a provider-based architecture. To create a`CertPathValidator`, call one of the static`getInstance`methods, passing in the algorithm name of the`CertPathValidator`desired and optionally the name of the provider desired.

Once a`CertPathValidator`object has been created, it can be used to validate certification paths by calling the [validate](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters))method and passing it the`CertPath`to be validated and an algorithm-specific set of parameters. If successful, the result is returned in an object that implements the`CertPathValidatorResult`interface.

The [getRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getRevocationChecker())method allows an application to specify additional algorithm-specific parameters and options used by the`CertPathValidator`when checking the revocation status of certificates. Here is an example demonstrating how it is used with the PKIX algorithm: 

```kotlin
CertPathValidator cpv = CertPathValidator.getInstance("PKIX");
  PKIXRevocationChecker rc = (PKIXRevocationChecker)cpv.getRevocationChecker();
  rc.setOptions(EnumSet.of(Option.SOFT_FAIL));
  params.addCertPathChecker(rc);
  CertPathValidatorResult cpvr = cpv.validate(path, params);
  
```

Every implementation of the Java platform is required to support the following standard`CertPathValidator`algorithm:

- `PKIX`

This algorithm is described in the [CertPathValidator section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathvalidator-algorithms) of the Java Security Standard Algorithm Names Specification. Consult the release documentation for your implementation to see if any other algorithms are supported.

**Concurrent Access**

The static methods of this class are guaranteed to be thread-safe. Multiple threads may concurrently invoke the static methods defined in this class with no ill effects.

However, this is not true for the non-static methods defined by this class. Unless otherwise documented by a specific provider, threads that need to access a single`CertPathValidator`instance concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating a different`CertPathValidator`instance need not synchronize.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#CertPathValidator(java.security.cert.CertPathValidatorSpi,%20java.security.Provider,%20kotlin.String))`(`validatorSpi:` ` [CertPathValidatorSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CertPathValidator`object of the given algorithm, and encapsulates the given provider implementation (SPI object) in it. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getAlgorithm())`()` Returns the algorithm name of this`CertPathValidator`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultType](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getDefaultType())`()` Returns the default`CertPathValidator`type as specified by the`certpathvalidator.type`security property, or the string "PKIX" if no such property exists. |
| openstatic [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`CertPathValidator`object that implements the specified algorithm. |
| --- | --- |
| openstatic [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`CertPathValidator`object that implements the specified algorithm. |
| openstatic [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`CertPathValidator`object that implements the specified algorithm. |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getProvider())`()` Returns the`Provider`of this`CertPathValidator`. |
| --- | --- |
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | [getRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#getRevocationChecker())`()` Returns a`CertPathChecker`that the encapsulated`CertPathValidatorSpi`implementation uses to check the revocation status of certificates. |
| [CertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult)! | [validate](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#validate(java.security.cert.CertPath,%20java.security.cert.CertPathParameters))`(`certPath:` ` [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!`, `params:` ` [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!`)` Validates the specified certification path using the specified algorithm parameter set. |

## Protected constructors

### CertPathValidator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CertPathValidator(
    validatorSpi: CertPathValidatorSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a`CertPathValidator`object of the given algorithm, and encapsulates the given provider implementation (SPI object) in it.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `validatorSpi` | [CertPathValidatorSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorSpi)!:the provider implementation |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name |
| --- | --- |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`CertPathValidator`.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`CertPathValidator` |

### getDefaultType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultType(): String!
```

Returns the default`CertPathValidator`type as specified by the`certpathvalidator.type`security property, or the string "PKIX" if no such property exists.

The default`CertPathValidator`type can be used by applications that do not want to use a hard-coded type when calling one of the`getInstance`methods, and want to provide a default type in case a user does not specify its own.

The default`CertPathValidator`type can be changed by setting the value of the`certpathvalidator.type`security property to the desired type.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default`CertPathValidator`type as specified by the`certpathvalidator.type`security property, or the string "PKIX" if no such property exists. |

**See Also**

- [java.security.Security](https://developer.android.com/reference/kotlin/java/security/Security.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): CertPathValidator!
```

Returns a`CertPathValidator`object that implements the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new CertPathValidator object encapsulating the CertPathValidatorSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathValidator`algorithm. See the CertPathValidator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathvalidator-algorithms) for information about standard algorithm names. |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | a`CertPathValidator`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`CertPathValidatorSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): CertPathValidator!
```

Returns a`CertPathValidator`object that implements the specified algorithm.

A new CertPathValidator object encapsulating the CertPathValidatorSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathValidator`algorithm. See the CertPathValidator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathvalidator-algorithms) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | a`CertPathValidator`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if a`CertPathValidatorSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): CertPathValidator!
```

Returns a`CertPathValidator`object that implements the specified algorithm.

A new CertPathValidator object encapsulating the CertPathValidatorSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathValidator`algorithm. See the CertPathValidator section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathvalidator-algorithms) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider. |

| Return ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [CertPathValidator](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidator#)! | a`CertPathValidator`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is`null` |
| `java.security.NoSuchAlgorithmException` | if a`CertPathValidatorSpi`implementation for the specified algorithm is not available from the specified Provider object |
| `java.lang.NullPointerException` | if`algorithm`is`null` |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the`Provider`of this`CertPathValidator`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the`Provider`of this`CertPathValidator` |

### getRevocationChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRevocationChecker(): CertPathChecker!
```

Returns a`CertPathChecker`that the encapsulated`CertPathValidatorSpi`implementation uses to check the revocation status of certificates. A PKIX implementation returns objects of type`PKIXRevocationChecker`. Each invocation of this method returns a new instance of`CertPathChecker`.

The primary purpose of this method is to allow callers to specify additional input parameters and options specific to revocation checking. See the class description for an example.

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------|
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | a`CertPathChecker` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the service provider does not support this method |

### validate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun validate(
    certPath: CertPath!, 
    params: CertPathParameters!
): CertPathValidatorResult!
```

Validates the specified certification path using the specified algorithm parameter set.

The`CertPath`specified must be of a type that is supported by the validation algorithm, otherwise an`InvalidAlgorithmParameterException`will be thrown. For example, a`CertPathValidator`that implements the PKIX algorithm validates`CertPath`objects of type X.509.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `certPath` | [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!:the`CertPath`to be validated |
| `params` | [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!:the algorithm parameters |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [CertPathValidatorResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorResult)! | the result of the validation algorithm |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.security.cert.CertPathValidatorException` | if the`CertPath`does not validate |
| `java.security.InvalidAlgorithmParameterException` | if the specified parameters or the type of the specified`CertPath`are inappropriate for this`CertPathValidator` |
