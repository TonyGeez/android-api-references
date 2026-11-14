# Signer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Signer

```
abstract class Signer : Identity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Identity](Identity.md) ||
| | ↳ | [java.security.Signer](Signer.md) |

| **This class was deprecated in API level 3.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.KeyStore`, the`java.security.cert`package, and`java.security.Principal`.

This class is used to represent an Identity that can also digitally sign data.

The management of a signer's private keys is an important and sensitive issue that should be handled by subclasses as appropriate to their intended use.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Signer](Signer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a signer with the specified identity name. |
| [Signer](Signer.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scope:` ` [IdentityScope](IdentityScope.md)!`)` Creates a signer with the specified identity name and scope. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [Signer](Signer.md))`()` Creates a signer. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PrivateKey](PrivateKey.md)! | [getPrivateKey](Signer.md))`()` Returns this signer's private key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeyPair](Signer.md))`(`pair:` ` [KeyPair](KeyPair.md)!`)` Sets the key pair (public key and private key) for this signer. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Signer.md))`()` Returns a string of information about the signer. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Identity](Identity.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertificate](Identity.md))`(`certificate:` ` [Certificate](Certificate.md)!`)` <br /> Adds a certificate for this identity. If the identity has a public key, the public key in the certificate must be the same, and if the identity does not have a public key, the identity's public key is set to be that specified in the certificate. First, if there is a security manager, its`checkSecurityAccess`method is called with`"addIdentityCertificate"`as its argument to see if it's ok to add a certificate. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](Certificate.md)!>! | [certificates](Identity.md))`()` <br /> Returns a copy of all the certificates for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Identity.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Tests for equality between the specified object and this identity. This first tests to see if the entities actually refer to the same object, in which case it returns true. Next, it checks to see if the entities have the same name and the same scope. If they do, the method returns true. Otherwise, it calls [identityEquals](Identity.md)), which subclasses should override. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfo](Identity.md))`()` <br /> Returns general information previously specified for this identity. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](Identity.md))`()` <br /> Returns this identity's name. <br /> | | [PublicKey](PublicKey.md)! | [getPublicKey](Identity.md))`()` <br /> Returns this identity's public key. <br /> | | [IdentityScope](IdentityScope.md)! | [getScope](Identity.md))`()` <br /> Returns this identity's scope. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Identity.md))`()` <br /> Returns a hashcode for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [identityEquals](Identity.md))`(`identity:` ` [Identity](Identity.md)!`)` <br /> Tests for equality between the specified identity and this identity. This method should be overriden by subclasses to test for equality. The default behavior is to return true if the names and public keys are equal. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCertificate](Identity.md))`(`certificate:` ` [Certificate](Certificate.md)!`)` <br /> Removes a certificate from this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"removeIdentityCertificate"`as its argument to see if it's ok to remove a certificate. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfo](Identity.md))`(`info:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Specifies a general information string for this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityInfo"`as its argument to see if it's ok to specify the information string. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicKey](Identity.md))`(`key:` ` [PublicKey](PublicKey.md)!`)` <br /> Sets this identity's public key. The old key and all of this identity's certificates are removed by this operation. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityPublicKey"`as its argument to see if it's ok to set the public key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](Identity.md))`(`detailed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Returns a string representation of this identity, with optionally more details than that provided by the`toString`method without any arguments. First, if there is a security manager, its`checkSecurityAccess`method is called with`"printIdentity"`as its argument to see if it's ok to return the string. <br /> | ||
| From class [Principal](Principal.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](Principal.md))`(`subject:` ` [Subject](../javax.security.auth/Subject.md)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

## Public constructors

### Signer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Signer(name: String!)
```

Creates a signer with the specified identity name.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the identity name. |

### Signer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Signer(
    name: String!, 
    scope: IdentityScope!)
```

Creates a signer with the specified identity name and scope.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the identity name. |
| `scope` | [IdentityScope](IdentityScope.md)!:the scope of the identity. |

| Exceptions ||
|----------------------------------------|------------------------------------------------------------------|
| `java.security.KeyManagementException` | if there is already an identity with the same name in the scope. |

## Protected constructors

### Signer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Signer()
```

Creates a signer. This constructor should only be used for serialization.

## Public methods

### getPrivateKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrivateKey(): PrivateKey!
```

**Deprecated:** *Deprecated in Java.*

Returns this signer's private key.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"getSignerPrivateKey"`as its argument to see if it's ok to return the private key.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [PrivateKey](PrivateKey.md)! | this signer's private key, or null if the private key has not yet been set. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow returning the private key. |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java.lang/SecurityManager.md)) 

### setKeyPair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setKeyPair(pair: KeyPair!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the key pair (public key and private key) for this signer.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"setSignerKeyPair"`as its argument to see if it's ok to set the key pair.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `pair` | [KeyPair](KeyPair.md)!:an initialized key pair. |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------|
| `java.security.InvalidParameterException` | if the key pair is not properly initialized. |
| `java.security.KeyException` | if the key pair cannot be set for any other reason. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow setting the key pair. |
| --- | --- |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java.lang/SecurityManager.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string of information about the signer.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string of information about the signer. |
