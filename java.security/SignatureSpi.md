# SignatureSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignatureSpi

```
abstract class SignatureSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.SignatureSpi](../java/security/SignatureSpi.md) |

| Known Direct Subclasses [Signature](../java/security/Signature.md) |-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------| | [Signature](../java/security/Signature.md) | The Signature class is used to provide applications the functionality of a digital signature algorithm. | |
| --- | --- | --- | --- | --- | --- | --- |

This class defines the*Service Provider Interface* (**SPI** ) for the`Signature`class, which is used to provide the functionality of a digital signature algorithm. Digital signatures are used for authentication and integrity assurance of digital data. .

All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular signature algorithm.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [SignatureSpi](../java/security/SignatureSpi.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](../java/security/SignatureSpi.md))`()` Returns a clone if the implementation is cloneable. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [engineGetParameter](../java/security/SignatureSpi.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of the specified algorithm parameter. |
| open [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | [engineGetParameters](../java/security/SignatureSpi.md))`()` This method is overridden by providers to return the parameters used with this signature engine, or null if this signature engine does not use any parameters. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSign](../java/security/SignatureSpi.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`)` Initializes this signature object with the specified private key for signing operations. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSign](../java/security/SignatureSpi.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initializes this signature object with the specified private key and source of randomness for signing operations. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitVerify](../java/security/SignatureSpi.md))`(`publicKey:` ` [PublicKey](../java/security/PublicKey.md)!`)` Initializes this signature object with the specified public key for verification operations. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetParameter](../java/security/SignatureSpi.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the specified algorithm parameter to the specified value. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetParameter](../java/security/SignatureSpi.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` This method is overridden by providers to initialize this signature engine with the specified parameter set. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineSign](../java/security/SignatureSpi.md))`()` Returns the signature bytes of all the data updated so far. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineSign](../java/security/SignatureSpi.md))`(`outbuf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finishes this signature operation and stores the resulting signature bytes in the provided buffer`outbuf`, starting at`offset`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Updates the data to be signed or verified using the specified byte. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the data to be signed or verified, using the specified array of bytes, starting at the specified offset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`input:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Updates the data to be signed or verified using the specified ByteBuffer. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineVerify](../java/security/SignatureSpi.md))`(`sigBytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Verifies the passed-in signature. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineVerify](../java/security/SignatureSpi.md))`(`sigBytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Verifies the passed-in signature in the specified array of bytes, starting at the specified offset. |

| Properties ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SecureRandom](../java/security/SecureRandom.md)! | [appRandom](../java/security/SignatureSpi.md) Application-specified source of randomness. |

## Public constructors

### SignatureSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignatureSpi()
```

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any!
```

Returns a clone if the implementation is cloneable.

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone if the implementation is cloneable. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
| `java.lang.CloneNotSupportedException` | if this is called on an implementation that does not support`Cloneable`. |

## Protected methods

### engineGetParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetParameter(param: String!): Any!
```

**Deprecated:** *Deprecated.*

Gets the value of the specified algorithm parameter. This method supplies a general-purpose mechanism through which it is possible to get the various parameters of this object. A parameter may be any settable parameter for the algorithm, such as a parameter size, or a source of random bits for signature generation (if appropriate), or an indication of whether or not to perform a specific but optional computation. A uniform algorithm-specific naming scheme for each parameter is desirable but left unspecified at this time.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `param` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string name of the parameter. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the object that represents the parameter value, or null if there is none. |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if`param`is an invalid parameter for this engine, or another exception occurs while trying to get this parameter. |

### engineGetParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetParameters(): AlgorithmParameters!
```

This method is overridden by providers to return the parameters used with this signature engine, or null if this signature engine does not use any parameters.

The returned parameters may be the same that were used to initialize this signature engine, or may contain a combination of default and randomly generated parameter values used by the underlying signature implementation if this signature engine requires algorithm parameters but was not initialized with any.

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | the parameters used with this signature engine, or null if this signature engine does not use any parameters |

| Exceptions ||
|-------------------------------------------|------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this method is not overridden by a provider |

### engineInitSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInitSign(privateKey: PrivateKey!): Unit
```

Initializes this signature object with the specified private key for signing operations.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the private key of the identity whose signature will be generated. |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the key is improperly encoded, parameters are missing, and so on. |

### engineInitSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineInitSign(
    privateKey: PrivateKey!, 
    random: SecureRandom!
): Unit
```

Initializes this signature object with the specified private key and source of randomness for signing operations.

This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.)

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the private key of the identity whose signature will be generated. |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the key is improperly encoded, parameters are missing, and so on. |

### engineInitVerify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInitVerify(publicKey: PublicKey!): Unit
```

Initializes this signature object with the specified public key for verification operations.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `publicKey` | [PublicKey](../java/security/PublicKey.md)!:the public key of the identity whose signature is going to be verified. |

| Exceptions ||
|-------------------------------------|----------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the key is improperly encoded, parameters are missing, and so on. |

### engineSetParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineSetParameter(
    param: String!, 
    value: Any!
): Unit
```

**Deprecated:** *Replaced by [engineSetParameter](../java/security/SignatureSpi.md)).*

Sets the specified algorithm parameter to the specified value. This method supplies a general-purpose mechanism through which it is possible to set the various parameters of this object. A parameter may be any settable parameter for the algorithm, such as a parameter size, or a source of random bits for signature generation (if appropriate), or an indication of whether or not to perform a specific but optional computation. A uniform algorithm-specific naming scheme for each parameter is desirable but left unspecified at this time.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string identifier of the parameter. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the parameter value. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if`param`is an invalid parameter for this signature algorithm engine, the parameter is already set and cannot be set again, a security exception occurs, and so on. |

### engineSetParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineSetParameter(params: AlgorithmParameterSpec!): Unit
```

