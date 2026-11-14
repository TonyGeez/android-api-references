# SecretKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecretKey

```
interface SecretKey : Destroyable, Key
```

| [javax.crypto.SecretKey](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey#) |

| Known Direct Subclasses [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey), [SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec) |-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [PBEKey](https://developer.android.com/reference/kotlin/javax/crypto/interfaces/PBEKey) | The interface to a PBE key. | | [SecretKeySpec](https://developer.android.com/reference/kotlin/javax/crypto/spec/SecretKeySpec) | This class specifies a secret key in a provider-independent fashion. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A secret (symmetric) key. The purpose of this interface is to group (and provide type safety for) all secret key interfaces.

Provider implementations of this interface must overwrite the`equals`and`hashCode`methods inherited from [java.lang.Object](https://developer.android.com/reference/kotlin/java/lang/Object.html#), so that secret keys are compared based on their underlying key material and not based on reference. Implementations should override the default`destroy`and`isDestroyed`methods from the [javax.security.auth.Destroyable](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#) interface to enable sensitive key information to be destroyed, cleared, or in the case where such information is immutable, unreferenced. Finally, since`SecretKey`is`Serializable`, implementations should also override [java.io.ObjectOutputStream#writeObject(java.lang.Object)](https://developer.android.com/reference/kotlin/java/io/ObjectOutputStream.html#writeObject(kotlin.Any))to prevent keys that have been destroyed from being serialized.

Keys that implement this interface return the string`RAW`as their encoding format (see`getFormat`), and return the raw key bytes as the result of a`getEncoded`method call. (The`getFormat`and`getEncoded`methods are inherited from the [java.security.Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) parent interface.)

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [serialVersionUID](https://developer.android.com/reference/kotlin/javax/crypto/SecretKey#serialVersionUID:kotlin.Long) The class fingerprint that is set to indicate serialization compatibility since J2SE 1. |

| Inherited functions ||
|---|---|
| From class [Destroyable](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [destroy](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#destroy())`()` <br /> Destroy this`Object`. Sensitive information associated with this`Object`is destroyed or cleared. Subsequent calls to certain methods on this`Object`will result in an`IllegalStateException`being thrown. The default implementation throws`DestroyFailedException`. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDestroyed](https://developer.android.com/reference/kotlin/javax/security/auth/Destroyable.html#isDestroyed())`()` <br /> Determine if this`Object`has been destroyed. The default implementation returns false. Android note: Up to and including API 25 this method did not have a default implementation. Implementations of this interface must provide a concrete implementation of this method in order to work on older versions of Android. <br /> | ||
| From class [Key](https://developer.android.com/reference/kotlin/java/security/Key.html#) |------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getAlgorithm](https://developer.android.com/reference/kotlin/java/security/Key.html#getAlgorithm())`()` <br /> Returns the standard algorithm name for this key. For example, "DSA" would indicate that this key is a DSA key. See the key related sections (KeyFactory, KeyGenerator, KeyPairGenerator, and SecretKeyFactory) in the [Java Security Standard Algorithm Names Specification](https://docs.oracle.com/en/java/javase/17/docs/specs/security/standard-names.html) for information about standard key algorithm names. <br /> | | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getEncoded](https://developer.android.com/reference/kotlin/java/security/Key.html#getEncoded())`()` <br /> Returns the key in its primary encoding format, or null if this key does not support encoding. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFormat](https://developer.android.com/reference/kotlin/java/security/Key.html#getFormat())`()` <br /> Returns the name of the primary encoding format of this key, or null if this key does not support encoding. The primary encoding format is named in terms of the appropriate ASN.1 data format, if an ASN.1 specification for this key exists. For example, the name of the ASN.1 data format for public keys is*SubjectPublicKeyInfo* , as defined by the X.509 standard; in this case, the returned format is`"X.509"`. Similarly, the name of the ASN.1 data format for private keys is*PrivateKeyInfo* , as defined by the PKCS #8 standard; in this case, the returned format is`"PKCS#8"`. <br /> | ||

## Constants

### serialVersionUID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val serialVersionUID: Long
```

The class fingerprint that is set to indicate serialization compatibility since J2SE 1.4. 

 Value: -4795878709595146952L
