# PKCS8EncodedKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PKCS8EncodedKeySpec

```
open class PKCS8EncodedKeySpec : EncodedKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.spec.EncodedKeySpec](../java/security/spec/EncodedKeySpec.md) ||
| | ↳ | [java.security.spec.PKCS8EncodedKeySpec](../java/security/spec/PKCS8EncodedKeySpec.md) |

This class represents the ASN.1 encoding of a private key, encoded according to the ASN.1 type`PrivateKeyInfo`. The`PrivateKeyInfo`syntax is defined in the PKCS#8 standard as follows: 

```kotlin
PrivateKeyInfo ::= SEQUENCE {
    version Version,
    privateKeyAlgorithm PrivateKeyAlgorithmIdentifier,
    privateKey PrivateKey,
    attributes [0] IMPLICIT Attributes OPTIONAL }
 
  Version ::= INTEGER
 
  PrivateKeyAlgorithmIdentifier ::= AlgorithmIdentifier
 
  PrivateKey ::= OCTET STRING
 
  Attributes ::= SET OF Attribute
  
```

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PKCS8EncodedKeySpec](../java/security/spec/PKCS8EncodedKeySpec.md))`(`encodedKey:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates a new`PKCS8EncodedKeySpec`with the given encoded key. |
| [PKCS8EncodedKeySpec](../java/security/spec/PKCS8EncodedKeySpec.md))`(`encodedKey:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`PKCS8EncodedKeySpec`with the given encoded key and algorithm. |

| Public methods ||
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](../java/security/spec/PKCS8EncodedKeySpec.md))`()` Returns the key bytes, encoded according to the PKCS #8 standard. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](../java/security/spec/PKCS8EncodedKeySpec.md))`()` Returns the name of the encoding format associated with this key specification. |

| Inherited functions ||
|---|---|
| From class [EncodedKeySpec](../java/security/spec/EncodedKeySpec.md) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](../java/security/spec/EncodedKeySpec.md))`()` <br /> Returns the name of the algorithm of the encoded key. <br /> | ||

## Public constructors

### PKCS8EncodedKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKCS8EncodedKeySpec(encodedKey: ByteArray!)
```

Creates a new`PKCS8EncodedKeySpec`with the given encoded key.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key, which is assumed to be encoded according to the PKCS #8 standard. The contents of the array are copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`encodedKey`is null. |

### PKCS8EncodedKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PKCS8EncodedKeySpec(
    encodedKey: ByteArray!, 
    algorithm: String!)
```

Creates a new`PKCS8EncodedKeySpec`with the given encoded key and algorithm. This constructor is useful when subsequent callers of the`PKCS8EncodedKeySpec`object might not know the algorithm of the private key.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key, which is assumed to be encoded according to the PKCS #8 standard. The contents of the array are copied to protect against subsequent modification. |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name of the encoded private key See the KeyFactory section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyfactory-algorithms) for information about standard algorithm names. |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.NullPointerException` | if`encodedKey`or`algorithm`is null. |
| `java.lang.IllegalArgumentException` | if`algorithm`is the empty string`""` |

## Public methods

### getEncoded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEncoded(): ByteArray!
```

Returns the key bytes, encoded according to the PKCS #8 standard.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the PKCS #8 encoding of the key. Returns a new array each time this method is called. |

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): String!
```

Returns the name of the encoding format associated with this key specification.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string`"PKCS#8"`. |
