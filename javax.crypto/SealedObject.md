# SealedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SealedObject

```
open class SealedObject : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [javax.crypto.SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#) |

This class enables a programmer to create an object and protect its confidentiality with a cryptographic algorithm.

Given any Serializable object, one can create a SealedObject that encapsulates the original object, in serialized format (i.e., a "deep copy"), and seals (encrypts) its serialized contents, using a cryptographic algorithm such as DES, to protect its confidentiality. The encrypted content can later be decrypted (with the corresponding algorithm using the correct decryption key) and de-serialized, yielding the original object.

Note that the Cipher object must be fully initialized with the correct algorithm, key, padding scheme, etc., before being applied to a SealedObject.

The original object that was sealed can be recovered in two different ways:

- by using the [getObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getObject(javax.crypto.Cipher))method that takes a`Cipher`object.

 This method requires a fully initialized`Cipher`object, initialized with the exact same algorithm, key, padding scheme, etc., that were used to seal the object.

 This approach has the advantage that the party who unseals the sealed object does not require knowledge of the decryption key. For example, after one party has initialized the cipher object with the required decryption key, it could hand over the cipher object to another party who then unseals the sealed object.
- by using one of the [getObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getObject(java.security.Key))methods that take a`Key`object.

 In this approach, the`getObject`method creates a cipher object for the appropriate decryption algorithm and initializes it with the given decryption key and the algorithm parameters (if any) that were stored in the sealed object.

 This approach has the advantage that the party who unseals the object does not need to keep track of the parameters (e.g., an IV) that were used to seal the object.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#SealedObject(java.io.Serializable,%20javax.crypto.Cipher))`(`object:` ` [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)!`, `c:` ` [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!`)` Constructs a SealedObject from any Serializable object. |

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#SealedObject(javax.crypto.SealedObject))`(`so:` ` [SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#)!`)` Constructs a SealedObject object from the passed-in SealedObject. |

| Public methods ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getAlgorithm())`()` Returns the algorithm that was used to seal this object. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getObject(java.security.Key))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`)` Retrieves the original (encapsulated) object. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getObject(java.security.Key,%20kotlin.String))`(`key:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `provider:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Retrieves the original (encapsulated) object. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#getObject(javax.crypto.Cipher))`(`c:` ` [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!`)` Retrieves the original (encapsulated) object. |

| Properties ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [encodedParams](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#encodedParams:kotlin.ByteArray) The cryptographic parameters used by the sealing Cipher, encoded in the default format. |

## Public constructors

### SealedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SealedObject(
    object: Serializable!, 
    c: Cipher!)
```

Constructs a SealedObject from any Serializable object.

The given object is serialized, and its serialized contents are encrypted using the given Cipher, which must be fully initialized.

Any algorithm parameters that may be used in the encryption operation are stored inside of the new`SealedObject`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| `object` | [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)!:the object to be sealed; can be null. |
| `c` | [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!:the cipher used to seal the object. |

| Exceptions ||
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given cipher is null. |
| `java.io.IOException` | if an error occurs during serialization |
| `javax.crypto.IllegalBlockSizeException` | if the given cipher is a block cipher, no padding has been requested, and the total input length (i.e., the length of the serialized object contents) is not a multiple of the cipher's block size |

## Protected constructors

### SealedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SealedObject(so: SealedObject!)
```

Constructs a SealedObject object from the passed-in SealedObject.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------|
| `so` | [SealedObject](https://developer.android.com/reference/kotlin/javax/crypto/SealedObject#)!:a SealedObject object |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the given sealed object is null. |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Returns the algorithm that was used to seal this object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the algorithm that was used to seal this object. |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObject(key: Key!): Any!
```

Retrieves the original (encapsulated) object.

This method creates a cipher for the algorithm that had been used in the sealing operation. If the default provider package provides an implementation of that algorithm, an instance of Cipher containing that implementation is used. If the algorithm is not available in the default package, other packages are searched. The Cipher object is initialized for decryption, using the given`key`and the parameters (if any) that had been used in the sealing operation.

The encapsulated object is unsealed and de-serialized, before it is returned.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the key used to unseal the object. |

| Return ||
|-----------------------------------------------------------------------------|----------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the original object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an error occurs during de-serialiazation. |
| `java.lang.ClassNotFoundException` | if an error occurs during de-serialiazation. |
| `java.security.NoSuchAlgorithmException` | if the algorithm to unseal the object is not available. |
| `java.security.InvalidKeyException` | if the given key cannot be used to unseal the object (e.g., it has the wrong algorithm). |
| `java.lang.NullPointerException` | if`key`is null. |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObject(
    key: Key!, 
    provider: String!
): Any!
```

Retrieves the original (encapsulated) object.

This method creates a cipher for the algorithm that had been used in the sealing operation, using an implementation of that algorithm from the given`provider`. The Cipher object is initialized for decryption, using the given`key`and the parameters (if any) that had been used in the sealing operation.

The encapsulated object is unsealed and de-serialized, before it is returned.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:the key used to unseal the object. |
| `provider` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the provider of the algorithm to unseal the object. |

| Return ||
|-----------------------------------------------------------------------------|----------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the original object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the given provider is null or empty. |
| `java.io.IOException` | if an error occurs during de-serialiazation. |
| `java.lang.ClassNotFoundException` | if an error occurs during de-serialiazation. |
| `java.security.NoSuchAlgorithmException` | if the algorithm to unseal the object is not available. |
| `java.security.NoSuchProviderException` | if the given provider is not configured. |
| `java.security.InvalidKeyException` | if the given key cannot be used to unseal the object (e.g., it has the wrong algorithm). |
| `java.lang.NullPointerException` | if`key`is null. |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObject(c: Cipher!): Any!
```

Retrieves the original (encapsulated) object.

The encapsulated object is unsealed (using the given Cipher, assuming that the Cipher is already properly initialized) and de-serialized, before it is returned.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------|
| `c` | [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!:the cipher used to unseal the object |

| Return ||
|-----------------------------------------------------------------------------|----------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the original object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the given cipher is null. |
| `java.io.IOException` | if an error occurs during de-serialiazation |
| `java.lang.ClassNotFoundException` | if an error occurs during de-serialiazation |
| `javax.crypto.IllegalBlockSizeException` | if the given cipher is a block cipher, no padding has been requested, and the total input length is not a multiple of the cipher's block size |
| `javax.crypto.BadPaddingException` | if the given cipher has been initialized for decryption, and padding has been specified, but the input data does not have proper expected padding bytes |

## Properties

### encodedParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var encodedParams: ByteArray!
```

The cryptographic parameters used by the sealing Cipher, encoded in the default format.

That is,`cipher.getParameters().getEncoded()`.
