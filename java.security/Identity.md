# Identity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Identity

```
abstract class Identity : Principal, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.security.Identity](../java/security/Identity.md) |

| Known Direct Subclasses [IdentityScope](../java/security/IdentityScope.md), [Signer](../java/security/Signer.md) |---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------| | [IdentityScope](../java/security/IdentityScope.md) | This class represents a scope for identities. | | [Signer](../java/security/Signer.md) | This class is used to represent an Identity that can also digitally sign data. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 3.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.KeyStore`, the`java.security.cert`package, and`java.security.Principal`.

This class represents identities: real-world objects such as people, companies or organizations whose identities can be authenticated using their public keys. Identities may also be more abstract (or concrete) constructs, such as daemon threads or smart cards.

All Identity objects have a name and a public key. Names are immutable. Identities may also be scoped. That is, if an Identity is specified to have a particular scope, then the name and public key of the Identity are unique within that scope.

An Identity also has a set of certificates (all certifying its own public key). The Principal names specified in these certificates need not be the same, only the key.

An Identity can be subclassed, to include postal and email addresses, telephone numbers, images of faces and logos, and so on.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Identity](../java/security/Identity.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an identity with the specified name and no scope. |
| [Identity](../java/security/Identity.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scope:` ` [IdentityScope](../java/security/IdentityScope.md)!`)` Constructs an identity with the specified name and scope. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------|---|
| [Identity](../java/security/Identity.md))`()` Constructor for serialization only. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertificate](../java/security/Identity.md))`(`certificate:` ` [Certificate](../java/security/Certificate.md)!`)` Adds a certificate for this identity. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java/security/Certificate.md)!\>! | [certificates](../java/security/Identity.md))`()` Returns a copy of all the certificates for this identity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/security/Identity.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Tests for equality between the specified object and this identity. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfo](../java/security/Identity.md))`()` Returns general information previously specified for this identity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java/security/Identity.md))`()` Returns this identity's name. |
| open [PublicKey](../java/security/PublicKey.md)! | [getPublicKey](../java/security/Identity.md))`()` Returns this identity's public key. |
| --- | --- |
| [IdentityScope](../java/security/IdentityScope.md)! | [getScope](../java/security/Identity.md))`()` Returns this identity's scope. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/security/Identity.md))`()` Returns a hashcode for this identity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCertificate](../java/security/Identity.md))`(`certificate:` ` [Certificate](../java/security/Certificate.md)!`)` Removes a certificate from this identity. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfo](../java/security/Identity.md))`(`info:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Specifies a general information string for this identity. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicKey](../java/security/Identity.md))`(`key:` ` [PublicKey](../java/security/PublicKey.md)!`)` Sets this identity's public key. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/security/Identity.md))`()` Returns a short string describing this identity, telling its name and its scope (if any). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../java/security/Identity.md))`(`detailed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a string representation of this identity, with optionally more details than that provided by the`toString`method without any arguments. |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [identityEquals](../java/security/Identity.md))`(`identity:` ` [Identity](../java/security/Identity.md)!`)` Tests for equality between the specified identity and this identity. |

| Inherited functions ||
|---|---|
| From class [Principal](../java/security/Principal.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java/security/Principal.md))`(`subject:` ` [Subject](../javax/security/auth/Subject.md)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

## Public constructors

### Identity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Identity(name: String!)
```

Constructs an identity with the specified name and no scope.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the identity name. |

### Identity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Identity(
    name: String!, 
    scope: IdentityScope!)
```

Constructs an identity with the specified name and scope.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the identity name. |
| `scope` | [IdentityScope](../java/security/IdentityScope.md)!:the scope of the identity. |

| Exceptions ||
|----------------------------------------|------------------------------------------------------------------|
| `java.security.KeyManagementException` | if there is already an identity with the same name in the scope. |

## Protected constructors

### Identity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected Identity()
```

Constructor for serialization only.

## Public methods

### addCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addCertificate(certificate: Certificate!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds a certificate for this identity. If the identity has a public key, the public key in the certificate must be the same, and if the identity does not have a public key, the identity's public key is set to be that specified in the certificate.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"addIdentityCertificate"`as its argument to see if it's ok to add a certificate.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `certificate` | [Certificate](../java/security/Certificate.md)!:the certificate to be added. |

