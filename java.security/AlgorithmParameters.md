# AlgorithmParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParameters

```
open class AlgorithmParameters
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParameters](AlgorithmParameters.md) |

This class is used as an opaque representation of cryptographic parameters.

An`AlgorithmParameters`object for managing the parameters for a particular algorithm can be obtained by calling one of the`getInstance`factory methods (static methods that return instances of a given class).

Once an`AlgorithmParameters`object is obtained, it must be initialized via a call to`init`, using an appropriate parameter specification or parameter encoding.

A transparent parameter specification is obtained from an`AlgorithmParameters`object via a call to`getParameterSpec`, and a byte encoding of the parameters is obtained via a call to`getEncoded`.

Android provides the following`AlgorithmParameters`algorithms:

| Algorithm | Supported API Levels |
|-----------------------------|----------------------|
| AES | 1+ |
| BLOWFISH | 10+ |
| ChaCha20 | 28+ |
| --- | --- |
| DES | 1+ |
| DESede | 1+ |
| DH | 1+ |
| --- | --- |
| DSA | 1+ |
| EC | 26+ |
| GCM | 22+ |
| --- | --- |
| IES | 1-8 |
| OAEP | 1+ |
| PBEwithHmacSHA1AndAES_128 | 26+ |
| --- | --- |
| PBEwithHmacSHA1AndAES_256 | 26+ |
| PBEwithHmacSHA224AndAES_128 | 26+ |
| PBEwithHmacSHA224AndAES_256 | 26+ |
| --- | --- |
| PBEwithHmacSHA256AndAES_128 | 26+ |
| PBEwithHmacSHA256AndAES_256 | 26+ |
| PBEwithHmacSHA384AndAES_128 | 26+ |
| --- | --- |
| PBEwithHmacSHA384AndAES_256 | 26+ |
| PBEwithHmacSHA512AndAES_128 | 26+ |
| PBEwithHmacSHA512AndAES_256 | 26+ |
| --- | --- |
| PKCS12PBE | 1+ |
| PSS | 1-8,24+ |

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlgorithmParameters](AlgorithmParameters.md))`(`paramSpi:` ` [AlgorithmParametersSpi](AlgorithmParametersSpi.md)!`, `provider:` ` [Provider](Provider.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates an AlgorithmParameters object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](AlgorithmParameters.md))`()` Returns the name of the algorithm associated with this parameter object. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](AlgorithmParameters.md))`()` Returns the parameters in their primary encoding format. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](AlgorithmParameters.md))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the parameters encoded in the specified scheme. |
| --- | --- |
| openstatic [AlgorithmParameters](AlgorithmParameters.md)! | [getInstance](AlgorithmParameters.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a parameter object for the specified algorithm. |
| openstatic [AlgorithmParameters](AlgorithmParameters.md)! | [getInstance](AlgorithmParameters.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a parameter object for the specified algorithm. |
| openstatic [AlgorithmParameters](AlgorithmParameters.md)! | [getInstance](AlgorithmParameters.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](Provider.md)!`)` Returns a parameter object for the specified algorithm. |
| --- | --- |
| T | [getParameterSpec](AlgorithmParameters.md))`(`paramSpec:` ` [Class](../java.lang/Class.md)<T>!`)` Returns a (transparent) specification of this parameter object. |
| [Provider](Provider.md)! | [getProvider](AlgorithmParameters.md))`()` Returns the provider of this parameter object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](AlgorithmParameters.md))`(`params:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Imports the specified parameters and decodes them according to the primary decoding format for parameters. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](AlgorithmParameters.md))`(`params:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Imports the parameters from`params`and decodes them according to the specified decoding scheme. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](AlgorithmParameters.md))`(`paramSpec:` ` [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!`)` Initializes this parameter object using the parameters specified in`paramSpec`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AlgorithmParameters.md))`()` Returns a formatted string describing the parameters. |
| --- | --- |

## Protected constructors

### AlgorithmParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AlgorithmParameters(
    paramSpi: AlgorithmParametersSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates an AlgorithmParameters object.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `paramSpi` | [AlgorithmParametersSpi](AlgorithmParametersSpi.md)!:the delegate |
| `provider` | [Provider](Provider.md)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |
| --- | --- |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the name of the algorithm associated with this parameter object.

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(): ByteArray!
```

Returns the parameters in their primary encoding format. The primary encoding format for parameters is ASN.1, if an ASN.1 specification for this type of parameters exists.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameters encoded using their primary encoding format. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------|
| `java.io.IOException` | on encoding errors, or if this parameter object has not been initialized. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoded(format: String!): ByteArray!
```

Returns the parameters encoded in the specified scheme. If`format`is null, the primary encoding format for parameters is used. The primary encoding format is ASN.1, if an ASN.1 specification for these parameters exists.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the encoding format. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameters encoded using the specified encoding scheme. |

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------|
| `java.io.IOException` | on encoding errors, or if this parameter object has not been initialized. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): AlgorithmParameters!
```

Returns a parameter object for the specified algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new AlgorithmParameters object encapsulating the AlgorithmParametersSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](Security.md))method.

