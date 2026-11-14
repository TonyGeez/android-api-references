Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PermissionCollection

```
abstract class PermissionCollection : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.security.PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection#) |

| Known Direct Subclasses [Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions) |---|---| | [Permissions](https://developer.android.com/reference/kotlin/java/security/Permissions) | Android doesn't support `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#`. | |

Android doesn't support `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#`. Do not use this class.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#PermissionCollection()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#add(java.security.Permission)(permission: https://developer.android.com/reference/kotlin/java/security/Permission!)` Adds a permission object to the current collection of permission objects. |
| abstract [Enumeration](https://developer.android.com/reference/kotlin/java/util/Enumeration.html#)\< [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!\>! | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#elements()()` Returns an enumeration of all the Permission objects in the collection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#implies(java.security.Permission)(permission: https://developer.android.com/reference/kotlin/java/security/Permission!)` Checks to see if the specified permission is implied by the collection of Permission objects held in this PermissionCollection. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#isReadOnly()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/security/PermissionCollection#setReadOnly()()` <br /> |

## Public constructors

### PermissionCollection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
PermissionCollection()
```

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(permission: Permission!): Unit
```

Adds a permission object to the current collection of permission objects.

| Parameters ||
|---|---|
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!: the Permission object to add. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | - if this PermissionCollection object is a homogeneous collection and the permission is not of the correct type. |
| `java.lang.SecurityException` | - if this PermissionCollection object has been marked readonly |

### elements

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun elements(): Enumeration<Permission!>!
```

Returns an enumeration of all the Permission objects in the collection.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Enumeration.html#<https://developer.android.com/reference/kotlin/java/security/Permission!>!` | an enumeration of all the Permissions. |

### implies

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun implies(permission: Permission!): Boolean
```

Checks to see if the specified permission is implied by the collection of Permission objects held in this PermissionCollection.

| Parameters ||
|---|---|
| `permission` | [Permission](https://developer.android.com/reference/kotlin/java/security/Permission)!: the Permission object to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if "permission" is implied by the permissions in the collection, false if not. |

### isReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isReadOnly(): Boolean
```

### setReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReadOnly(): Unit
```
