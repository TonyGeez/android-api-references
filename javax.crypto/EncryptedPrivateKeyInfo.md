# EncryptedPrivateKeyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EncryptedPrivateKeyInfo

```
open class EncryptedPrivateKeyInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.crypto.EncryptedPrivateKeyInfo](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#) |

This class implements the`EncryptedPrivateKeyInfo`type as defined in PKCS #8.

Its ASN.1 definition is as follows: 

```kotlin
EncryptedPrivateKeyInfo ::=  SEQUENCE {
      encryptionAlgorithm   AlgorithmIdentifier,
      encryptedData   OCTET STRING }
 
  AlgorithmIdentifier  ::=  SEQUENCE  {
      algorithm              OBJECT IDENTIFIER,
      parameters             ANY DEFINED BY algorithm OPTIONAL  }
  
```

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EncryptedPrivateKeyInfo](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#EncryptedPrivateKeyInfo(kotlin.ByteArray))`(`encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs (i.e., parses) an |
| [EncryptedPrivateKeyInfo](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#EncryptedPrivateKeyInfo(kotlin.String,%20kotlin.ByteArray))`(`algName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `encryptedData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs an`EncryptedPrivateKeyInfo`from the encryption algorithm name and the encrypted data. |
| [EncryptedPrivateKeyInfo](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#EncryptedPrivateKeyInfo(java.security.AlgorithmParameters,%20kotlin.ByteArray))`(`algParams:` ` [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)!`, `encryptedData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Constructs an`EncryptedPrivateKeyInfo`from the encryption algorithm parameters and the encrypted data. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgName](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getAlgName())`()` Returns the encryption algorithm. |
| open [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)! | [getAlgParameters](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getAlgParameters())`()` Returns the algorithm parameters used by the encryption algorithm. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getEncoded())`()` Returns the ASN. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncryptedData](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getEncryptedData())`()` Returns the encrypted data. |
| open [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getKeySpec(java.security.Key))`(`decryptKey:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`)` Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it. |
| open [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getKeySpec(java.security.Key,%20kotlin.String))`(`decryptKey:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `providerName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it. |
| --- | --- |
| open [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getKeySpec(java.security.Key,%20java.security.Provider))`(`decryptKey:` ` [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!`, `provider:` ` [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!`)` Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it. |
| open [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | [getKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/EncryptedPrivateKeyInfo#getKeySpec(javax.crypto.Cipher))`(`cipher:` ` [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!`)` Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it. |

## Public constructors

### EncryptedPrivateKeyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EncryptedPrivateKeyInfo(encoded: ByteArray!)
```

Constructs (i.e., parses) an`EncryptedPrivateKeyInfo`from its ASN.1 encoding.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the ASN.1 encoding of this object. The contents of the array are copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|--------------------------------------------------|
| `java.lang.NullPointerException` | if the`encoded`is null. |
| `java.io.IOException` | if error occurs when parsing the ASN.1 encoding. |

### EncryptedPrivateKeyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EncryptedPrivateKeyInfo(
    algName: String!, 
    encryptedData: ByteArray!)
```

Constructs an`EncryptedPrivateKeyInfo`from the encryption algorithm name and the encrypted data.

Note: This constructor will use null as the value of the algorithm parameters. If the encryption algorithm has parameters whose value is not null, a different constructor, e.g. EncryptedPrivateKeyInfo(AlgorithmParameters, byte\[\]), should be used.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:encryption algorithm name. See Appendix A in the [Java Cryptography Architecture Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard Cipher algorithm names. |
| `encryptedData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:encrypted data. The contents of`encrypedData`are copied to protect against subsequent modification when constructing this object. |

| Exceptions ||
|------------------------------------------|--------------------------------------------|
| `java.lang.NullPointerException` | if`algName`or`encryptedData`is null. |
| `java.lang.IllegalArgumentException` | if`encryptedData`is empty, i.e. 0-length. |
| `java.security.NoSuchAlgorithmException` | if the specified algName is not supported. |
| --- | --- |

### EncryptedPrivateKeyInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EncryptedPrivateKeyInfo(
    algParams: AlgorithmParameters!, 
    encryptedData: ByteArray!)
