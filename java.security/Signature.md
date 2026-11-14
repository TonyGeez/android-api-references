# Signature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Signature

```
abstract class Signature : SignatureSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.SignatureSpi](../java/security/SignatureSpi.md) ||
| | ↳ | [java.security.Signature](../java/security/Signature.md) |

The Signature class is used to provide applications the functionality of a digital signature algorithm. Digital signatures are used for authentication and integrity assurance of digital data.

The signature algorithm can be, among others, the NIST standard DSA, using DSA and SHA-1. The DSA algorithm using the SHA-1 message digest algorithm can be specified as`SHA1withDSA`. In the case of RSA, there are multiple choices for the message digest algorithm, so the signing algorithm could be specified as, for example,`MD2withRSA`,`MD5withRSA`, or`SHA1withRSA`. The algorithm name must be specified, as there is no default.

A Signature object can be used to generate and verify digital signatures.

There are three phases to the use of a Signature object for either signing data or verifying a signature:

1. Initialization, with either
 - a public key, which initializes the signature for verification (see [initVerify](../java/security/Signature.md))), or
 - a private key (and optionally a Secure Random Number Generator), which initializes the signature for signing (see [initSign(java.security.PrivateKey)](../java/security/Signature.md))and [initSign(java.security.PrivateKey,java.security.SecureRandom)](../java/security/Signature.md))).
2. UpdatingDepending on the type of initialization, this will update the bytes to be signed or verified. See the [update](../java/security/Signature.md))methods.

3. Signing or Verifying a signature on all updated bytes. See the [sign](../java/security/Signature.md))methods and the [verify](../java/security/Signature.md))method.

Note that this class is abstract and extends from`SignatureSpi`for historical reasons. Application developers should only take notice of the methods defined in this`Signature`class; all the methods in the superclass are intended for cryptographic service providers who wish to supply their own implementations of digital signature algorithms.

Android provides the following`Signature`algorithms:

| Algorithm | Supported API Levels |
|-----------------------|----------------------|
| DSA | 1+ |
| DSAwithSHA1 | 1+ |
| DSS | 1-19 |
| --- | --- |
| ECDSA | 11+ |
| ECDSAwithSHA1 | 11+ |
| Ed25519 | 33+ |
| --- | --- |
| MD2withRSA | 1-3 |
| MD4withRSA | 1-8 |
| MD5withRSA | 1+ |
| --- | --- |
| MD5withRSA/ISO9796-2 | 1-8 |
| NONEwithDSA | 1+ |
| NONEwithECDSA | 11+ |
| --- | --- |
| NONEwithRSA | 17+ |
| RSASSA-PSS | 1-8 |
| SHA1withDSA | 1+ |
| --- | --- |
| SHA1withECDSA | 11+ |
| SHA1withRSA | 1+ |
| SHA1withRSA/ISO9796-2 | 1-8 |
| --- | --- |
| SHA1withRSA/PSS | 23+ |
| SHA224withDSA | 20+ |
| SHA224withECDSA | 20+ |
| --- | --- |
| SHA224withRSA | 20+ |
| SHA224withRSA/PSS | 23+ |
| SHA256withDSA | 1+ |
| --- | --- |
| SHA256withECDSA | 11+ |
| SHA256withRSA | 1+ |
| SHA256withRSA/PSS | 23+ |
| --- | --- |
| SHA384withECDSA | 11+ |
| SHA384withRSA | 1+ |
| SHA384withRSA/PSS | 23+ |
| --- | --- |
| SHA512withECDSA | 11+ |
| SHA512withRSA | 1+ |
| SHA512withRSA/PSS | 23+ |
| --- | --- |

These algorithms are described in the [Signature section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Signature) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGN](../java/security/Signature.md) Possible [state](../java/security/Signature.md) value, signifying that this signature object has been initialized for signing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNINITIALIZED](../java/security/Signature.md) Possible [state](../java/security/Signature.md) value, signifying that this signature object has not yet been initialized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VERIFY](../java/security/Signature.md) Possible [state](../java/security/Signature.md) value, signifying that this signature object has been initialized for verification. |
| --- | --- |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Signature](../java/security/Signature.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a Signature object for the specified algorithm. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](../java/security/Signature.md))`()` Returns a clone if the implementation is cloneable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/Signature.md))`()` Returns the name of the algorithm for this signature object. |
| openstatic [Signature](../java/security/Signature.md)! | [getInstance](../java/security/Signature.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a Signature object that implements the specified signature algorithm. |
| --- | --- |
| openstatic [Signature](../java/security/Signature.md)! | [getInstance](../java/security/Signature.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a Signature object that implements the specified signature algorithm. |
| openstatic [Signature](../java/security/Signature.md)! | [getInstance](../java/security/Signature.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` Returns a Signature object that implements the specified signature algorithm. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getParameter](../java/security/Signature.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Gets the value of the specified algorithm parameter. |
| --- | --- |
| [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | [getParameters](../java/security/Signature.md))`()` Returns the parameters used with this signature object. |
| [Provider](../java/security/Provider.md)! | [getProvider](../java/security/Signature.md))`()` Returns the provider of this signature object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initSign](../java/security/Signature.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`)` Initialize this object for signing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initSign](../java/security/Signature.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` Initialize this object for signing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initVerify](../java/security/Signature.md))`(`certificate:` ` [Certificate](../java/security/cert/Certificate.md)!`)` Initializes this object for verification, using the public key from the given certificate. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initVerify](../java/security/Signature.md))`(`publicKey:` ` [PublicKey](../java/security/PublicKey.md)!`)` Initializes this object for verification. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameter](../java/security/Signature.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the specified algorithm parameter to the specified value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameter](../java/security/Signature.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` Initializes this signature engine with the specified parameter set. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [sign](../java/security/Signature.md))`()` Returns the signature bytes of all the data updated. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sign](../java/security/Signature.md))`(`outbuf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finishes the signature operation and stores the resulting signature bytes in the provided buffer`outbuf`, starting at`offset`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/Signature.md))`()` Returns a string representation of this signature object, providing information that includes the state of the object and the name of the algorithm used. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/security/Signature.md))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Updates the data to be signed or verified by a byte. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/security/Signature.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Updates the data to be signed or verified, using the specified array of bytes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/security/Signature.md))`(`data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Updates the data to be signed or verified, using the specified array of bytes, starting at the specified offset. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../java/security/Signature.md))`(`data:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Updates the data to be signed or verified using the specified ByteBuffer. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](../java/security/Signature.md))`(`signature:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Verifies the passed-in signature. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](../java/security/Signature.md))`(`signature:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Verifies the passed-in signature in the specified array of bytes, starting at the specified offset. |

