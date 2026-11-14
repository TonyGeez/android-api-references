# SignedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignedObject

```
class SignedObject : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.SignedObject](https://developer.android.com/reference/kotlin/java/security/SignedObject#) |

SignedObject is a class for the purpose of creating authentic runtime objects whose integrity cannot be compromised without being detected.

More specifically, a SignedObject contains another Serializable object, the (to-be-)signed object and its signature.

The signed object is a "deep copy" (in serialized form) of an original object. Once the copy is made, further manipulation of the original object has no side effect on the copy.

The underlying signing algorithm is designated by the Signature object passed to the constructor and the`verify`method. A typical usage for signing is the following: 

```kotlin
<code>Signature signingEngine = Signature.getInstance(algorithm,
                                                  provider);
  SignedObject so = new SignedObject(myobject, signingKey,
                                     signingEngine);
  </code>
```

A typical usage for verification is the following (having received SignedObject`so`): 

```kotlin
<code>Signature verificationEngine =
      Signature.getInstance(algorithm, provider);
  if (so.verify(publickey, verificationEngine))
      try {
          Object myobj = so.getObject();
      } catch (java.lang.ClassNotFoundException e) {};
  </code>
```

Several points are worth noting. First, there is no need to initialize the signing or verification engine, as it will be re-initialized inside the constructor and the`verify`method. Secondly, for verification to succeed, the specified public key must be the public key corresponding to the private key used to generate the SignedObject.

More importantly, for flexibility reasons, the constructor and`verify`method allow for customized signature engines, which can implement signature algorithms that are not installed formally as part of a crypto provider. However, it is crucial that the programmer writing the verifier code be aware what`Signature`engine is being used, as its own implementation of the`verify`method is invoked to verify a signature. In other words, a malicious`Signature`may choose to always return true on verification in an attempt to bypass a security check.

The signature algorithm can be, among others, the NIST standard DSA, using DSA and SHA-256. The algorithm is specified using the same convention as that for signatures. The DSA algorithm using the SHA-256 message digest algorithm can be specified, for example, as "SHA256withDSA". In the case of RSA the signing algorithm could be specified as, for example, "SHA256withRSA". The algorithm name must be specified, as there is no default.

The name of the Cryptography Package Provider is designated also by the Signature parameter to the constructor and the`verify`method. If the provider is not specified, the default provider is used. Each installation can be configured to use a particular provider as default.

Potential applications of SignedObject include:

- It can be used internally to any Java runtime as an unforgeable authorization token -- one that can be passed around without the fear that the token can be maliciously modified without being detected.
- It can be used to sign and serialize data/object for storage outside the Java runtime (e.g., storing critical access control data on disk).
- Nested SignedObjects can be used to construct a logical sequence of signatures, resembling a chain of authorization and delegation.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignedObject](https://developer.android.com/reference/kotlin/java/security/SignedObject#SignedObject(java.io.Serializable,%20java.security.PrivateKey,%20java.security.Signature))`(`object:` ` [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)!`, `signingKey:` ` [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)!`, `signingEngine:` ` [Signature](https://developer.android.com/reference/kotlin/java/security/Signature)!`)` Constructs a SignedObject from any Serializable object. |

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/SignedObject#getAlgorithm())`()` Retrieves the name of the signature algorithm. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getObject](https://developer.android.com/reference/kotlin/java/security/SignedObject#getObject())`()` Retrieves the encapsulated object. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getSignature](https://developer.android.com/reference/kotlin/java/security/SignedObject#getSignature())`()` Retrieves the signature on the signed object, in the form of a byte array. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [verify](https://developer.android.com/reference/kotlin/java/security/SignedObject#verify(java.security.PublicKey,%20java.security.Signature))`(`verificationKey:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!`, `verificationEngine:` ` [Signature](https://developer.android.com/reference/kotlin/java/security/Signature)!`)` Verifies that the signature in this SignedObject is the valid signature for the object stored inside, with the given verification key, using the designated verification engine. |

## Public constructors

### SignedObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignedObject(
    object: Serializable!, 
    signingKey: PrivateKey!, 
    signingEngine: Signature!)
```

Constructs a SignedObject from any Serializable object. The given object is signed with the given signing key, using the designated signature engine.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------|
| `object` | [Serializable](https://developer.android.com/reference/kotlin/java/io/Serializable.html#)!:the object to be signed. |
| `signingKey` | [PrivateKey](https://developer.android.com/reference/kotlin/java/security/PrivateKey)!:the private key for signing. |
| `signingEngine` | [Signature](https://developer.android.com/reference/kotlin/java/security/Signature)!:the signature signing engine. |

| Exceptions ||
|-------------------------------------|-----------------------------------------|
| `java.io.IOException` | if an error occurs during serialization |
| `java.security.InvalidKeyException` | if the key is invalid. |
| `java.security.SignatureException` | if signing fails. |

## Public methods

### getAlgorithm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAlgorithm(): String!
```

Retrieves the name of the signature algorithm.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the signature algorithm name. |

### getObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObject(): Any!
```

Retrieves the encapsulated object. The encapsulated object is de-serialized before it is returned.

| Return ||
|-----------------------------------------------------------------------------|--------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the encapsulated object. |

| Exceptions ||
|------------------------------------|--------------------------------------------|
| `java.io.IOException` | if an error occurs during de-serialization |
| `java.lang.ClassNotFoundException` | if an error occurs during de-serialization |

### getSignature

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignature(): ByteArray!
```

Retrieves the signature on the signed object, in the form of a byte array.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the signature. Returns a new array each time this method is called. |

### verify

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun verify(
    verificationKey: PublicKey!, 
    verificationEngine: Signature!
): Boolean
```

Verifies that the signature in this SignedObject is the valid signature for the object stored inside, with the given verification key, using the designated verification engine.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------|
| `verificationKey` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!:the public key for verification. |
| `verificationEngine` | [Signature](https://developer.android.com/reference/kotlin/java/security/Signature)!:the signature verification engine. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the signature is valid,`false`otherwise |

| Exceptions ||
|-------------------------------------|-------------------------------------|
| `java.security.SignatureException` | if signature verification failed. |
| `java.security.InvalidKeyException` | if the verification key is invalid. |