```

Constructs an`EncryptedPrivateKeyInfo`from the encryption algorithm parameters and the encrypted data.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `algParams` | [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)!:the algorithm parameters for the encryption algorithm.`algParams.getEncoded()`should return the ASN.1 encoded bytes of the`parameters`field of the`AlgorithmIdentifer`component of the`EncryptedPrivateKeyInfo`type. |
| `encryptedData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:encrypted data. The contents of`encrypedData`are copied to protect against subsequent modification when constructing this object. |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`algParams`or`encryptedData`is null. |
| `java.lang.IllegalArgumentException` | if`encryptedData`is empty, i.e. 0-length. |
| `java.security.NoSuchAlgorithmException` | if the specified algName of the specified`algParams`parameter is not supported. |
| --- | --- |

## Public methods

### getAlgName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlgName(): String!
```

Returns the encryption algorithm.

Note: Standard name is returned instead of the specified one in the constructor when such mapping is available. See Appendix A in the [Java Cryptography Architecture Reference Guide](https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#AppA) for information about standard Cipher algorithm names.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the encryption algorithm name. |

### getAlgParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlgParameters(): AlgorithmParameters!
```

Returns the algorithm parameters used by the encryption algorithm.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------|
| [AlgorithmParameters](https://developer.android.com/reference/kotlin/java/security/AlgorithmParameters.html#)! | the algorithm parameters. |

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoded(): ByteArray!
```

Returns the ASN.1 encoding of this object.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the ASN.1 encoding. Returns a new array each time this method is called. |

| Exceptions ||
|-----------------------|-------------------------------------------------------|
| `java.io.IOException` | if error occurs when constructing its ASN.1 encoding. |

### getEncryptedData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncryptedData(): ByteArray!
```

Returns the encrypted data.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the encrypted data. Returns a new array each time this method is called. |

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeySpec(decryptKey: Key!): PKCS8EncodedKeySpec!
```

Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `decryptKey` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:key used for decrypting the encrypted data. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | the PKCS8EncodedKeySpec object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`decryptKey`is null. |
| `java.security.NoSuchAlgorithmException` | if cannot find appropriate cipher to decrypt the encrypted data. |
| `java.security.InvalidKeyException` | if`decryptKey`cannot be used to decrypt the encrypted data or the decryption result is not a valid PKCS8KeySpec. |
| --- | --- |

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeySpec(
    decryptKey: Key!, 
    providerName: String!
): PKCS8EncodedKeySpec!
```

Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `decryptKey` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:key used for decrypting the encrypted data. |
| `providerName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of provider whose Cipher implementation will be used. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | the PKCS8EncodedKeySpec object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`decryptKey`or`providerName`is null. |
| `java.security.NoSuchProviderException` | if no provider`providerName`is registered. |
| `java.security.NoSuchAlgorithmException` | if cannot find appropriate cipher to decrypt the encrypted data. |
| --- | --- |
| `java.security.InvalidKeyException` | if`decryptKey`cannot be used to decrypt the encrypted data or the decryption result is not a valid PKCS8KeySpec. |

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeySpec(
    decryptKey: Key!, 
    provider: Provider!
): PKCS8EncodedKeySpec!
```

Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `decryptKey` | [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#)!:key used for decrypting the encrypted data. |
| `provider` | [Provider](https://developer.android.com/reference/kotlin/java/security/Provider.html#)!:the name of provider whose Cipher implementation will be used. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | the PKCS8EncodedKeySpec object. |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`decryptKey`or`provider`is null. |
| `java.security.NoSuchAlgorithmException` | if cannot find appropriate cipher to decrypt the encrypted data in`provider`. |
| `java.security.InvalidKeyException` | if`decryptKey`cannot be used to decrypt the encrypted data or the decryption result is not a valid PKCS8KeySpec. |
| --- | --- |

### getKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeySpec(cipher: Cipher!): PKCS8EncodedKeySpec!
```

Extract the enclosed PKCS8EncodedKeySpec object from the encrypted data and return it. 
Note: In order to successfully retrieve the enclosed PKCS8EncodedKeySpec object,`cipher`needs to be initialized to either Cipher.DECRYPT_MODE or Cipher.UNWRAP_MODE, with the same key and parameters used for generating the encrypted data.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cipher` | [Cipher](https://developer.android.com/reference/kotlin/javax/crypto/Cipher)!:the initialized cipher object which will be used for decrypting the encrypted data. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [PKCS8EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/PKCS8EncodedKeySpec.html#)! | the PKCS8EncodedKeySpec object. |

| Exceptions ||
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`cipher`is null. |
| `java.security.spec.InvalidKeySpecException` | if the given cipher is inappropriate for the encrypted data or the encrypted data is corrupted and cannot be decrypted. |