| Inherited functions ||
|---|---|
| From class [SignatureSpi](../java/security/SignatureSpi.md) |----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [engineGetParameter](../java/security/SignatureSpi.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Gets the value of the specified algorithm parameter. This method supplies a general-purpose mechanism through which it is possible to get the various parameters of this object. A parameter may be any settable parameter for the algorithm, such as a parameter size, or a source of random bits for signature generation (if appropriate), or an indication of whether or not to perform a specific but optional computation. A uniform algorithm-specific naming scheme for each parameter is desirable but left unspecified at this time. <br /> | | [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | [engineGetParameters](../java/security/SignatureSpi.md))`()` <br /> This method is overridden by providers to return the parameters used with this signature engine, or null if this signature engine does not use any parameters. The returned parameters may be the same that were used to initialize this signature engine, or may contain a combination of default and randomly generated parameter values used by the underlying signature implementation if this signature engine requires algorithm parameters but was not initialized with any. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSign](../java/security/SignatureSpi.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`)` <br /> Initializes this signature object with the specified private key for signing operations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitSign](../java/security/SignatureSpi.md))`(`privateKey:` ` [PrivateKey](../java/security/PrivateKey.md)!`, `random:` ` [SecureRandom](../java/security/SecureRandom.md)!`)` <br /> Initializes this signature object with the specified private key and source of randomness for signing operations. This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInitVerify](../java/security/SignatureSpi.md))`(`publicKey:` ` [PublicKey](../java/security/PublicKey.md)!`)` <br /> Initializes this signature object with the specified public key for verification operations. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetParameter](../java/security/SignatureSpi.md))`(`param:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the specified algorithm parameter to the specified value. This method supplies a general-purpose mechanism through which it is possible to set the various parameters of this object. A parameter may be any settable parameter for the algorithm, such as a parameter size, or a source of random bits for signature generation (if appropriate), or an indication of whether or not to perform a specific but optional computation. A uniform algorithm-specific naming scheme for each parameter is desirable but left unspecified at this time. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetParameter](../java/security/SignatureSpi.md))`(`params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` <br /> This method is overridden by providers to initialize this signature engine with the specified parameter set. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineSign](../java/security/SignatureSpi.md))`()` <br /> Returns the signature bytes of all the data updated so far. The format of the signature depends on the underlying signature scheme. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineSign](../java/security/SignatureSpi.md))`(`outbuf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Finishes this signature operation and stores the resulting signature bytes in the provided buffer`outbuf`, starting at`offset`. The format of the signature depends on the underlying signature scheme. The signature implementation is reset to its initial state (the state it was in after a call to one of the`engineInitSign`methods) and can be reused to generate further signatures with the same private key. This method should be abstract, but we leave it concrete for binary compatibility. Knowledgeable providers should override this method. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` <br /> Updates the data to be signed or verified using the specified byte. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`b:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Updates the data to be signed or verified, using the specified array of bytes, starting at the specified offset. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdate](../java/security/SignatureSpi.md))`(`input:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` <br /> Updates the data to be signed or verified using the specified ByteBuffer. Processes the`data.remaining()`bytes starting at at`data.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineVerify](../java/security/SignatureSpi.md))`(`sigBytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Verifies the passed-in signature. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineVerify](../java/security/SignatureSpi.md))`(`sigBytes:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Verifies the passed-in signature in the specified array of bytes, starting at the specified offset. Note: Subclasses should overwrite the default implementation. <br /> | ||

| Properties ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [state](../java/security/Signature.md) Current state of this signature object. |

| Inherited properties ||
|---|---|
| From class [SignatureSpi](../java/security/SignatureSpi.md) |--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SecureRandom](../java/security/SecureRandom.md)! | [appRandom](../java/security/SignatureSpi.md) <br /> Application-specified source of randomness. <br /> | ||

## Constants

### SIGN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val SIGN: Int
```

Possible [state](../java/security/Signature.md) value, signifying that this signature object has been initialized for signing. 

 Value: 2

### UNINITIALIZED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val UNINITIALIZED: Int
```

Possible [state](../java/security/Signature.md) value, signifying that this signature object has not yet been initialized. 

 Value: 0

### VERIFY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected static val VERIFY: Int
```

Possible [state](../java/security/Signature.md) value, signifying that this signature object has been initialized for verification. 

 Value: 3

## Protected constructors

### Signature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Signature(algorithm: String!)
```

Creates a Signature object for the specified algorithm.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard string name of the algorithm. See the Signature section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Signature) for information about standard algorithm names. |

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

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the name of the algorithm for this signature object.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of the algorithm for this signature object. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(algorithm: String!): Signature!
```

Returns a Signature object that implements the specified signature algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new Signature object encapsulating the SignatureSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the algorithm requested. See the Signature section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Signature) for information about standard algorithm names. |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------|
| [Signature](../java/security/Signature.md)! | the new Signature object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a Signature implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: String!
): Signature!
```

Returns a Signature object that implements the specified signature algorithm.

A new Signature object encapsulating the SignatureSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm requested. See the Signature section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Signature) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------|
| [Signature](../java/security/Signature.md)! | the new Signature object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SignatureSpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the provider name is null or empty. |
| --- | --- |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): Signature!
```

Returns a Signature object that implements the specified signature algorithm.

A new Signature object encapsulating the SignatureSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the algorithm requested. See the Signature section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Signature) for information about standard algorithm names. |
| `provider` | [Provider](../java/security/Provider.md)!:the provider. |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------|
| [Signature](../java/security/Signature.md)! | the new Signature object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a SignatureSpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the provider is null. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameter(param: String!): Any!
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

**See Also**

- [#setParameter(String, Object)](../java/security/Signature.md)) 

### getParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameters(): AlgorithmParameters!
```

Returns the parameters used with this signature object.

The returned parameters may be the same that were used to initialize this signature, or may contain a combination of default and randomly generated parameter values used by the underlying signature implementation if this signature requires algorithm parameters but was not initialized with any.

| Return ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [AlgorithmParameters](../java/security/AlgorithmParameters.md)! | the parameters used with this signature, or null if this signature does not use any parameters. |

**See Also**

- [#setParameter(AlgorithmParameterSpec)](../java/security/Signature.md)) 

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this signature object.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Provider](../java/security/Provider.md)! | the provider of this signature object |

### initSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initSign(privateKey: PrivateKey!): Unit
```

Initialize this object for signing. If this method is called again with a different argument, it negates the effect of this call.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the private key of the identity whose signature is going to be generated. |

| Exceptions ||
|-------------------------------------|------------------------|
| `java.security.InvalidKeyException` | if the key is invalid. |

### initSign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initSign(
    privateKey: PrivateKey!, 
    random: SecureRandom!
): Unit
```

Initialize this object for signing. If this method is called again with a different argument, it negates the effect of this call.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `privateKey` | [PrivateKey](../java/security/PrivateKey.md)!:the private key of the identity whose signature is going to be generated. |
| `random` | [SecureRandom](../java/security/SecureRandom.md)!:the source of randomness for this signature. |

| Exceptions ||
|-------------------------------------|------------------------|
| `java.security.InvalidKeyException` | if the key is invalid. |

### initVerify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initVerify(certificate: Certificate!): Unit
```

Initializes this object for verification, using the public key from the given certificate.

If the certificate is of type X.509 and has a*key usage* extension field marked as critical, and the value of the*key usage* extension field implies that the public key in the certificate and its corresponding private key are not supposed to be used for digital signatures, an`InvalidKeyException`is thrown.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [Certificate](../java/security/cert/Certificate.md)!:the certificate of the identity whose signature is going to be verified. |

| Exceptions ||
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the public key in the certificate is not encoded properly or does not include required parameter information or cannot be used for digital signature purposes. |

### initVerify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun initVerify(publicKey: PublicKey!): Unit
```

Initializes this object for verification. If this method is called again with a different argument, it negates the effect of this call.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `publicKey` | [PublicKey](../java/security/PublicKey.md)!:the public key of the identity whose signature is going to be verified. |

| Exceptions ||
|-------------------------------------|------------------------|
| `java.security.InvalidKeyException` | if the key is invalid. |

### setParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setParameter(
    param: String!, 
    value: Any!
): Unit
```

**Deprecated:** *Use [setParameter](../java/security/Signature.md)).*

