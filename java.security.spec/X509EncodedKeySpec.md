# X509EncodedKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# X509EncodedKeySpec

```
open class X509EncodedKeySpec : EncodedKeySpec
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.spec.EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EncodedKeySpec) ||
| | ↳ | [java.security.spec.X509EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec#) |

This class represents the ASN.1 encoding of a public key, encoded according to the ASN.1 type`SubjectPublicKeyInfo`. The`SubjectPublicKeyInfo`syntax is defined in the X.509 standard as follows: 

```kotlin
SubjectPublicKeyInfo ::= SEQUENCE {
    algorithm AlgorithmIdentifier,
    subjectPublicKey BIT STRING }
  
```

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [X509EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec#X509EncodedKeySpec(kotlin.ByteArray))`(`encodedKey:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates a new`X509EncodedKeySpec`with the given encoded key. |
| [X509EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec#X509EncodedKeySpec(kotlin.ByteArray,%20kotlin.String))`(`encodedKey:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a new`X509EncodedKeySpec`with the given encoded key. |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec#getEncoded())`()` Returns the key bytes, encoded according to the X. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/java/security/spec/X509EncodedKeySpec#getFormat())`()` Returns the name of the encoding format associated with this key specification. |

| Inherited functions ||
|---|---|
| From class [EncodedKeySpec](https://developer.android.com/reference/kotlin/java/security/spec/EncodedKeySpec) |-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/spec/EncodedKeySpec#getAlgorithm())`()` <br /> Returns the name of the algorithm of the encoded key. <br /> | ||

## Public constructors

### X509EncodedKeySpec

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509EncodedKeySpec(encodedKey: ByteArray!)
```

Creates a new`X509EncodedKeySpec`with the given encoded key.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key, which is assumed to be encoded according to the X.509 standard. The contents of the array are copied to protect against subsequent modification. |

| Exceptions ||
|----------------------------------|------------------------|
| `java.lang.NullPointerException` | if`encodedKey`is null. |

### X509EncodedKeySpec

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
X509EncodedKeySpec(
    encodedKey: ByteArray!, 
    algorithm: String!)
```

Creates a new`X509EncodedKeySpec`with the given encoded key. This constructor is useful when subsequent callers of the`X509EncodedKeySpec`object might not know the algorithm of the key.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `encodedKey` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the key, which is assumed to be encoded according to the X.509 standard. The contents of the array are copied to protect against subsequent modification. |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm name of the encoded public key See the KeyFactory section in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html#keyfactory-algorithms) for information about standard algorithm names. |

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

Returns the key bytes, encoded according to the X.509 standard.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the X.509 encoding of the key. Returns a new array each time this method is called. |

### getFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormat(): String!
```

Returns the name of the encoding format associated with this key specification.

| Return ||
|-----------------------------------------------------------------------------------|----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string`"X.509"`. |
