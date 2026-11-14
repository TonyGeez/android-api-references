# KeyRep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyRep

```
open class KeyRep : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.KeyRep](KeyRep.md) |

Standardized representation for serialized Key objects.

Note that a serialized Key may contain sensitive information which should not be exposed in untrusted environments. See the [Security Appendix](https://docs.oracle.com/en/java/javase/17/docs/specs/serialization/security.html) of the Serialization Specification for more information.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------|
| | [Type](../java/security/KeyRep.Type.md) Key type. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyRep](KeyRep.md))`(`type:` ` [KeyRep.Type](../java/security/KeyRep.Type.md)!`, `algorithm:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `format:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `encoded:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Construct the alternate Key class. |

| Protected methods ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [readResolve](KeyRep.md))`()` Resolve the Key object. |

## Public constructors

### KeyRep

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyRep(
    type: KeyRep.Type!, 
    algorithm: String!, 
    format: String!, 
    encoded: ByteArray!)
```

Construct the alternate Key class.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [KeyRep.Type](../java/security/KeyRep.Type.md)!:either one of Type.SECRET, Type.PUBLIC, or Type.PRIVATE |
| `algorithm` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the algorithm returned from`Key.getAlgorithm()` |
| `format` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the encoding format returned from`Key.getFormat()` |
| --- | --- |
| `encoded` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the encoded bytes returned from`Key.getEncoded()` |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if type is`null`, if algorithm is`null`, if format is`null`, or if encoded is`null` |

## Protected methods

### readResolve

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun readResolve(): Any!
```

Resolve the Key object.

This method supports three Type/format combinations:

- Type.SECRET/"RAW" - returns a SecretKeySpec object constructed using encoded key bytes and algorithm
- Type.PUBLIC/"X.509" - gets a KeyFactory instance for the key algorithm, constructs an X509EncodedKeySpec with the encoded key bytes, and generates a public key from the spec
- Type.PRIVATE/"PKCS#8" - gets a KeyFactory instance for the key algorithm, constructs a PKCS8EncodedKeySpec with the encoded key bytes, and generates a private key from the spec

| Return ||
|-----------------------------------------------------------------------------|-------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the resolved Key object |

| Exceptions ||
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.ObjectStreamException` | if the Type/format combination is unrecognized, if the algorithm, key format, or encoded key bytes are unrecognized/invalid, of if the resolution of the key fails for any reason |