Sets the specified algorithm parameter to the specified value. This method supplies a general-purpose mechanism through which it is possible to set the various parameters of this object. A parameter may be any settable parameter for the algorithm, such as a parameter size, or a source of random bits for signature generation (if appropriate), or an indication of whether or not to perform a specific but optional computation. A uniform algorithm-specific naming scheme for each parameter is desirable but left unspecified at this time.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `param` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the string identifier of the parameter. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the parameter value. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if`param`is an invalid parameter for this signature algorithm engine, the parameter is already set and cannot be set again, a security exception occurs, and so on. |

**See Also**

- [#getParameter](../java/security/Signature.md)) 

### setParameter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setParameter(params: AlgorithmParameterSpec!): Unit
```

Initializes this signature engine with the specified parameter set.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the parameters |

| Exceptions ||
|----------------------------------------------------|---------------------------------------------------------------------|
| `java.security.InvalidAlgorithmParameterException` | if the given parameters are inappropriate for this signature engine |

**See Also**

- [#getParameters](../java/security/Signature.md)) 

### sign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sign(): ByteArray!
```

Returns the signature bytes of all the data updated. The format of the signature depends on the underlying signature scheme.

A call to this method resets this signature object to the state it was in when previously initialized for signing via a call to`initSign(PrivateKey)`. That is, the object is reset and available to generate another signature from the same signer, if desired, via new calls to`update`and`sign`.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the signature bytes of the signing operation's result. |

| Exceptions ||
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly or if this signature algorithm is unable to process the input data provided. |

### sign

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sign(
    outbuf: ByteArray!, 
    offset: Int, 
    len: Int
): Int
```

Finishes the signature operation and stores the resulting signature bytes in the provided buffer`outbuf`, starting at`offset`. The format of the signature depends on the underlying signature scheme.

This signature object is reset to its initial state (the state it was in after a call to one of the`initSign`methods) and can be reused to generate further signatures with the same private key.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `outbuf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for the signature result. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):offset into`outbuf`where the signature is stored. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes within`outbuf`allotted for the signature. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes placed into`outbuf`. |

