# AclEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntry

```
interface AclEntry : Cloneable
```

| [java.security.acl.AclEntry](../java/security/acl/AclEntry.md) |

| **This interface was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

This is the interface used for representing one entry in an Access Control List (ACL).

An ACL can be thought of as a data structure with multiple ACL entry objects. Each ACL entry object contains a set of permissions associated with a particular principal. (A principal represents an entity such as an individual user or a group). Additionally, each ACL entry is specified as being either positive or negative. If positive, the permissions are to be granted to the associated principal. If negative, the permissions are to be denied. Each principal can have at most one positive ACL entry and one negative entry; that is, multiple positive or negative ACL entries are not allowed for any principal. Note: ACL entries are by default positive. An entry becomes a negative entry only if the [setNegativePermissions](../java/security/acl/AclEntry.md))method is called on it.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addPermission](../java/security/acl/AclEntry.md))`(`permission:` ` [Permission](../java/security/acl/Permission.md)!`)` Adds the specified permission to this ACL entry. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkPermission](../java/security/acl/AclEntry.md))`(`permission:` ` [Permission](../java/security/acl/Permission.md)!`)` Checks if the specified permission is part of the permission set in this entry. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/security/acl/AclEntry.md))`()` Clones this ACL entry. |
| --- | --- |
| abstract [Principal](../java/security/Principal.md)! | [getPrincipal](../java/security/acl/AclEntry.md))`()` Returns the principal for which permissions are granted or denied by this ACL entry. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNegative](../java/security/acl/AclEntry.md))`()` Returns true if this is a negative ACL entry (one denying the associated principal the set of permissions in the entry), false otherwise. |
| abstract [Enumeration](../java/util/Enumeration.md)\< [Permission](../java/security/acl/Permission.md)!\>! | [permissions](../java/security/acl/AclEntry.md))`()` Returns an enumeration of the permissions in this ACL entry. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removePermission](../java/security/acl/AclEntry.md))`(`permission:` ` [Permission](../java/security/acl/Permission.md)!`)` Removes the specified permission from this ACL entry. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativePermissions](../java/security/acl/AclEntry.md))`()` Sets this ACL entry to be a negative one. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPrincipal](../java/security/acl/AclEntry.md))`(`user:` ` [Principal](../java/security/Principal.md)!`)` Specifies the principal for which permissions are granted or denied by this ACL entry. |
| --- | --- |

## Public methods

### addPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addPermission(permission: Permission!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds the specified permission to this ACL entry. Note: An entry can have multiple permissions.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](../java/security/acl/Permission.md)!:the permission to be associated with the principal in this entry. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the permission was added, false if the permission was already part of this entry's permission set. |

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkPermission(permission: Permission!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the specified permission is part of the permission set in this entry.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](../java/security/acl/Permission.md)!:the permission to be checked for. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the permission is part of the permission set in this entry, false otherwise. |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Any
```

**Deprecated:** *Deprecated in Java.*

Clones this ACL entry.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this ACL entry. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPrincipal(): Principal!
```

**Deprecated:** *Deprecated in Java.*

Returns the principal for which permissions are granted or denied by this ACL entry. Returns null if there is no principal set for this entry yet.

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------|
| [Principal](../java/security/Principal.md)! | the principal associated with this entry. |

**See Also**

- [#setPrincipal](../java/security/acl/AclEntry.md)) 

### isNegative

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isNegative(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if this is a negative ACL entry (one denying the associated principal the set of permissions in the entry), false otherwise.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is a negative ACL entry, false if it's not. |

### permissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun permissions(): Enumeration<Permission!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration of the permissions in this ACL entry.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [Enumeration](../java/util/Enumeration.md)< [Permission](../java/security/acl/Permission.md)!>! | an enumeration of the permissions in this ACL entry. |

### removePermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removePermission(permission: Permission!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes the specified permission from this ACL entry.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `permission` | [Permission](../java/security/acl/Permission.md)!:the permission to be removed from this entry. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the permission is removed, false if the permission was not part of this entry's permission set. |

### setNegativePermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNegativePermissions(): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets this ACL entry to be a negative one. That is, the associated principal (e.g., a user or a group) will be denied the permission set specified in the entry. Note: ACL entries are by default positive. An entry becomes a negative entry only if this`setNegativePermissions`method is called on it. 

### setPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPrincipal(user: Principal!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Specifies the principal for which permissions are granted or denied by this ACL entry. If a principal was already set for this ACL entry, false is returned, otherwise true is returned.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `user` | [Principal](../java/security/Principal.md)!:the principal to be set for this entry. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the principal is set, false if there was already a principal set for this entry. |

**See Also**

- [#getPrincipal](../java/security/acl/AclEntry.md))
