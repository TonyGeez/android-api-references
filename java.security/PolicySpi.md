# PolicySpi

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PolicySpi

```
abstract class PolicySpi
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.PolicySpi](https://developer.android.com/reference/kotlin/java/security/PolicySpi#) |

This class defines the*Service Provider Interface* (**SPI** ) for the`Policy`class. All the abstract methods in this class must be implemented by each service provider who wishes to supply a Policy implementation.

Subclass implementations of this abstract class must provide a public constructor that takes a`Policy.Parameters`object as an input parameter. This constructor also must throw an IllegalArgumentException if it does not understand the`Policy.Parameters`input.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------|---|
| [PolicySpi](https://developer.android.com/reference/kotlin/java/security/PolicySpi#PolicySpi())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [engineGetPermissions](https://developer.android.com/reference/kotlin/java/security/PolicySpi#engineGetPermissions(java.security.CodeSource))`(`codesource:` ` [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)!`)` Return a PermissionCollection object containing the set of permissions granted to the specified CodeSource. |
| open [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | [engineGetPermissions](https://developer.android.com/reference/kotlin/java/security/PolicySpi#engineGetPermissions(java.security.ProtectionDomain))`(`domain:` ` [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!`)` Return a PermissionCollection object containing the set of permissions granted to the specified ProtectionDomain. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [engineImplies](https://developer.android.com/reference/kotlin/java/security/PolicySpi#engineImplies(java.security.ProtectionDomain,%20java.security.Permission))`(`domain:` ` [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!`, `permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!`)` Check whether the policy has granted a Permission to a ProtectionDomain. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [engineRefresh](https://developer.android.com/reference/kotlin/java/security/PolicySpi#engineRefresh())`()` Refreshes/reloads the policy configuration. |

## Public constructors

### PolicySpi

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PolicySpi()
```

## Protected methods

### engineGetPermissions

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetPermissions(codesource: CodeSource!): PermissionCollection!
```

Return a PermissionCollection object containing the set of permissions granted to the specified CodeSource.

The default implementation of this method returns Policy.UNSUPPORTED_EMPTY_COLLECTION object. This method can be overridden if the policy implementation can return a set of permissions granted to a CodeSource.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codesource` | [CodeSource](https://developer.android.com/reference/kotlin/java/security/CodeSource)!:the CodeSource to which the returned PermissionCollection has been granted. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | a set of permissions granted to the specified CodeSource. If this operation is supported, the returned set of permissions must be a new mutable instance and it must support heterogeneous Permission types. If this operation is not supported, Policy.UNSUPPORTED_EMPTY_COLLECTION is returned. |

### engineGetPermissions

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineGetPermissions(domain: ProtectionDomain!): PermissionCollection!
```

Return a PermissionCollection object containing the set of permissions granted to the specified ProtectionDomain.

The default implementation of this method returns Policy.UNSUPPORTED_EMPTY_COLLECTION object. This method can be overridden if the policy implementation can return a set of permissions granted to a ProtectionDomain.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `domain` | [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!:the ProtectionDomain to which the returned PermissionCollection has been granted. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection)! | a set of permissions granted to the specified ProtectionDomain. If this operation is supported, the returned set of permissions must be a new mutable instance and it must support heterogeneous Permission types. If this operation is not supported, Policy.UNSUPPORTED_EMPTY_COLLECTION is returned. |

### engineImplies

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun engineImplies(
    domain: ProtectionDomain!, 
    permission: Permission!
): Boolean
```

Check whether the policy has granted a Permission to a ProtectionDomain.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `domain` | [ProtectionDomain](https://developer.android.com/reference/kotlin/java/security/ProtectionDomain)!:the ProtectionDomain to check. |
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!:check whether this permission is granted to the specified domain. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean true if the permission is granted to the domain. |

### engineRefresh

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun engineRefresh(): Unit
```

Refreshes/reloads the policy configuration. The behavior of this method depends on the implementation. For example, calling`refresh`on a file-based policy will cause the file to be re-read.

The default implementation of this method does nothing. This method should be overridden if a refresh operation is supported by the policy implementation.
