# AlgorithmParametersSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlgorithmParametersSpi

```
abstract class AlgorithmParametersSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.AlgorithmParametersSpi](../java/security/AlgorithmParametersSpi.md) |

This class defines the*Service Provider Interface* (**SPI** ) for the`AlgorithmParameters`class, which is used to manage algorithm parameters.

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply parameter management for a particular algorithm.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AlgorithmParametersSpi](../java/security/AlgorithmParametersSpi.md))`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGetEncoded](../java/security/AlgorithmParametersSpi.md))`()` Returns the parameters in their primary encoding format. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGetEncoded](../java/security/AlgorithmParametersSpi.md))`(`format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the parameters encoded in the specified format. |
| abstractT | [engineGetParameterSpec](../java/security/AlgorithmParametersSpi.md))`(`paramSpec:` ` [Class](../java/lang/Class.md)<T>!`)` Returns a (transparent) specification of this parameters object. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../java/security/AlgorithmParametersSpi.md))`(`params:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Imports the specified parameters and decodes them according to the primary decoding format for parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../java/security/AlgorithmParametersSpi.md))`(`params:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Imports the parameters from`params`and decodes them according to the specified decoding format. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](../java/security/AlgorithmParametersSpi.md))`(`paramSpec:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` Initializes this parameters object using the parameters specified in`paramSpec`. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [engineToString](../java/security/AlgorithmParametersSpi.md))`()` Returns a formatted string describing the parameters. |

## Public constructors

### AlgorithmParametersSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AlgorithmParametersSpi()
```

## Protected methods

### engineGetEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetEncoded(): ByteArray!
```

Returns the parameters in their primary encoding format. The primary encoding format for parameters is ASN.1, if an ASN.1 specification for this type of parameters exists.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameters encoded using their primary encoding format. |

| Exceptions ||
|-----------------------|---------------------|
| `java.io.IOException` | on encoding errors. |

### engineGetEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetEncoded(format: String!): ByteArray!
```

Returns the parameters encoded in the specified format. If`format`is null, the primary encoding format for parameters is used. The primary encoding format is ASN.1, if an ASN.1 specification for these parameters exists.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the encoding format. |

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the parameters encoded using the specified encoding scheme. |

| Exceptions ||
|-----------------------|---------------------|
| `java.io.IOException` | on encoding errors. |

### engineGetParameterSpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun <T : AlgorithmParameterSpec!> engineGetParameterSpec(paramSpec: Class<T>!): T
```

Returns a (transparent) specification of this parameters object.`paramSpec`identifies the specification class in which the parameters should be returned. It could, for example, be`DSAParameterSpec.class`, to indicate that the parameters should be returned in an instance of the`DSAParameterSpec`class.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the parameter specification to be returned |
| `paramSpec` | [Class](../java/lang/Class.md)\<T\>!:the specification class in which the parameters should be returned. |

| Return ||
|---|------------------------------|
| T | the parameter specification. |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------|
| `java.security.spec.InvalidParameterSpecException` | if the requested parameter specification is inappropriate for this parameter object. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(params: ByteArray!): Unit
```

Imports the specified parameters and decodes them according to the primary decoding format for parameters. The primary decoding format for parameters is ASN.1, if an ASN.1 specification for this type of parameters exists.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------|
| `params` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded parameters. |

| Exceptions ||
|-----------------------|--------------------|
| `java.io.IOException` | on decoding errors |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    params: ByteArray!, 
    format: String!
): Unit
```

Imports the parameters from`params`and decodes them according to the specified decoding format. If`format`is null, the primary decoding format for parameters is used. The primary decoding format is ASN.1, if an ASN.1 specification for these parameters exists.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `params` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded parameters. |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the decoding format. |

| Exceptions ||
|-----------------------|--------------------|
| `java.io.IOException` | on decoding errors |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(paramSpec: AlgorithmParameterSpec!): Unit
```

Initializes this parameters object using the parameters specified in`paramSpec`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `paramSpec` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the parameter specification. |

| Exceptions ||
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.security.spec.InvalidParameterSpecException` | if the given parameter specification is inappropriate for the initialization of this parameter object. |

### engineToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineToString(): String!
```

Returns a formatted string describing the parameters.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a formatted string describing the parameters. |
