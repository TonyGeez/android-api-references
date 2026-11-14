# IdentityScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdentityScope

```
abstract class IdentityScope : Identity
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.security.Identity](Identity.md) ||
| | ↳ | [java.security.IdentityScope](IdentityScope.md) |

| **This class was deprecated in API level 3.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.KeyStore`, the`java.security.cert`package, and`java.security.Principal`.

This class represents a scope for identities. It is an Identity itself, and therefore has a name and can have a scope. It can also optionally have a public key and associated certificates.

An IdentityScope can contain Identity objects of all kinds, including Signers. All types of Identity objects can be retrieved, added, and removed using the same methods. Note that it is possible, and in fact expected, that different types of identity scopes will apply different policies for their various operations on the various types of Identities.

There is a one-to-one mapping between keys and identities, and there can only be one copy of one key per scope. For example, suppose**Acme Software, Inc**is a software publisher known to a user. Suppose it is an Identity, that is, it has a public key, and a set of associated certificates. It is named in the scope using the name "Acme Software". No other named Identity in the scope has the same public key. Of course, none has the same name as well.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityScope](IdentityScope.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new identity scope with the specified name. |
| [IdentityScope](IdentityScope.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `scope:` ` [IdentityScope](IdentityScope.md)!`)` Constructs a new identity scope with the specified name and scope. |

| Protected constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IdentityScope](IdentityScope.md))`()` This constructor is used for serialization only and should not be used by subclasses. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addIdentity](IdentityScope.md))`(`identity:` ` [Identity](Identity.md)!`)` Adds an identity to this identity scope. |
| abstract [Identity](Identity.md)! | [getIdentity](IdentityScope.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the identity in this scope with the specified name (if any). |
| open [Identity](Identity.md)! | [getIdentity](IdentityScope.md))`(`principal:` ` [Principal](Principal.md)!`)` Retrieves the identity whose name is the same as that of the specified principal. |
| --- | --- |
| abstract [Identity](Identity.md)! | [getIdentity](IdentityScope.md))`(`key:` ` [PublicKey](PublicKey.md)!`)` Retrieves the identity with the specified public key. |
| openstatic [IdentityScope](IdentityScope.md)! | [getSystemScope](IdentityScope.md))`()` Returns the system's identity scope. |
| abstract [Enumeration](../java.util/Enumeration.md)\< [Identity](Identity.md)!\>! | [identities](IdentityScope.md))`()` Returns an enumeration of all identities in this identity scope. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeIdentity](IdentityScope.md))`(`identity:` ` [Identity](Identity.md)!`)` Removes an identity from this identity scope. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](IdentityScope.md))`()` Returns the number of identities within this identity scope. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](IdentityScope.md))`()` Returns a string representation of this identity scope, including its name, its scope name, and the number of identities in this identity scope. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSystemScope](IdentityScope.md))`(`scope:` ` [IdentityScope](IdentityScope.md)!`)` Sets the system's identity scope. |

| Inherited functions ||
|---|---|
| From class [Identity](Identity.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addCertificate](Identity.md))`(`certificate:` ` [Certificate](Certificate.md)!`)` <br /> Adds a certificate for this identity. If the identity has a public key, the public key in the certificate must be the same, and if the identity does not have a public key, the identity's public key is set to be that specified in the certificate. First, if there is a security manager, its`checkSecurityAccess`method is called with`"addIdentityCertificate"`as its argument to see if it's ok to add a certificate. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Certificate](Certificate.md)!>! | [certificates](Identity.md))`()` <br /> Returns a copy of all the certificates for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Identity.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Tests for equality between the specified object and this identity. This first tests to see if the entities actually refer to the same object, in which case it returns true. Next, it checks to see if the entities have the same name and the same scope. If they do, the method returns true. Otherwise, it calls [identityEquals](Identity.md)), which subclasses should override. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getInfo](Identity.md))`()` <br /> Returns general information previously specified for this identity. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](Identity.md))`()` <br /> Returns this identity's name. <br /> | | [PublicKey](PublicKey.md)! | [getPublicKey](Identity.md))`()` <br /> Returns this identity's public key. <br /> | | [IdentityScope](IdentityScope.md)! | [getScope](Identity.md))`()` <br /> Returns this identity's scope. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Identity.md))`()` <br /> Returns a hashcode for this identity. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [identityEquals](Identity.md))`(`identity:` ` [Identity](Identity.md)!`)` <br /> Tests for equality between the specified identity and this identity. This method should be overriden by subclasses to test for equality. The default behavior is to return true if the names and public keys are equal. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeCertificate](Identity.md))`(`certificate:` ` [Certificate](Certificate.md)!`)` <br /> Removes a certificate from this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"removeIdentityCertificate"`as its argument to see if it's ok to remove a certificate. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInfo](Identity.md))`(`info:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Specifies a general information string for this identity. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityInfo"`as its argument to see if it's ok to specify the information string. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPublicKey](Identity.md))`(`key:` ` [PublicKey](PublicKey.md)!`)` <br /> Sets this identity's public key. The old key and all of this identity's certificates are removed by this operation. First, if there is a security manager, its`checkSecurityAccess`method is called with`"setIdentityPublicKey"`as its argument to see if it's ok to set the public key. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](Identity.md))`(`detailed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Returns a string representation of this identity, with optionally more details than that provided by the`toString`method without any arguments. First, if there is a security manager, its`checkSecurityAccess`method is called with`"printIdentity"`as its argument to see if it's ok to return the string. <br /> | ||
| From class [Principal](Principal.md) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](Principal.md))`(`subject:` ` [Subject](../javax.security.auth/Subject.md)!`)` <br /> Returns true if the specified subject is implied by this principal. <br /> | ||

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
| `scope` | [IdentityScope](IdentityScope.md)!:the scope for the new identity scope. |

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
| `identity` | [Identity](Identity.md)!:the identity to be added. |

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
| [Identity](Identity.md)! | the identity named`name`, or null if there are no identities named`name`in this scope. |

### getIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIdentity(principal: Principal!): Identity!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the identity whose name is the same as that of the specified principal. (Note: Identity implements Principal.)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `principal` | [Principal](Principal.md)!:the principal corresponding to the identity to be retrieved. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Identity](Identity.md)! | the identity whose name is the same as that of the principal, or null if there are no identities of the same name in this scope. |

### getIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIdentity(key: PublicKey!): Identity!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the identity with the specified public key.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [PublicKey](PublicKey.md)!:the public key for the identity to be returned. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Identity](Identity.md)! | the identity with the given key, or null if there are no identities in this scope with that key. |

### getSystemScope

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getSystemScope(): IdentityScope!
```

**Deprecated:** *Deprecated in Java.*

Returns the system's identity scope.

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [IdentityScope](IdentityScope.md)! | the system's identity scope, or`null`if none has been set. |

**See Also**

- [#setSystemScope](IdentityScope.md)) 

### identities

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun identities(): Enumeration<Identity!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration of all identities in this identity scope.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Enumeration](../java.util/Enumeration.md)< [Identity](Identity.md)!>! | an enumeration of all identities in this identity scope. |

### removeIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeIdentity(identity: Identity!): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes an identity from this identity scope.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------|
| `identity` | [Identity](Identity.md)!:the identity to be removed. |

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
| `scope` | [IdentityScope](IdentityScope.md)!:the scope to set. |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | if a security manager exists and its`checkSecurityAccess`method doesn't allow setting the identity scope. |

**See Also**

- [#getSystemScope](IdentityScope.md))
- [java.lang.SecurityManager#checkSecurityAccess](../java.lang/SecurityManager.md))
