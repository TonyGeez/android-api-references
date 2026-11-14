# Mac

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Mac

```
open class Mac : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.Mac](../javax/crypto/Mac.md) |

This class provides the functionality of a "Message Authentication Code" (MAC) algorithm.

A MAC provides a way to check the integrity of information transmitted over or stored in an unreliable medium, based on a secret key. Typically, message authentication codes are used between two parties that share a secret key in order to validate information transmitted between these parties.

A MAC mechanism that is based on cryptographic hash functions is referred to as HMAC. HMAC can be used with any cryptographic hash function, e.g., MD5 or SHA-1, in combination with a secret shared key. HMAC is specified in RFC 2104.

Android provides the following`Mac`algorithms:

| Algorithm | Supported API Levels |
|-------------------|----------------------|
| AESCMAC | 31+ |
| DESMAC | 1-8 |
| DESMAC/CFB8 | 1-8 |
| --- | --- |
| DESedeMAC | 1-8 |
| DESedeMAC/CFB8 | 1-8 |
| DESedeMAC64 | 1-8 |
| --- | --- |
| DESwithISO9797 | 1-8 |
| HmacMD5 | 1+ |
| HmacSHA1 | 1+ |
| --- | --- |
| HmacSHA224 | 1-8,22+ |
| HmacSHA256 | 1+ |
| HmacSHA384 | 1+ |
| --- | --- |
| HmacSHA512 | 1+ |
| ISO9797ALG3MAC | 1-8 |
| PBEwithHmacSHA | 1+ |
| --- | --- |
| PBEwithHmacSHA1 | 1+ |
| PBEwithHmacSHA224 | 26-31 |
| PBEwithHmacSHA256 | 26-31 |
| --- | --- |
| PBEwithHmacSHA384 | 26-31 |
| PBEwithHmacSHA512 | 26-31 |

These algorithms are described in the [Mac section](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Mac) of the Java Cryptography Architecture Standard Algorithm Name Documentation.

## Summary

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Mac](../javax/crypto/Mac.md))`(`macSpi:` ` [MacSpi](../javax/crypto/MacSpi.md)!`, `provider:` ` [Provider](../java/security/Provider.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a MAC object. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../javax/crypto/Mac.md))`()` Returns a clone if the provider implementation is cloneable. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [doFinal](../javax/crypto/Mac.md))`()` Finishes the MAC operation. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [doFinal](../javax/crypto/Mac.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Processes the given array of bytes and finishes the MAC operation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [doFinal](../javax/crypto/Mac.md))`(`output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `outOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finishes the MAC operation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../javax/crypto/Mac.md))`()` Returns the algorithm name of this`Mac`object. |
| static [Mac](../javax/crypto/Mac.md)! | [getInstance](../javax/crypto/Mac.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`Mac`object that implements the specified MAC algorithm. |
| --- | --- |
| static [Mac](../javax/crypto/Mac.md)! | [getInstance](../javax/crypto/Mac.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns a`Mac`object that implements the specified MAC algorithm. |
| static [Mac](../javax/crypto/Mac.md)! | [getInstance](../javax/crypto/Mac.md))`(`algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `provider:` ` [Provider](../java/security/Provider.md)!`)` Returns a`Mac`object that implements the specified MAC algorithm. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMacLength](../javax/crypto/Mac.md))`()` Returns the length of the MAC in bytes. |
| --- | --- |
| [Provider](../java/security/Provider.md)! | [getProvider](../javax/crypto/Mac.md))`()` Returns the provider of this`Mac`object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../javax/crypto/Mac.md))`(`key:` ` [Key](../java/security/Key.md)!`)` Initializes this`Mac`object with the given key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [init](../javax/crypto/Mac.md))`(`key:` ` [Key](../java/security/Key.md)!`, `params:` ` [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!`)` Initializes this`Mac`object with the given key and algorithm parameters. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](../javax/crypto/Mac.md))`()` Resets this`Mac`object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../javax/crypto/Mac.md))`(`input:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Processes the given byte. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../javax/crypto/Mac.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Processes the given array of bytes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../javax/crypto/Mac.md))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Processes the first`len`bytes in`input`, starting at`offset`inclusive. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [update](../javax/crypto/Mac.md))`(`input:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Processes`input.remaining()`bytes in the ByteBuffer`input`, starting at`input.position()`. |

## Protected constructors

### Mac

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Mac(
    macSpi: MacSpi!, 
    provider: Provider!, 
    algorithm: String!)
```

Creates a MAC object.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------|
| `macSpi` | [MacSpi](../javax/crypto/MacSpi.md)!:the delegate |
| `provider` | [Provider](../java/security/Provider.md)!:the provider |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm |
| --- | --- |

## Public methods

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): Any
```

Returns a clone if the provider implementation is cloneable.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone if the provider implementation is cloneable. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |
| `java.lang.CloneNotSupportedException` | if this is called on a delegate that does not support`Cloneable`. |

### doFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doFinal(): ByteArray!
```

Finishes the MAC operation.

A call to this method resets this`Mac`object to the state it was in when previously initialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`. That is, the object is reset and available to generate another MAC from the same key, if desired, via new calls to`update`and`doFinal`. (In order to reuse this`Mac`object with a different key, it must be reinitialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`.

| Return ||
|------------------------------------------------------------------------------------------|-----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the MAC result. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### doFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doFinal(input: ByteArray!): ByteArray!
```

Processes the given array of bytes and finishes the MAC operation.

A call to this method resets this`Mac`object to the state it was in when previously initialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`. That is, the object is reset and available to generate another MAC from the same key, if desired, via new calls to`update`and`doFinal`. (In order to reuse this`Mac`object with a different key, it must be reinitialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:data in bytes |

| Return ||
|------------------------------------------------------------------------------------------|-----------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the MAC result. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### doFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun doFinal(
    output: ByteArray!, 
    outOffset: Int
): Unit
```

Finishes the MAC operation.

A call to this method resets this`Mac`object to the state it was in when previously initialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`. That is, the object is reset and available to generate another MAC from the same key, if desired, via new calls to`update`and`doFinal`. (In order to reuse this`Mac`object with a different key, it must be reinitialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`.

The MAC result is stored in`output`, starting at`outOffset`inclusive.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer where the MAC result is stored |
| `outOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`output`where the MAC is stored |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------|
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result |
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm name of this`Mac`object.

This is the same name that was specified in one of the`getInstance`calls that created this`Mac`object.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm name of this`Mac`object. |

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(algorithm: String!): Mac!
```

Returns a`Mac`object that implements the specified MAC algorithm.

This method traverses the list of registered security Providers, starting with the most preferred Provider. A new Mac object encapsulating the MacSpi implementation from the first Provider that supports the specified algorithm is returned.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested MAC algorithm. See the Mac section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Mac) for information about standard algorithm names. |

| Return ||
|--------------------------------------------------------------------------|---------------------|
| [Mac](../javax/crypto/Mac.md)! | the new`Mac`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if no Provider supports a MacSpi implementation for the specified algorithm. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: String!
): Mac!
```

Returns a`Mac`object that implements the specified MAC algorithm.

A new Mac object encapsulating the MacSpi implementation from the specified provider is returned. The specified provider must be registered in the security provider list.

Note that the list of registered providers may be retrieved via the [Security.getProviders()](../java/security/Security.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested MAC algorithm. See the Mac section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Mac) for information about standard algorithm names. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider. |

| Return ||
|--------------------------------------------------------------------------|---------------------|
| [Mac](../javax/crypto/Mac.md)! | the new`Mac`object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a MacSpi implementation for the specified algorithm is not available from the specified provider. |
| `java.security.NoSuchProviderException` | if the specified provider is not registered in the security provider list. |
| `java.lang.IllegalArgumentException` | if the`provider`is null or empty. |
| --- | --- |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getInstance(
    algorithm: String!, 
    provider: Provider!
): Mac!
```

Returns a`Mac`object that implements the specified MAC algorithm.

A new Mac object encapsulating the MacSpi implementation from the specified Provider object is returned. Note that the specified Provider object does not have to be registered in the provider list.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the standard name of the requested MAC algorithm. See the Mac section in the [Java Cryptography Architecture Standard Algorithm Name Documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/security/StandardNames.html#Mac) for information about standard algorithm names. |
| `provider` | [Provider](../java/security/Provider.md)!:the provider. |

| Return ||
|--------------------------------------------------------------------------|---------------------|
| [Mac](../javax/crypto/Mac.md)! | the new`Mac`object. |

| Exceptions ||
|------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if a MacSpi implementation for the specified algorithm is not available from the specified Provider object. |
| `java.lang.IllegalArgumentException` | if the`provider`is null. |

**See Also**

- [java.security.Provider](../java/security/Provider.md) 

### getMacLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMacLength(): Int
```

Returns the length of the MAC in bytes.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the MAC length in bytes. |

### getProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProvider(): Provider!
```

Returns the provider of this`Mac`object.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [Provider](../java/security/Provider.md)! | the provider of this`Mac`object. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(key: Key!): Unit
```

Initializes this`Mac`object with the given key.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------|
| `key` | [Key](../java/security/Key.md)!:the key. |

| Exceptions ||
|-------------------------------------|--------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this MAC. |

### init

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun init(
    key: Key!, 
    params: AlgorithmParameterSpec!
): Unit
```

Initializes this`Mac`object with the given key and algorithm parameters.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](../java/security/Key.md)!:the key. |
| `params` | [AlgorithmParameterSpec](../java/security/spec/AlgorithmParameterSpec.md)!:the algorithm parameters. |

| Exceptions ||
|----------------------------------------------------|-------------------------------------------------------------------|
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this MAC. |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this MAC. |

### reset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun reset(): Unit
```

Resets this`Mac`object.

A call to this method resets this`Mac`object to the state it was in when previously initialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`. That is, the object is reset and available to generate another MAC from the same key, if desired, via new calls to`update`and`doFinal`. (In order to reuse this`Mac`object with a different key, it must be reinitialized via a call to`init(Key)`or`init(Key, AlgorithmParameterSpec)`. 

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(input: Byte): Unit
```

Processes the given byte.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `input` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the input byte to be processed. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(input: ByteArray!): Unit
```

Processes the given array of bytes.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the array of bytes to be processed. |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(
    input: ByteArray!, 
    offset: Int, 
    len: Int
): Unit
```

Processes the first`len`bytes in`input`, starting at`offset`inclusive.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts. |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to process. |
| --- | --- |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |

### update

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun update(input: ByteBuffer!): Unit
```

Processes`input.remaining()`bytes in the ByteBuffer`input`, starting at`input.position()`. Upon return, the buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](../java/nio/ByteBuffer.md)!:the ByteBuffer |

| Exceptions ||
|-----------------------------------|---------------------------------------|
| `java.lang.IllegalStateException` | if this`Mac`has not been initialized. |
