# LinkPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkPermission

```
class LinkPermission : BasicPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.security.Permission](../java.security/Permission.md) |||
| | ↳ | [java.security.BasicPermission](../java.security/BasicPermission.md) ||
| | | ↳ | [java.nio.file.LinkPermission](LinkPermission.md) |
| --- | --- | --- | --- |

The`Permission`class for link creation operations.

The following table provides a summary description of what the permission allows, and discusses the risks of granting code the permission.

| Permission Target Name | What the Permission Allows | Risks of Allowing this Permission |
| --- | --- | --- |
| hard | Ability to add an existing file to a directory. This is sometimes known as creating a link, or hard link. | Extreme care should be taken when granting this permission. It allows linking to any file or directory in the file system thus allowing the attacker access to all files. |
| symbolic | Ability to create symbolic links. | Extreme care should be taken when granting this permission. It allows linking to any file or directory in the file system thus allowing the attacker to access to all files. |
|------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkPermission](LinkPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`LinkPermission`with the specified name. |
| [LinkPermission](LinkPermission.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `actions:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`LinkPermission`with the specified name. |

| Inherited functions ||
|---|---|
| From class [Permission](../java.security/Permission.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkGuard](../java.security/Permission.md))`(`object:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](../java.security/Permission.md))`()` <br /> | | [PermissionCollection](../java.security/PermissionCollection.md)! | [newPermissionCollection](../java.security/Permission.md))`()` <br /> | ||
| From class [BasicPermission](../java.security/BasicPermission.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getActions](../java.security/BasicPermission.md))`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [implies](../java.security/BasicPermission.md))`(`p:` ` [Permission](../java.security/Permission.md)!`)` <br /> | ||

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
