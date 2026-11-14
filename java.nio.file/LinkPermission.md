# LinkPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkPermission

```
class LinkPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.security.Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |||
| | ↳ | [java.security.BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) ||
| | | ↳ | [java.nio.file.LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission#) |

The`Permission`class for link creation operations.

The following table provides a summary description of what the permission allows, and discusses the risks of granting code the permission.

| Permission Target Name | What the Permission Allows | Risks of Allowing this Permission |
| hard | Ability to add an existing file to a directory. This is sometimes known as creating a link, or hard link. | Extreme care should be taken when granting this permission. It allows linking to any file or directory in the file system thus allowing the attacker access to all files. |
| symbolic | Ability to create symbolic links. | Extreme care should be taken when granting this permission. It allows linking to any file or directory in the file system thus allowing the attacker to access to all files. |
|------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission#LinkPermission(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`LinkPermission`with the specified name. |
| [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission#LinkPermission(kotlin.String,%20kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`LinkPermission`with the specified name. |

| Inherited functions ||
|---|---|
| From class [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](https://developer.android.com/reference/kotlin/java/security/Permission.html#checkGuard(kotlin.Any))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](https://developer.android.com/reference/kotlin/java/security/Permission.html#getName())`()` <br /> | | [PermissionCollection](https://developer.android.com/reference/kotlin/java/security/PermissionCollection.html#)! | [newPermissionCollection](https://developer.android.com/reference/kotlin/java/security/Permission.html#newPermissionCollection())`()` <br /> | ||
| From class [BasicPermission](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#getActions())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](https://developer.android.com/reference/kotlin/java/security/BasicPermission.html#implies(java.security.Permission))`(`p:` ` [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)!`)` <br /> | ||

## Public constructors

### LinkPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkPermission(name: String!)
```

Constructs a`LinkPermission`with the specified name.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the permission. It must be "hard" or "symbolic". |

| Exceptions ||
|--------------------------------------|-----------------------------|
| `java.lang.IllegalArgumentException` | if name is empty or invalid |

### LinkPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkPermission(
    name: String!, 
    actions: String!)
```

Constructs a`LinkPermission`with the specified name.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the permission; must be "hard" or "symbolic". |
| `actions` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the actions for the permission; must be the empty string or`null` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if name is empty or invalid, or actions is a non-empty string |
