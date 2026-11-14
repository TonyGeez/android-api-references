# CertPathBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathBuilder

```
open class CertPathBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.cert.CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#) |

A class for building certification paths (also known as certificate chains).

This class uses a provider-based architecture. To create a`CertPathBuilder`, call one of the static`getInstance`methods, passing in the algorithm name of the`CertPathBuilder`desired and optionally the name of the provider desired.

Once a`CertPathBuilder`object has been created, certification paths can be constructed by calling the [build](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#build(java.security.cert.CertPathParameters))method and passing it an algorithm-specific set of parameters. If successful, the result (including the`CertPath`that was built) is returned in an object that implements the`CertPathBuilderResult`interface.

The [getRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getRevocationChecker())method allows an application to specify additional algorithm-specific parameters and options used by the`CertPathBuilder`when checking the revocation status of certificates. Here is an example demonstrating how it is used with the PKIX algorithm: 

```kotlin
CertPathBuilder cpb = CertPathBuilder.getInstance("PKIX");
  PKIXRevocationChecker rc = (PKIXRevocationChecker)cpb.getRevocationChecker();
  rc.setOptions(EnumSet.of(Option.PREFER_CRLS));
  params.addCertPathChecker(rc);
  CertPathBuilderResult cpbr = cpb.build(params);
  
```

Every implementation of the Java platform is required to support the following standard`CertPathBuilder`algorithm:

- `PKIX`

This algorithm is described in the [CertPathBuilder section](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathbuilder-algorithms) of the Java Security Standard Algorithm Names Specification. Consult the release documentation for your implementation to see if any other algorithms are supported.

**Concurrent Access**

The static methods of this class are guaranteed to be thread-safe. Multiple threads may concurrently invoke the static methods defined in this class with no ill effects.

However, this is not true for the non-static methods defined by this class. Unless otherwise documented by a specific provider, threads that need to access a single`CertPathBuilder`instance concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating a different`CertPathBuilder`instance need not synchronize.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#CertPathBuilder(java.security.cert.CertPathBuilderSpi,%20java.security.Provider,%20kotlin.String))`(`builderSpi:` ` [CertPathBuilderSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`CertPathBuilder`object of the given algorithm, and encapsulates the given provider implementation (SPI object) in it. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderResult)! | [build](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#build(java.security.cert.CertPathParameters))`(`params:` ` [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!`)` Attempts to build a certification path using the specified algorithm parameter set. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getAlgorithm())`()` Returns the name of the algorithm of this`CertPathBuilder`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDefaultType](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getDefaultType())`()` Returns the default`CertPathBuilder`type as specified by the`certpathbuilder.type`security property, or the string "PKIX" if no such property exists. |
| --- | --- |
| openstatic [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getInstance(kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`CertPathBuilder`object that implements the specified algorithm. |
| openstatic [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getInstance(kotlin.String,%20kotlin.String))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`CertPathBuilder`object that implements the specified algorithm. |
| openstatic [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | [getInstance](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getInstance(kotlin.String,%20java.security.Provider))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Returns a`CertPathBuilder`object that implements the specified algorithm. |
| --- | --- |
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | [getProvider](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getProvider())`()` Returns the provider of this`CertPathBuilder`. |
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | [getRevocationChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#getRevocationChecker())`()` Returns a`CertPathChecker`that the encapsulated`CertPathBuilderSpi`implementation uses to check the revocation status of certificates. |

## Protected constructors

### CertPathBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected CertPathBuilder(
    builderSpi: CertPathBuilderSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a`CertPathBuilder`object of the given algorithm, and encapsulates the given provider implementation (SPI object) in it.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `builderSpi` | [CertPathBuilderSpi](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderSpi)!:the provider implementation |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name |
| --- | --- |

## Public methods

### build

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun build(params: CertPathParameters!): CertPathBuilderResult!
```

Attempts to build a certification path using the specified algorithm parameter set.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [CertPathParameters](https://developer.android.com/reference/kotlin/java/security/cert/CertPathParameters)!:the algorithm parameters |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| [CertPathBuilderResult](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilderResult)! | the result of the build algorithm |

| Exceptions ||
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.security.cert.CertPathBuilderException` | if the builder is unable to construct a certification path that satisfies the specified parameters |
| `java.security.InvalidAlgorithmParameterException` | if the specified parameters are inappropriate for this`CertPathBuilder` |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the name of the algorithm of this`CertPathBuilder`.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the algorithm of this`CertPathBuilder` |

### getDefaultType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getDefaultType(): String!
```

Returns the default`CertPathBuilder`type as specified by the`certpathbuilder.type`security property, or the string "PKIX" if no such property exists.

The default`CertPathBuilder`type can be used by applications that do not want to use a hard-coded type when calling one of the`getInstance`methods, and want to provide a default type in case a user does not specify its own.

The default`CertPathBuilder`type can be changed by setting the value of the`certpathbuilder.type`security property to the desired type.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the default`CertPathBuilder`type as specified by the`certpathbuilder.type`security property, or the string "PKIX" if no such property exists. |

**See Also**

- [java.security.Security](https://developer.android.com/reference/kotlin/java/security/Security.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): CertPathBuilder!
```

Returns a`CertPathBuilder`object that implements the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new CertPathBuilder object encapsulating the CertPathBuilderSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathBuilder`algorithm. See the CertPathBuilder section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathbuilder-algorithms) for information about standard algorithm names. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | a`CertPathBuilder`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|-----------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports a`CertPathBuilderSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null` |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): CertPathBuilder!
```

Returns a`CertPathBuilder`object that implements the specified algorithm.

A new CertPathBuilder object encapsulating the CertPathBuilderSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](https://developer.android.com/reference/kotlin/java/security/Security.html#getProviders())method.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathBuilder`algorithm. See the CertPathBuilder section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathbuilder-algorithms) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | a`CertPathBuilder`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if a`CertPathBuilderSpi`implementation for the specified algorithm is not available from the specified provider |
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
): CertPathBuilder!
```

Returns a`CertPathBuilder`object that implements the specified algorithm.

A new CertPathBuilder object encapsulating the CertPathBuilderSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the requested`CertPathBuilder`algorithm. See the CertPathBuilder section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#certpathbuilder-algorithms) for information about standard algorithm names. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the provider. |

| Return ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [CertPathBuilder](https://developer.android.com/reference/kotlin/java/security/cert/CertPathBuilder#)! | a`CertPathBuilder`object that implements the specified algorithm |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`provider`is`null` |
| `java.security.NoSuchAlgorithmException` | if a`CertPathBuilderSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null` |
| --- | --- |

**See Also**

- [java.security.Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`CertPathBuilder`.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------|
| [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)! | the provider of this`CertPathBuilder` |

### getRevocationChecker

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRevocationChecker(): CertPathChecker!
```

Returns a`CertPathChecker`that the encapsulated`CertPathBuilderSpi`implementation uses to check the revocation status of certificates. A PKIX implementation returns objects of type`PKIXRevocationChecker`. Each invocation of this method returns a new instance of`CertPathChecker`.

The primary purpose of this method is to allow callers to specify additional input parameters and options specific to revocation checking. See the class description for an example.

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------------|
| [CertPathChecker](https://developer.android.com/reference/kotlin/java/security/cert/CertPathChecker)! | a`CertPathChecker` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the service provider does not support this method |