This method is overridden by providers to initialize this signature engine with the specified parameter set.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the parameters |

| Exceptions ||
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this method is not overridden by a provider |
| `java.security.InvalidAlgorithmParameterException` | if this method is overridden by a provider and the given parameters are inappropriate for this signature engine |

### engineSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineSign(): ByteArray!
```

Returns the signature bytes of all the data updated so far. The format of the signature depends on the underlying signature scheme.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the signature bytes of the signing operation's result. |

| Exceptions ||
|------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly or if this signature algorithm is unable to process the input data provided. |

### engineSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineSign(
    outbuf: ByteArray!, 
    offset: Int, 
    len: Int
): Int
```

Finishes this signature operation and stores the resulting signature bytes in the provided buffer`outbuf`, starting at`offset`. The format of the signature depends on the underlying signature scheme.

The signature implementation is reset to its initial state (the state it was in after a call to one of the`engineInitSign`methods) and can be reused to generate further signatures with the same private key. This method should be abstract, but we leave it concrete for binary compatibility. Knowledgeable providers should override this method.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `outbuf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for the signature result. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into`outbuf`where the signature is stored. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes within`outbuf`allotted for the signature. Both this default implementation and the SUN provider do not return partial digests. If the value of this parameter is less than the actual signature length, this method will throw a SignatureException. This parameter is ignored if its value is greater than or equal to the actual signature length. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes placed into`outbuf` |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly, if this signature algorithm is unable to process the input data provided, or if`len`is less than the actual signature length. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(b: Byte): Unit
```

Updates the data to be signed or verified using the specified byte.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the byte to use for the update. |

| Exceptions ||
|------------------------------------|--------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(
    b: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the data to be signed or verified, using the specified array of bytes, starting at the specified offset.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------|
| `b` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at offset |
| --- | --- |

| Exceptions ||
|------------------------------------|-------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdate(input: ByteBuffer!): Unit
```

Updates the data to be signed or verified using the specified ByteBuffer. Processes the`data.remaining()`bytes starting at at`data.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](../java/nio/ByteBuffer.md)!:the ByteBuffer |

### engineVerify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineVerify(sigBytes: ByteArray!): Boolean
```

Verifies the passed-in signature.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `sigBytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the signature bytes to be verified. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the signature was verified, false if not. |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly, the passed-in signature is improperly encoded or of the wrong type, if this signature algorithm is unable to process the input data provided, etc. |

### engineVerify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineVerify(
    sigBytes: ByteArray!, 
    offset: Int, 
    length: Int
): Boolean
```

Verifies the passed-in signature in the specified array of bytes, starting at the specified offset.

Note: Subclasses should overwrite the default implementation.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------|
| `sigBytes` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the signature bytes to be verified. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at offset. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the signature was verified, false if not. |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if the engine is not initialized properly, the passed-in signature is improperly encoded or of the wrong type, if this signature algorithm is unable to process the input data provided, etc. |

## Properties

### appRandom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var appRandom: SecureRandom!
```

Application-specified source of randomness.