The returned parameter object must be initialized via a call to`init`, using an appropriate parameter specification or parameter encoding.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm requested. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------|
| [AlgorithmParameters](AlgorithmParameters.md)! | the new parameter object |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no`Provider`supports an`AlgorithmParametersSpi`implementation for the specified algorithm |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): AlgorithmParameters!
```

Returns a parameter object for the specified algorithm.

A new AlgorithmParameters object encapsulating the AlgorithmParametersSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](Security.md))method.

The returned parameter object must be initialized via a call to`init`, using an appropriate parameter specification or parameter encoding.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm requested. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------|
| [AlgorithmParameters](AlgorithmParameters.md)! | the new parameter object |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider name is`null`or empty |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParametersSpi`implementation for the specified algorithm is not available from the specified provider |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list |
| --- | --- |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |

**See Also**

- [java.security.Provider](Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): AlgorithmParameters!
```

Returns a parameter object for the specified algorithm.

A new AlgorithmParameters object encapsulating the AlgorithmParametersSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

The returned parameter object must be initialized via a call to`init`, using an appropriate parameter specification or parameter encoding.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm requested. |
| `provider` | [Provider](Provider.md)!:the name of the provider. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------|
| [AlgorithmParameters](AlgorithmParameters.md)! | the new parameter object |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the provider is`null` |
| `java.security.NoSuchAlgorithmException` | if an`AlgorithmParameterGeneratorSpi`implementation for the specified algorithm is not available from the specified`Provider`object |
| `java.lang.NullPointerException` | if`algorithm`is`null`on Android 14 or above |
| --- | --- |

**See Also**

- [java.security.Provider](Provider.md) 

### getParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : AlgorithmParameterSpec!> getParameterSpec(paramSpec: Class<T>!): T
```

Returns a (transparent) specification of this parameter object.`paramSpec`identifies the specification class in which the parameters should be returned. It could, for example, be`DSAParameterSpec.class`, to indicate that the parameters should be returned in an instance of the`DSAParameterSpec`class.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the parameter specification to be returrned |
| `paramSpec` | [Class](../java.lang/Class.md)\<T\>!:the specification class in which the parameters should be returned. |

| Return ||
|---|------------------------------|
| T | the parameter specification. |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidParameterSpecException` | if the requested parameter specification is inappropriate for this parameter object, or if this parameter object has not been initialized. |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this parameter object.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Provider](Provider.md)! | the provider of this parameter object |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(params: ByteArray!): Unit
```

Imports the specified parameters and decodes them according to the primary decoding format for parameters. The primary decoding format for parameters is ASN.1, if an ASN.1 specification for this type of parameters exists.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `params` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded parameters. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------|
| `java.io.IOException` | on decoding errors, or if this parameter object has already been initialized. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    params: ByteArray!, 
    format: String!
): Unit
```

Imports the parameters from`params`and decodes them according to the specified decoding scheme. If`format`is null, the primary decoding format for parameters is used. The primary decoding format is ASN.1, if an ASN.1 specification for these parameters exists.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `params` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded parameters. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the decoding scheme. |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------------|
| `java.io.IOException` | on decoding errors, or if this parameter object has already been initialized. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(paramSpec: AlgorithmParameterSpec!): Unit
```

Initializes this parameter object using the parameters specified in`paramSpec`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `paramSpec` | [AlgorithmParameterSpec](../java.security.spec/AlgorithmParameterSpec.md)!:the parameter specification. |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidParameterSpecException` | if the given parameter specification is inappropriate for the initialization of this parameter object, or if this parameter object has already been initialized. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a formatted string describing the parameters.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a formatted string describing the parameters, or null if this parameter object has not been initialized. |
