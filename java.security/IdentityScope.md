# IdentityScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityScope

```
abstract class IdentityScope : Identity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.security.Identity](https://developer.android.com/reference/kotlin/java/security/Identity) ||
| | ↳ | [java.security.IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#) |

| **This class was deprecated in API level 3.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.KeyStore`, the`java.security.cert`package, and`java.security.Principal`.

This class represents a scope for identities. It is an Identity itself, and therefore has a name and can have a scope. It can also optionally have a public key and associated certificates.

An IdentityScope can contain Identity objects of all kinds, including Signers. All types of Identity objects can be retrieved, added, and removed using the same methods. Note that it is possible, and in fact expected, that different types of identity scopes will apply different policies for their various operations on the various types of Identities.

There is a one-to-one mapping between keys and identities, and there can only be one copy of one key per scope. For example, suppose**Acme Software, Inc**is a software publisher known to a user. Suppose it is an Identity, that is, it has a public key, and a set of associated certificates. It is named in the scope using the name "Acme Software". No other named Identity in the scope has the same public key. Of course, none has the same name as well.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#IdentityScope(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new identity scope with the specified name. |
| [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#IdentityScope(kotlin.String,%20java.security.IdentityScope))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scope:` ` [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)!`)` Constructs a new identity scope with the specified name and scope. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#IdentityScope())`()` This constructor is used for serialization only and should not be used by subclasses. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIdentity](https://developer.android.com/reference/kotlin/java/security/IdentityScope#addIdentity(java.security.Identity))`(`identity:` ` [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!`)` Adds an identity to this identity scope. |
| abstract [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | [getIdentity](https://developer.android.com/reference/kotlin/java/security/IdentityScope#getIdentity(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the identity in this scope with the specified name (if any). |
| open [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | [getIdentity](https://developer.android.com/reference/kotlin/java/security/IdentityScope#getIdentity(java.security.Principal))`(`principal:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)!`)` Retrieves the identity whose name is the same as that of the specified principal. |
| abstract [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | [getIdentity](https://developer.android.com/reference/kotlin/java/security/IdentityScope#getIdentity(java.security.PublicKey))`(`key:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!`)` Retrieves the identity with the specified public key. |
| openstatic [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)! | [getSystemScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#getSystemScope())`()` Returns the system's identity scope. |
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!\>! | [identities](https://developer.android.com/reference/kotlin/java/security/IdentityScope#identities())`()` Returns an enumeration of all identities in this identity scope. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeIdentity](https://developer.android.com/reference/kotlin/java/security/IdentityScope#removeIdentity(java.security.Identity))`(`identity:` ` [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!`)` Removes an identity from this identity scope. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/security/IdentityScope#size())`()` Returns the number of identities within this identity scope. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/security/IdentityScope#toString())`()` Returns a string representation of this identity scope, including its name, its scope name, and the number of identities in this identity scope. |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#setSystemScope(java.security.IdentityScope))`(`scope:` ` [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)!`)` Sets the system's identity scope. |

| Inherited functions ||
|---|---|
| From class [Identity](https://developer.android.com/reference/kotlin/java/security/Identity) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertificate](https://developer.android.com/reference/kotlin/java/security/Identity#addCertificate(java.security.Certificate))`(`certificate:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/Certificate)!`)` <br /> Adds a certificate for this identity. If the identity has a public key, the public key in the certificate must be the same, and if the identity does not have a public key, the identity's public key is set to be that specified in the certificate. First, if there is a security manager, its`checkSecurityAccess`method is called with`"addIdentityCertificate"`as its argument to see if it's ok to add a certificate. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](https://developer.android.com/reference/kotlin/java/security/Certificate)!>! | [certificates](https://developer.android.com/reference/kotlin/java/security/Identity#certificates())`()` <br /> Returns a copy of all the certificates for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/security/Identity#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Tests for equality between the specified object and this identity. This first tests to see if the entities actually refer to the same object, in which case it returns true. Next, it checks to see if the entities have the same name and the same scope. If they do, the method returns true. Otherwise, it calls [identityEquals](https://developer.android.com/reference/kotlin/java/security/Identity#identityEquals(java.security.Identity)), which subclasses should override. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfo](https://developer.android.com/reference/kotlin/java/security/Identity#getInfo())`()` <br /> Returns general information previously specified for this identity. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Identity#getName())`()` <br /> Returns this identity's name. <br /> | | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)! | [getPublicKey](https://developer.android.com/reference/kotlin/java/security/Identity#getPublicKey())`()` <br /> Returns this identity's public key. <br /> | | [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)! | [getScope](https://developer.android.com/reference/kotlin/java/security/Identity#getScope())`()` <br /> Returns this identity's scope. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/security/Identity#hashCode())`()` <br /> Returns a hashcode for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [identityEquals](https://developer.android.com/reference/kotlin/java/security/Identity#identityEquals(java.security.Identity))`(`identity:` ` [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!`)` <br /> Tests for equality between the specified identity and this identity. This method should be overriden by subclasses to test for equality. The default behavior is to return true if the names and public keys are equal. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCertificate](https://developer.android.com/reference/kotlin/java/security/Identity#removeCertificate(java.security.Certificate))`(`certificate:` ` [Certificate](https://developer.android.com/reference/kotlin/java/security/Certificate)!`)` <br /> Removes a certificate from this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"removeIdentityCertificate"`as its argument to see if it's ok to remove a certificate. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfo](https://developer.android.com/reference/kotlin/java/security/Identity#setInfo(kotlin.String))`(`info:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Specifies a general information string for this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityInfo"`as its argument to see if it's ok to specify the information string. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicKey](https://developer.android.com/reference/kotlin/java/security/Identity#setPublicKey(java.security.PublicKey))`(`key:` ` [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!`)` <br /> Sets this identity's public key. The old key and all of this identity's certificates are removed by this operation. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityPublicKey"`as its argument to see if it's ok to set the public key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](https://developer.android.com/reference/kotlin/java/security/Identity#toString(kotlin.Boolean))`(`detailed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Returns a string representation of this identity, with optionally more details than that provided by the`toString`method without any arguments. First, if there is a security manager, its`checkSecurityAccess`method is called with`"printIdentity"`as its argument to see if it's ok to return the string. <br /> | ||
| From class [Principal](https://developer.android.com/reference/kotlin/java/security/Principal) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/Principal#implies(javax.security.auth.Subject))`(`subject:` ` [Subject](https://developer.android.com/reference/kotlin/javax/security/auth/Subject.html#)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

## Public constructors

### IdentityScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityScope(name: String!)
```

Constructs a new identity scope with the specified name.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the scope name. |

### IdentityScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IdentityScope(
    name: String!, 
    scope: IdentityScope!)
```

Constructs a new identity scope with the specified name and scope.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the scope name. |
| `scope` | [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)!:the scope for the new identity scope. |

| Exceptions ||
|----------------------------------------|------------------------------------------------------------------|
| `java.security.KeyManagementException` | if there is already an identity with the same name in the scope. |

## Protected constructors

### IdentityScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected IdentityScope()
```

This constructor is used for serialization only and should not be used by subclasses.

## Public methods

### addIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addIdentity(identity: Identity!): Unit
```

**Deprecated:** *Deprecated in Java.*

Adds an identity to this identity scope.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `identity` | [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!:the identity to be added. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.security.KeyManagementException` | if the identity is not valid, a name conflict occurs, another identity has the same public key as the identity being added, or another exception occurs. |

### getIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIdentity(name: String!): Identity!
```

**Deprecated:** *Deprecated in Java.*

Returns the identity in this scope with the specified name (if any).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the identity to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | the identity named`name`, or null if there are no identities named`name`in this scope. |

### getIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentity(principal: Principal!): Identity!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the identity whose name is the same as that of the specified principal. (Note: Identity implements Principal.)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `principal` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal)!:the principal corresponding to the identity to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | the identity whose name is the same as that of the principal, or null if there are no identities of the same name in this scope. |

### getIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIdentity(key: PublicKey!): Identity!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the identity with the specified public key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](https://developer.android.com/reference/kotlin/java/security/PublicKey)!:the public key for the identity to be returned. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)! | the identity with the given key, or null if there are no identities in this scope with that key. |

### getSystemScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemScope(): IdentityScope!
```

**Deprecated:** *Deprecated in Java.*

Returns the system's identity scope.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)! | the system's identity scope, or`null`if none has been set. |

**See Also**

- [#setSystemScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#setSystemScope(java.security.IdentityScope)) 

### identities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun identities(): Enumeration<Identity!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration of all identities in this identity scope.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)< [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!>! | an enumeration of all identities in this identity scope. |

### removeIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeIdentity(identity: Identity!): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes an identity from this identity scope.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `identity` | [Identity](https://developer.android.com/reference/kotlin/java/security/Identity)!:the identity to be removed. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------|
| `java.security.KeyManagementException` | if the identity is missing, or another exception occurs. |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the number of identities within this identity scope.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of identities within this identity scope. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

Returns a string representation of this identity scope, including its name, its scope name, and the number of identities in this identity scope.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this identity scope. |

## Protected methods

### setSystemScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open static fun setSystemScope(scope: IdentityScope!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the system's identity scope.

First, if there is a security manager, its`checkSecurityAccess`method is called with`"setSystemScope"`as its argument to see if it's ok to set the identity scope.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------|
| `scope` | [IdentityScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#)!:the scope to set. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow setting the identity scope. |

**See Also**

- [#getSystemScope](https://developer.android.com/reference/kotlin/java/security/IdentityScope#getSystemScope())
- [java.lang.SecurityManager#checkSecurityAccess](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSecurityAccess(kotlin.String))
