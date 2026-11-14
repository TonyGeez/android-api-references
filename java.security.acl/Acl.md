# Acl

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Acl

```
interface Acl : Owner
```

| [java.security.acl.Acl](https://developer.android.com/reference/kotlin/java/security/acl/Acl#) |

| **This interface was deprecated in API level 33.**
|
| This class is deprecated and subject to removal in a future version of Java SE. It has been replaced by`java.security.Policy`and related classes since 1.2.

Interface representing an Access Control List (ACL). An Access Control List is a data structure used to guard access to resources.

An ACL can be thought of as a data structure with multiple ACL entries. Each ACL entry, of interface type AclEntry, contains a set of permissions associated with a particular principal. (A principal represents an entity such as an individual user or a group). Additionally, each ACL entry is specified as being either positive or negative. If positive, the permissions are to be granted to the associated principal. If negative, the permissions are to be denied.

The ACL Entries in each ACL observe the following rules:

- Each principal can have at most one positive ACL entry and one negative entry; that is, multiple positive or negative ACL entries are not allowed for any principal. Each entry specifies the set of permissions that are to be granted (if positive) or denied (if negative).
- If there is no entry for a particular principal, then the principal is considered to have a null (empty) permission set.
- If there is a positive entry that grants a principal a particular permission, and a negative entry that denies the principal the same permission, the result is as though the permission was never granted or denied.
- Individual permissions always override permissions of the group(s) to which the individual belongs. That is, individual negative permissions (specific denial of permissions) override the groups' positive permissions. And individual positive permissions override the groups' negative permissions.

The`java.security.acl `package provides the interfaces to the ACL and related data structures (ACL entries, groups, permissions, etc.).

The`java.security.acl.Acl `interface extends the`java.security.acl.Owner `interface. The Owner interface is used to maintain a list of owners for each ACL. Only owners are allowed to modify an ACL. For example, only an owner can call the ACL's`addEntry`method to add a new ACL entry to the ACL.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addEntry](https://developer.android.com/reference/kotlin/java/security/acl/Acl#addEntry(java.security.Principal,%20java.security.acl.AclEntry))`(`caller:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `entry:` ` [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!`)` Adds an ACL entry to this ACL. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [checkPermission](https://developer.android.com/reference/kotlin/java/security/acl/Acl#checkPermission(java.security.Principal,%20java.security.acl.Permission))`(`principal:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `permission:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/acl/Permission)!`)` Checks whether or not the specified principal has the specified permission. |
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!\>! | [entries](https://developer.android.com/reference/kotlin/java/security/acl/Acl#entries())`()` Returns an enumeration of the entries in this ACL. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/acl/Acl#getName())`()` Returns the name of this ACL. |
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Permission](https://developer.android.com/reference/kotlin/java/security/acl/Permission)!\>! | [getPermissions](https://developer.android.com/reference/kotlin/java/security/acl/Acl#getPermissions(java.security.Principal))`(`user:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`)` Returns an enumeration for the set of allowed permissions for the specified principal (representing an entity such as an individual or a group). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeEntry](https://developer.android.com/reference/kotlin/java/security/acl/Acl#removeEntry(java.security.Principal,%20java.security.acl.AclEntry))`(`caller:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `entry:` ` [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!`)` Removes an ACL entry from this ACL. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setName](https://developer.android.com/reference/kotlin/java/security/acl/Acl#setName(java.security.Principal,%20kotlin.String))`(`caller:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of this ACL. |

| Inherited functions ||
|---|---|
| From class [Owner](https://developer.android.com/reference/kotlin/java/security/acl/Owner) |------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addOwner](https://developer.android.com/reference/kotlin/java/security/acl/Owner#addOwner(java.security.Principal,%20java.security.Principal))`(`caller:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `owner:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`)` <br /> Adds an owner. Only owners can modify ACL contents. The caller principal must be an owner of the ACL in order to invoke this method. That is, only an owner can add another owner. The initial owner is configured at ACL construction time. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deleteOwner](https://developer.android.com/reference/kotlin/java/security/acl/Owner#deleteOwner(java.security.Principal,%20java.security.Principal))`(`caller:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`, `owner:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`)` <br /> Deletes an owner. If this is the last owner in the ACL, an exception is raised. The caller principal must be an owner of the ACL in order to invoke this method. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOwner](https://developer.android.com/reference/kotlin/java/security/acl/Owner#isOwner(java.security.Principal))`(`owner:` ` [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!`)` <br /> Returns true if the given principal is an owner of the ACL. <br /> | ||

## Public methods

### addEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addEntry(
    caller: Principal!, 
    entry: AclEntry!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds an ACL entry to this ACL. An entry associates a principal (e.g., an individual or a group) with a set of permissions. Each principal can have at most one positive ACL entry (specifying permissions to be granted to the principal) and one negative ACL entry (specifying permissions to be denied). If there is already an ACL entry of the same type (negative or positive) already in the ACL, false is returned.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!:the principal invoking this method. It must be an owner of this ACL. |
| `entry` | [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!:the ACL entry to be added to this ACL. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true on success, false if an entry of the same type (positive or negative) for the same principal is already present in this ACL. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------|
| `java.security.acl.NotOwnerException` | if the caller principal is not an owner of this ACL. |

### checkPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkPermission(
    principal: Principal!, 
    permission: Permission!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether or not the specified principal has the specified permission. If it does, true is returned, otherwise false is returned. More specifically, this method checks whether the passed permission is a member of the allowed permission set of the specified principal. The allowed permission set is determined by the same algorithm as is used by the`getPermissions`method.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `principal` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!:the principal, assumed to be a valid authenticated Principal. |
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/acl/Permission)!:the permission to be checked for. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the principal has the specified permission, false otherwise. |

**See Also**

- [#getPermissions](https://developer.android.com/reference/kotlin/java/security/acl/Acl#getPermissions(java.security.Principal)) 

### entries

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun entries(): Enumeration<AclEntry!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration of the entries in this ACL. Each element in the enumeration is of type AclEntry.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)< [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!>! | an enumeration of the entries in this ACL. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the name of this ACL.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the name of this ACL. |

**See Also**

- [#setName](https://developer.android.com/reference/kotlin/java/security/acl/Acl#setName(java.security.Principal,%20kotlin.String)) 

### getPermissions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPermissions(user: Principal!): Enumeration<Permission!>!
```

**Deprecated:** *Deprecated in Java.*

Returns an enumeration for the set of allowed permissions for the specified principal (representing an entity such as an individual or a group). This set of allowed permissions is calculated as follows:

- If there is no entry in this Access Control List for the specified principal, an empty permission set is returned.
- Otherwise, the principal's group permission sets are determined. (A principal can belong to one or more groups, where a group is a group of principals, represented by the Group interface.) The group positive permission set is the union of all the positive permissions of each group that the principal belongs to. The group negative permission set is the union of all the negative permissions of each group that the principal belongs to. If there is a specific permission that occurs in both the positive permission set and the negative permission set, it is removed from both.The individual positive and negative permission sets are also determined. The positive permission set contains the permissions specified in the positive ACL entry (if any) for the principal. Similarly, the negative permission set contains the permissions specified in the negative ACL entry (if any) for the principal. The individual positive (or negative) permission set is considered to be null if there is not a positive (negative) ACL entry for the principal in this ACL.

 The set of permissions granted to the principal is then calculated using the simple rule that individual permissions always override the group permissions. That is, the principal's individual negative permission set (specific denial of permissions) overrides the group positive permission set, and the principal's individual positive permission set overrides the group negative permission set.

<br />

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `user` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!:the principal whose permission set is to be returned. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)< [Permission](https://developer.android.com/reference/kotlin/java/security/acl/Permission)!>! | the permission set specifying the permissions the principal is allowed. |

### removeEntry

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeEntry(
    caller: Principal!, 
    entry: AclEntry!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes an ACL entry from this ACL.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!:the principal invoking this method. It must be an owner of this ACL. |
| `entry` | [AclEntry](https://developer.android.com/reference/kotlin/java/security/acl/AclEntry)!:the ACL entry to be removed from this ACL. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true on success, false if the entry is not part of this ACL. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------|
| `java.security.acl.NotOwnerException` | if the caller principal is not an owner of this Acl. |

### setName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setName(
    caller: Principal!, 
    name: String!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the name of this ACL.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `caller` | [Principal](https://developer.android.com/reference/kotlin/java/security/Principal.html#)!:the principal invoking this method. It must be an owner of this ACL. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name to be given to this ACL. |

| Exceptions ||
|---------------------------------------|------------------------------------------------------|
| `java.security.acl.NotOwnerException` | if the caller principal is not an owner of this ACL. |

**See Also**

- [#getName](https://developer.android.com/reference/kotlin/java/security/acl/Acl#getName())