| Exceptions ||
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.KeyManagementException` | if the certificate is not valid, if the public key in the certificate being added conflicts with this identity's public key, or if another exception occurs. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow adding a certificate. |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md)) 

### certificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun certificates(): Array<Certificate!>!
```

**Deprecated:** *Deprecated in Java.*

Returns a copy of all the certificates for this identity.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](../java/security/Certificate.md)!>! | a copy of all the certificates for this identity. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

**Deprecated:** *Deprecated in Java.*

Tests for equality between the specified object and this identity. This first tests to see if the entities actually refer to the same object, in which case it returns true. Next, it checks to see if the entities have the same name and the same scope. If they do, the method returns true. Otherwise, it calls [identityEquals](../java/security/Identity.md)), which subclasses should override.

| Parameters ||
|------------|-----------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `another` | principal to compare with. |
| `identity` | the object to test for equality with this identity. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the objects are considered equal, false otherwise. |

**See Also**

- [#identityEquals](../java/security/Identity.md)) 

### getInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInfo(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns general information previously specified for this identity.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | general information about this identity. |

**See Also**

- [#setInfo](../java/security/Identity.md)) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns this identity's name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this identity. |

### getPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPublicKey(): PublicKey!
```

**Deprecated:** *Deprecated in Java.*

Returns this identity's public key.

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------|
| [PublicKey](../java/security/PublicKey.md)! | the public key for this identity. |

**See Also**

- [#setPublicKey](../java/security/Identity.md)) 

### getScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScope(): IdentityScope!
```

**Deprecated:** *Deprecated in Java.*

Returns this identity's scope.

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------|
| [IdentityScope](../java/security/IdentityScope.md)! | the scope of this identity. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns a hashcode for this identity.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hashcode for this identity. |

### removeCertificate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeCertificate(certificate: Certificate!): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes a certificate from this identity.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"removeIdentityCertificate"`as its argument to see if it's ok to remove a certificate.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| `certificate` | [Certificate](../java/security/Certificate.md)!:the certificate to be removed. |

| Exceptions ||
|----------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.security.KeyManagementException` | if the certificate is missing, or if another exception occurs. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow removing a certificate. |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md)) 

### setInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInfo(info: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Specifies a general information string for this identity.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityInfo"`as its argument to see if it's ok to specify the information string.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------|
| `info` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the information string. |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow setting the information string. |

**See Also**

- [#getInfo](../java/security/Identity.md))
- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md)) 

### setPublicKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPublicKey(key: PublicKey!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets this identity's public key. The old key and all of this identity's certificates are removed by this operation.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityPublicKey"`as its argument to see if it's ok to set the public key.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](../java/security/PublicKey.md)!:the public key for this identity. |

| Exceptions ||
|----------------------------------------|-------------------------------------------------------------------------------------------------------|
| `java.security.KeyManagementException` | if another identity in the identity's scope has the same public key, or if another exception occurs. |
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow setting the public key. |

**See Also**

- [#getPublicKey](../java/security/Identity.md))
- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a short string describing this identity, telling its name and its scope (if any).

First, if there is a security manager, its`checkSecurityAccess`method is called with`"printIdentity"`as its argument to see if it's ok to return the string.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | information about this identity, such as its name and the name of its scope (if any). |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow returning a string describing this identity. |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md)) 

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(detailed: Boolean): String!
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of this identity, with optionally more details than that provided by the`toString`method without any arguments.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"printIdentity"`as its argument to see if it's ok to return the string.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------|
| `detailed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether or not to provide detailed information. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | information about this identity. If`detailed`is true, then this method returns more information than that provided by the`toString`method without any arguments. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow returning a string describing this identity. |

**See Also**

- [java.lang.SecurityManager#checkSecurityAccess](../java/lang/SecurityManager.md))

## Protected methods

### identityEquals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun identityEquals(identity: Identity!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Tests for equality between the specified identity and this identity. This method should be overriden by subclasses to test for equality. The default behavior is to return true if the names and public keys are equal.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `identity` | [Identity](../java/security/Identity.md)!:the identity to test for equality with this identity. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the identities are considered equal, false otherwise. |

**See Also**

- [#equals](../java/security/Identity.md))
