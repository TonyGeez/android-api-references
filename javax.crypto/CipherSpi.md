# CipherSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CipherSpi

```
abstract class CipherSpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.CipherSpi](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`Cipher`class. All the abstract methods in this class must be implemented by each cryptographic service provider who wishes to supply the implementation of a particular cipher algorithm.

In order to create an instance of`Cipher`, which encapsulates an instance of this`CipherSpi`class, an application calls one of the [getInstance](https://developer.android.com/reference/kotlin/javax/crypto/Cipher#getInstance(kotlin.String))factory methods of the [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher) engine class and specifies the requested*transformation*. Optionally, the application may also specify the name of a provider.

A*transformation* is a string that describes the operation (or set of operations) to be performed on the given input, to produce some output. A transformation always includes the name of a cryptographic algorithm (e.g.,*DES*), and may be followed by a feedback mode and padding scheme.

A transformation is of the form:

- "*algorithm/mode/padding*" or
- "*algorithm*"

(in the latter case, provider-specific default values for the mode and padding scheme are used). For example, the following is a valid transformation: 

```kotlin
<code>Cipher c = Cipher.getInstance("DES/CBC/PKCS5Padding");
  </code>
```

A provider may supply a separate class for each combination of*algorithm/mode/padding* , or may decide to provide more generic classes representing sub-transformations corresponding to*algorithm* or*algorithm/mode* or*algorithm//padding* (note the double slashes), in which case the requested mode and/or padding are set automatically by the`getInstance`methods of`Cipher`, which invoke the [engineSetMode](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineSetMode(kotlin.String))and [engineSetPadding](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineSetPadding(kotlin.String))methods of the provider's subclass of`CipherSpi`.

A`Cipher`property in a provider master class may have one of the following formats:

-

  ```kotlin
  // provider's subclass of "CipherSpi" implements "algName" with
        // pluggable mode and padding
        <code>Cipher.</code><i>algName</i>
  ```
-

  ```kotlin
  // provider's subclass of "CipherSpi" implements "algName" in the
        // specified "mode", with pluggable padding
        <code>Cipher.</code><i>algName/mode</i>
  ```
-

  ```kotlin
  // provider's subclass of "CipherSpi" implements "algName" with the
        // specified "padding", with pluggable mode
        <code>Cipher.</code><i>algName//padding</i>
  ```
-

  ```kotlin
  // provider's subclass of "CipherSpi" implements "algName" with the
        // specified "mode" and "padding"
        <code>Cipher.</code><i>algName/mode/padding</i>
  ```

For example, a provider may supply a subclass of`CipherSpi`that implements*DES/ECB/PKCS5Padding* , one that implements*DES/CBC/PKCS5Padding* , one that implements*DES/CFB/PKCS5Padding* , and yet another one that implements*DES/OFB/PKCS5Padding* . That provider would have the following`Cipher`properties in its master class:

-

  ```kotlin
  <code>Cipher.</code><i>DES/ECB/PKCS5Padding</i>
  ```
-

  ```kotlin
  <code>Cipher.</code><i>DES/CBC/PKCS5Padding</i>
  ```
-

  ```kotlin
  <code>Cipher.</code><i>DES/CFB/PKCS5Padding</i>
  ```
-

  ```kotlin
  <code>Cipher.</code><i>DES/OFB/PKCS5Padding</i>
  ```

Another provider may implement a class for each of the above modes (i.e., one class for*ECB* , one for*CBC* , one for*CFB* , and one for*OFB* ), one class for*PKCS5Padding* , and a generic*DES* class that subclasses from`CipherSpi`. That provider would have the following`Cipher`properties in its master class:

-

  ```kotlin
  <code>Cipher.</code><i>DES</i>
  ```

The`getInstance`factory method of the`Cipher`engine class follows these rules in order to instantiate a provider's implementation of`CipherSpi`for a transformation of the form "*algorithm*":

1. Check if the provider has registered a subclass of`CipherSpi`for the specified "*algorithm* ".

 If the answer is YES, instantiate this class, for whose mode and padding scheme default values (as supplied by the provider) are used.

 If the answer is NO, throw a`NoSuchAlgorithmException`exception.

The`getInstance`factory method of the`Cipher`engine class follows these rules in order to instantiate a provider's implementation of`CipherSpi`for a transformation of the form "*algorithm/mode/padding*":

1. Check if the provider has registered a subclass of`CipherSpi`for the specified "*algorithm/mode/padding* " transformation.

 If the answer is YES, instantiate it.

 If the answer is NO, go to the next step.
2. Check if the provider has registered a subclass of`CipherSpi`for the sub-transformation "*algorithm/mode* ".

 If the answer is YES, instantiate it, and call`engineSetPadding(`*padding*`)`on the new instance.

 If the answer is NO, go to the next step.
3. Check if the provider has registered a subclass of`CipherSpi`for the sub-transformation "*algorithm//padding* " (note the double slashes).

 If the answer is YES, instantiate it, and call`engineSetMode(`*mode*`)`on the new instance.

 If the answer is NO, go to the next step.
4. Check if the provider has registered a subclass of`CipherSpi`for the sub-transformation "*algorithm* ".

 If the answer is YES, instantiate it, and call`engineSetMode(`*mode*`)`and`engineSetPadding(`*padding*`)`on the new instance.

 If the answer is NO, throw a`NoSuchAlgorithmException`exception.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------|---|
| [CipherSpi](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#CipherSpi())`()` <br /> |

| Protected methods ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineDoFinal](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineDoFinal(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `inputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineDoFinal](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineDoFinal(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `inputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `outputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineDoFinal](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineDoFinal(java.nio.ByteBuffer,%20java.nio.ByteBuffer))`(`input:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `output:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetBlockSize](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetBlockSize())`()` Returns the block size (in bytes). |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineGetIV](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetIV())`()` Returns the initialization vector (IV) in a new buffer. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetKeySize](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetKeySize(java.security.Key))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`)` Returns the key size of the given key object in bits. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineGetOutputSize](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetOutputSize(kotlin.Int))`(`inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the length in bytes that an output buffer would need to be in order to hold the result of the next`update`or`doFinal`operation, given the input length`inputLen`(in bytes). |
| abstract [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)! | [engineGetParameters](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetParameters())`()` Returns the parameters used with this cipher. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineInit(kotlin.Int,%20java.security.Key,%20java.security.AlgorithmParameters,%20java.security.SecureRandom))`(`opmode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `params:` ` [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this cipher with a key, a set of algorithm parameters, and a source of randomness. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineInit(kotlin.Int,%20java.security.Key,%20java.security.SecureRandom))`(`opmode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this cipher with a key and a source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineInit](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineInit(kotlin.Int,%20java.security.Key,%20java.security.spec.AlgorithmParameterSpec,%20java.security.SecureRandom))`(`opmode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `params:` ` [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!`, `random:` ` [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!`)` Initializes this cipher with a key, a set of algorithm parameters, and a source of randomness. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetMode](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineSetMode(kotlin.String))`(`mode:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the mode of this cipher. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineSetPadding](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineSetPadding(kotlin.String))`(`padding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the padding mechanism of this cipher. |
| open [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)! | [engineUnwrap](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUnwrap(kotlin.ByteArray,%20kotlin.String,%20kotlin.Int))`(`wrappedKey:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `wrappedKeyAlgorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `wrappedKeyType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Unwrap a previously wrapped key. |
| abstract [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUpdate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `inputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUpdate(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int))`(`input:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `inputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputLen:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `output:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `outputOffset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [engineUpdate](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUpdate(java.nio.ByteBuffer,%20java.nio.ByteBuffer))`(`input:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `output:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdateAAD](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUpdateAAD(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`src:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `len:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Continues a multi-part update of the Additional Authentication Data (AAD), using a subset of the provided buffer. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineUpdateAAD](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineUpdateAAD(java.nio.ByteBuffer))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Continues a multi-part update of the Additional Authentication Data (AAD). |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [engineWrap](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineWrap(java.security.Key))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`)` Wrap a key. |

## Public constructors

### CipherSpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CipherSpi()
```

## Protected methods

### engineDoFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineDoFinal(
    input: ByteArray!, 
    inputOffset: Int, 
    inputLen: Int
): ByteArray!
```

Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. The data is encrypted or decrypted, depending on how this cipher was initialized.

The first`inputLen`bytes in the`input`buffer, starting at`inputOffset`inclusive, and any input bytes that may have been buffered during a previous`update`operation, are processed, with padding (if requested) being applied. If an AEAD mode such as GCM/CCM is being used, the authentication tag is appended in the case of encryption, or verified in the case of decryption. The result is stored in a new buffer.

Upon finishing, this method resets this cipher object to the state it was in when previously initialized via a call to`engineInit`. That is, the object is reset and available to encrypt or decrypt (depending on the operation mode that was specified in the call to`engineInit`) more data.

Note: if any exception is thrown, this cipher object may need to be reset before it can be used again.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer |
| `inputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts |
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the result |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.crypto.IllegalBlockSizeException` | if this cipher is a block cipher, no padding has been requested (only in encryption mode), and the total input length of the data processed by this cipher is not a multiple of block size; or if this encryption algorithm is unable to process the input data provided. |
| `javax.crypto.BadPaddingException` | if this cipher is in decryption mode, and (un)padding has been requested, but the decrypted data is not bounded by the appropriate padding bytes |
| `javax.crypto.AEADBadTagException` | if this cipher is decrypting in an AEAD mode (such as GCM/CCM), and the received authentication tag does not match the calculated value |
| --- | --- |

### engineDoFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineDoFinal(
    input: ByteArray!, 
    inputOffset: Int, 
    inputLen: Int, 
    output: ByteArray!, 
    outputOffset: Int
): Int
```

Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. The data is encrypted or decrypted, depending on how this cipher was initialized.

The first`inputLen`bytes in the`input`buffer, starting at`inputOffset`inclusive, and any input bytes that may have been buffered during a previous`update`operation, are processed, with padding (if requested) being applied. If an AEAD mode such as GCM/CCM is being used, the authentication tag is appended in the case of encryption, or verified in the case of decryption. The result is stored in the`output`buffer, starting at`outputOffset`inclusive.

If the`output`buffer is too small to hold the result, a`ShortBufferException`is thrown.

Upon finishing, this method resets this cipher object to the state it was in when previously initialized via a call to`engineInit`. That is, the object is reset and available to encrypt or decrypt (depending on the operation mode that was specified in the call to`engineInit`) more data.

Note: if any exception is thrown, this cipher object may need to be reset before it can be used again.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer |
| `inputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts |
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length |
| --- | --- |
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the result |
| `outputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`output`where the result is stored |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `javax.crypto.IllegalBlockSizeException` | if this cipher is a block cipher, no padding has been requested (only in encryption mode), and the total input length of the data processed by this cipher is not a multiple of block size; or if this encryption algorithm is unable to process the input data provided. |
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result |
| `javax.crypto.BadPaddingException` | if this cipher is in decryption mode, and (un)padding has been requested, but the decrypted data is not bounded by the appropriate padding bytes |
| --- | --- |
| `javax.crypto.AEADBadTagException` | if this cipher is decrypting in an AEAD mode (such as GCM/CCM), and the received authentication tag does not match the calculated value |

### engineDoFinal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineDoFinal(
    input: ByteBuffer!, 
    output: ByteBuffer!
): Int
```

Encrypts or decrypts data in a single-part operation, or finishes a multiple-part operation. The data is encrypted or decrypted, depending on how this cipher was initialized.

All`input.remaining()`bytes starting at`input.position()`are processed. If an AEAD mode such as GCM/CCM is being used, the authentication tag is appended in the case of encryption, or verified in the case of decryption. The result is stored in the output buffer. Upon return, the input buffer's position will be equal to its limit; its limit will not have changed. The output buffer's position will have advanced by n, where n is the value returned by this method; the output buffer's limit will not have changed.

If`output.remaining()`bytes are insufficient to hold the result, a`ShortBufferException`is thrown.

Upon finishing, this method resets this cipher object to the state it was in when previously initialized via a call to`engineInit`. That is, the object is reset and available to encrypt or decrypt (depending on the operation mode that was specified in the call to`engineInit`) more data.

Note: if any exception is thrown, this cipher object may need to be reset before it can be used again.

Subclasses should consider overriding this method if they can process ByteBuffers more efficiently than byte arrays.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the input ByteBuffer |
| `output` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the output ByteByffer |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either parameter is`null` |
| `javax.crypto.IllegalBlockSizeException` | if this cipher is a block cipher, no padding has been requested (only in encryption mode), and the total input length of the data processed by this cipher is not a multiple of block size; or if this encryption algorithm is unable to process the input data provided. |
| `javax.crypto.ShortBufferException` | if there is insufficient space in the output buffer |
| --- | --- |
| `javax.crypto.BadPaddingException` | if this cipher is in decryption mode, and (un)padding has been requested, but the decrypted data is not bounded by the appropriate padding bytes |
| `javax.crypto.AEADBadTagException` | if this cipher is decrypting in an AEAD mode (such as GCM/CCM), and the received authentication tag does not match the calculated value |

### engineGetBlockSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetBlockSize(): Int
```

Returns the block size (in bytes).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the block size (in bytes), or 0 if the underlying algorithm is not a block cipher |

### engineGetIV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetIV(): ByteArray!
```

Returns the initialization vector (IV) in a new buffer.

This is useful in the context of password-based encryption or decryption, where the IV is derived from a user-provided passphrase.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the initialization vector in a new buffer, or null if the underlying algorithm does not use an IV, or if the IV has not yet been set. |

### engineGetKeySize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetKeySize(key: Key!): Int
```

Returns the key size of the given key object in bits.

This concrete method has been added to this previously-defined abstract class. It throws an`UnsupportedOperationException`if it is not overridden by the provider.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the key object. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the key size of the given key object. |

| Exceptions ||
|-------------------------------------|--------------------|
| `java.security.InvalidKeyException` | if`key`is invalid. |

### engineGetOutputSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetOutputSize(inputLen: Int): Int
```

Returns the length in bytes that an output buffer would need to be in order to hold the result of the next`update`or`doFinal`operation, given the input length`inputLen`(in bytes).

This call takes into account any unprocessed (buffered) data from a previous`update`call, padding, and AEAD tagging.

The actual output length of the next`update`or`doFinal`call may be smaller than the length returned by this method.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------|
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length (in bytes) |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the required output buffer size (in bytes) |

### engineGetParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineGetParameters(): AlgorithmParameters!
```

Returns the parameters used with this cipher.

The returned parameters may be the same that were used to initialize this cipher, or may contain a combination of default and random parameter values used by the underlying cipher implementation if this cipher requires algorithm parameters but was not initialized with any.

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)! | the parameters used with this cipher, or null if this cipher does not use any parameters. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    opmode: Int, 
    key: Key!, 
    params: AlgorithmParameters!, 
    random: SecureRandom!
): Unit
```

Initializes this cipher with a key, a set of algorithm parameters, and a source of randomness.

The cipher is initialized for one of the following four operations: encryption, decryption, key wrapping or key unwrapping, depending on the value of`opmode`.

If this cipher requires any algorithm parameters and`params`is null, the underlying cipher implementation is supposed to generate the required parameters itself (using provider-specific default or random values) if it is being initialized for encryption or key wrapping, and raise an`InvalidAlgorithmParameterException`if it is being initialized for decryption or key unwrapping. The generated parameters can be retrieved using [engineGetParameters](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetParameters())or [engineGetIV](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetIV())(if the parameter is an IV).

If this cipher requires algorithm parameters that cannot be derived from the input parameters, and there are no reasonable provider-specific default values, initialization will necessarily fail.

If this cipher (including its underlying feedback or padding scheme) requires any random bytes (e.g., for parameter generation), it will get them from`random`.

Note that when a Cipher object is initialized, it loses all previously-acquired state. In other words, initializing a Cipher is equivalent to creating a new instance of that Cipher and initializing it.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `opmode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the operation mode of this cipher (this is one of the following:`ENCRYPT_MODE`,`DECRYPT_MODE`,`WRAP_MODE`or`UNWRAP_MODE`) |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the encryption key |
| `params` | [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)!:the algorithm parameters |
| --- | --- |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if`opmode`is`WRAP_MODE`or`UNWRAP_MODE`is not implemented by the cipher. |
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this cipher |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this cipher, or if this cipher requires algorithm parameters and`params`is null. |
| --- | --- |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    opmode: Int, 
    key: Key!, 
    random: SecureRandom!
): Unit
```

Initializes this cipher with a key and a source of randomness.

The cipher is initialized for one of the following four operations: encryption, decryption, key wrapping or key unwrapping, depending on the value of`opmode`.

If this cipher requires any algorithm parameters that cannot be derived from the given`key`, the underlying cipher implementation is supposed to generate the required parameters itself (using provider-specific default or random values) if it is being initialized for encryption or key wrapping, and raise an`InvalidKeyException`if it is being initialized for decryption or key unwrapping. The generated parameters can be retrieved using [engineGetParameters](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetParameters())or [engineGetIV](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetIV())(if the parameter is an IV).

If this cipher requires algorithm parameters that cannot be derived from the input parameters, and there are no reasonable provider-specific default values, initialization will necessarily fail.

If this cipher (including its underlying feedback or padding scheme) requires any random bytes (e.g., for parameter generation), it will get them from`random`.

Note that when a Cipher object is initialized, it loses all previously-acquired state. In other words, initializing a Cipher is equivalent to creating a new instance of that Cipher and initializing it.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `opmode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the operation mode of this cipher (this is one of the following:`ENCRYPT_MODE`,`DECRYPT_MODE`,`WRAP_MODE`or`UNWRAP_MODE`) |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the encryption key |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness |
| --- | --- |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if`opmode`is`WRAP_MODE`or`UNWRAP_MODE`is not implemented by the cipher. |
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this cipher, or requires algorithm parameters that cannot be determined from the given key. |

### engineInit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineInit(
    opmode: Int, 
    key: Key!, 
    params: AlgorithmParameterSpec!, 
    random: SecureRandom!
): Unit
```

Initializes this cipher with a key, a set of algorithm parameters, and a source of randomness.

The cipher is initialized for one of the following four operations: encryption, decryption, key wrapping or key unwrapping, depending on the value of`opmode`.

If this cipher requires any algorithm parameters and`params`is null, the underlying cipher implementation is supposed to generate the required parameters itself (using provider-specific default or random values) if it is being initialized for encryption or key wrapping, and raise an`InvalidAlgorithmParameterException`if it is being initialized for decryption or key unwrapping. The generated parameters can be retrieved using [engineGetParameters](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetParameters())or [engineGetIV](https://developer.android.com/reference/kotlin/javax/crypto/CipherSpi#engineGetIV())(if the parameter is an IV).

If this cipher requires algorithm parameters that cannot be derived from the input parameters, and there are no reasonable provider-specific default values, initialization will necessarily fail.

If this cipher (including its underlying feedback or padding scheme) requires any random bytes (e.g., for parameter generation), it will get them from`random`.

Note that when a Cipher object is initialized, it loses all previously-acquired state. In other words, initializing a Cipher is equivalent to creating a new instance of that Cipher and initializing it.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `opmode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the operation mode of this cipher (this is one of the following:`ENCRYPT_MODE`,`DECRYPT_MODE`,`WRAP_MODE`or`UNWRAP_MODE`) |
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the encryption key |
| `params` | [AlgorithmParameterSpec](https://developer.android.com/reference/kotlin/java/security/spec/AlgorithmParameterSpec.html#)!:the algorithm parameters |
| --- | --- |
| `random` | [SecureRandom](https://developer.android.com/reference/kotlin/java/security/SecureRandom.html#)!:the source of randomness |

| Exceptions ||
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if`opmode`is`WRAP_MODE`or`UNWRAP_MODE`is not implemented by the cipher. |
| `java.security.InvalidKeyException` | if the given key is inappropriate for initializing this cipher |
| `java.security.InvalidAlgorithmParameterException` | if the given algorithm parameters are inappropriate for this cipher, or if this cipher requires algorithm parameters and`params`is null. |
| --- | --- |

### engineSetMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineSetMode(mode: String!): Unit
```

Sets the mode of this cipher.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `mode` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the cipher mode |

| Exceptions ||
|------------------------------------------|---------------------------------------------|
| `java.security.NoSuchAlgorithmException` | if the requested cipher mode does not exist |

### engineSetPadding

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineSetPadding(padding: String!): Unit
```

Sets the padding mechanism of this cipher.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------|
| `padding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the padding mechanism |

| Exceptions ||
|---------------------------------------|---------------------------------------------------|
| `javax.crypto.NoSuchPaddingException` | if the requested padding mechanism does not exist |

### engineUnwrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUnwrap(
    wrappedKey: ByteArray!, 
    wrappedKeyAlgorithm: String!, 
    wrappedKeyType: Int
): Key!
```

Unwrap a previously wrapped key.

This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.) It may be overridden by a provider to unwrap a previously wrapped key. Such an override is expected to throw an InvalidKeyException if the given wrapped key cannot be unwrapped. If this method is not overridden, it always throws an UnsupportedOperationException.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `wrappedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key to be unwrapped. |
| `wrappedKeyAlgorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm associated with the wrapped key. |
| `wrappedKeyType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of the wrapped key. This is one of`SECRET_KEY`,`PRIVATE_KEY`, or`PUBLIC_KEY`. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------|--------------------|
| [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)! | the unwrapped key. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this method is not supported. |
| `java.security.NoSuchAlgorithmException` | if no installed providers can create keys of type`wrappedKeyType`for the`wrappedKeyAlgorithm`. |
| `java.security.InvalidKeyException` | if`wrappedKey`does not represent a wrapped key of type`wrappedKeyType`for the`wrappedKeyAlgorithm`. |
| --- | --- |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(
    input: ByteArray!, 
    inputOffset: Int, 
    inputLen: Int
): ByteArray!
```

Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part.

The first`inputLen`bytes in the`input`buffer, starting at`inputOffset`inclusive, are processed, and the result is stored in a new buffer.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer |
| `inputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts |
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the new buffer with the result, or null if the underlying cipher is a block cipher and the input data is too short to result in a new block. |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineUpdate(
    input: ByteArray!, 
    inputOffset: Int, 
    inputLen: Int, 
    output: ByteArray!, 
    outputOffset: Int
): Int
```

Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part.

The first`inputLen`bytes in the`input`buffer, starting at`inputOffset`inclusive, are processed, and the result is stored in the`output`buffer, starting at`outputOffset`inclusive.

If the`output`buffer is too small to hold the result, a`ShortBufferException`is thrown.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `input` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the input buffer |
| `inputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`input`where the input starts |
| `inputLen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input length |
| --- | --- |
| `output` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer for the result |
| `outputOffset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`output`where the result is stored |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------|
| `javax.crypto.ShortBufferException` | if the given output buffer is too small to hold the result |

### engineUpdate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdate(
    input: ByteBuffer!, 
    output: ByteBuffer!
): Int
```

Continues a multiple-part encryption or decryption operation (depending on how this cipher was initialized), processing another data part.

All`input.remaining()`bytes starting at`input.position()`are processed. The result is stored in the output buffer. Upon return, the input buffer's position will be equal to its limit; its limit will not have changed. The output buffer's position will have advanced by n, where n is the value returned by this method; the output buffer's limit will not have changed.

If`output.remaining()`bytes are insufficient to hold the result, a`ShortBufferException`is thrown.

Subclasses should consider overriding this method if they can process ByteBuffers more efficiently than byte arrays.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `input` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the input ByteBuffer |
| `output` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the output ByteByffer |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes stored in`output` |

| Exceptions ||
|-------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if either parameter is`null` |
| `javax.crypto.ShortBufferException` | if there is insufficient space in the output buffer |

### engineUpdateAAD

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdateAAD(
    src: ByteArray!, 
    offset: Int, 
    len: Int
): Unit
```

Continues a multi-part update of the Additional Authentication Data (AAD), using a subset of the provided buffer.

Calls to this method provide AAD to the cipher when operating in modes such as AEAD (GCM/CCM). If this cipher is operating in either GCM or CCM mode, all AAD must be supplied before beginning operations on the ciphertext (via the`update`and`doFinal`methods).

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer containing the AAD |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset in`src`where the AAD input starts |
| `len` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of AAD bytes |
| --- | --- |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this cipher is in a wrong state (e.g., has not been initialized), does not accept AAD, or if operating in either GCM or CCM mode and one of the`update`methods has already been called for the active encryption/decryption operation |
| `java.lang.UnsupportedOperationException` | if this method has not been overridden by an implementation |

### engineUpdateAAD

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineUpdateAAD(src: ByteBuffer!): Unit
```

Continues a multi-part update of the Additional Authentication Data (AAD).

Calls to this method provide AAD to the cipher when operating in modes such as AEAD (GCM/CCM). If this cipher is operating in either GCM or CCM mode, all AAD must be supplied before beginning operations on the ciphertext (via the`update`and`doFinal`methods).

All`src.remaining()`bytes starting at`src.position()`are processed. Upon return, the input buffer's position will be equal to its limit; its limit will not have changed.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the buffer containing the AAD |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this cipher is in a wrong state (e.g., has not been initialized), does not accept AAD, or if operating in either GCM or CCM mode and one of the`update`methods has already been called for the active encryption/decryption operation |
| `java.lang.UnsupportedOperationException` | if this method has not been overridden by an implementation |

### engineWrap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineWrap(key: Key!): ByteArray!
```

Wrap a key.

This concrete method has been added to this previously-defined abstract class. (For backwards compatibility, it cannot be abstract.) It may be overridden by a provider to wrap a key. Such an override is expected to throw an IllegalBlockSizeException or InvalidKeyException (under the specified circumstances), if the given key cannot be wrapped. If this method is not overridden, it always throws an UnsupportedOperationException.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the key to be wrapped. |

| Return ||
|------------------------------------------------------------------------------------------|------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the wrapped key. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this method is not supported. |
| `javax.crypto.IllegalBlockSizeException` | if this cipher is a block cipher, no padding has been requested, and the length of the encoding of the key to be wrapped is not a multiple of the block size. |
| `java.security.InvalidKeyException` | if it is impossible or unsafe to wrap the key with this cipher (e.g., a hardware protected key is being passed to a software-only cipher). |
| --- | --- |