| Exceptions ||
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly, if this signature algorithm is unable to process the input data provided, or if`len`is less than the actual signature length. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of this signature object, providing information that includes the state of the object and the name of the algorithm used.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this signature object. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(b: Byte): Unit
```

Updates the data to be signed or verified by a byte.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------|
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the byte to use for the update. |

| Exceptions ||
|------------------------------------|-------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(data: ByteArray!): Unit
```

Updates the data to be signed or verified, using the specified array of bytes.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the byte array to use for the update. |

| Exceptions ||
|------------------------------------|-------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    data: ByteArray!, 
    off: Int, 
    len: Int
): Unit
```

Updates the data to be signed or verified, using the specified array of bytes, starting at the specified offset.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at offset. |
| --- | --- |

| Exceptions ||
|------------------------------------|-------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(data: ByteBuffer!): Unit
```

Updates the data to be signed or verified using the specified ByteBuffer. Processes the`data.remaining()`bytes starting at at`data.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------|
| `data` | [ByteBuffer](../java/nio/ByteBuffer.md)!:the ByteBuffer |

| Exceptions ||
|------------------------------------|-------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(signature: ByteArray!): Boolean
```

Verifies the passed-in signature.

A call to this method resets this signature object to the state it was in when previously initialized for verification via a call to`initVerify(PublicKey)`. That is, the object is reset and available to verify another signature from the identity whose public key was specified in the call to`initVerify`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `signature` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the signature bytes to be verified. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the signature was verified, false if not. |

| Exceptions ||
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly, the passed-in signature is improperly encoded or of the wrong type, if this signature algorithm is unable to process the input data provided, etc. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    signature: ByteArray!, 
    offset: Int, 
    length: Int
): Boolean
```

Verifies the passed-in signature in the specified array of bytes, starting at the specified offset.

A call to this method resets this signature object to the state it was in when previously initialized for verification via a call to`initVerify(PublicKey)`. That is, the object is reset and available to verify another signature from the identity whose public key was specified in the call to`initVerify`.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------|
| `signature` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the signature bytes to be verified. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset to start from in the array of bytes. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to use, starting at offset. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the signature was verified, false if not. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.SignatureException` | if this signature object is not initialized properly, the passed-in signature is improperly encoded or of the wrong type, if this signature algorithm is unable to process the input data provided, etc. |
| `java.lang.IllegalArgumentException` | if the`signature`byte array is null, or the`offset`or`length`is less than 0, or the sum of the`offset`and`length`is greater than the length of the`signature`byte array. |

## Properties

### state

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var state: Int
```

Current state of this signature object.
