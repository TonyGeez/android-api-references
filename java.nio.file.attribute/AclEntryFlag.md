# AclEntryFlag

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntryFlag

```
class AclEntryFlag
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.AclEntryFlag](AclEntryFlag.md)\> ||
| | ↳ | [java.nio.file.attribute.AclEntryFlag](AclEntryFlag.md) |

| Known Direct Subclasses [AclEntryFlag.DIRECTORY_INHERIT](AclEntryFlag.md), [AclEntryFlag.FILE_INHERIT](AclEntryFlag.md), [AclEntryFlag.INHERIT_ONLY](AclEntryFlag.md), [AclEntryFlag.NO_PROPAGATE_INHERIT](AclEntryFlag.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AclEntryFlag.DIRECTORY_INHERIT](AclEntryFlag.md) | Can be placed on a directory and indicates that the ACL entry should be added to each new directory created. | | [AclEntryFlag.FILE_INHERIT](AclEntryFlag.md) | Can be placed on a directory and indicates that the ACL entry should be added to each new non-directory file created. | | [AclEntryFlag.INHERIT_ONLY](AclEntryFlag.md) | Can be placed on a directory but does not apply to the directory, only to newly created files/directories as specified by the [FILE_INHERIT](AclEntryFlag.md) and [DIRECTORY_INHERIT](AclEntryFlag.md) flags. | | [AclEntryFlag.NO_PROPAGATE_INHERIT](AclEntryFlag.md) | Can be placed on a directory to indicate that the ACL entry should not be placed on the newly created directory which is inheritable by subdirectories of the created directory. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the flags for used by the flags component of an ACL [entry](AclEntry.md).

In this release, this class does not define flags related to [java.nio.file.attribute.AclEntryType#AUDIT](AclEntryType.md) and [AclEntryType.ALARM](AclEntryType.md) entry types.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DIRECTORY_INHERIT](AclEntryFlag.md) Can be placed on a directory and indicates that the ACL entry should be added to each new directory created. |
| [FILE_INHERIT](AclEntryFlag.md) Can be placed on a directory and indicates that the ACL entry should be added to each new non-directory file created. |
| [INHERIT_ONLY](AclEntryFlag.md) Can be placed on a directory but does not apply to the directory, only to newly created files/directories as specified by the [FILE_INHERIT](AclEntryFlag.md) and [DIRECTORY_INHERIT](AclEntryFlag.md) flags. |
| [NO_PROPAGATE_INHERIT](AclEntryFlag.md) Can be placed on a directory to indicate that the ACL entry should not be placed on the newly created directory which is inheritable by subdirectories of the created directory. |

## Enum values

### DIRECTORY_INHERIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DIRECTORY_INHERIT : AclEntryFlag
```

Can be placed on a directory and indicates that the ACL entry should be added to each new directory created. 

### FILE_INHERIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FILE_INHERIT : AclEntryFlag
```

Can be placed on a directory and indicates that the ACL entry should be added to each new non-directory file created. 

### INHERIT_ONLY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INHERIT_ONLY : AclEntryFlag
```

Can be placed on a directory but does not apply to the directory, only to newly created files/directories as specified by the [FILE_INHERIT](AclEntryFlag.md) and [DIRECTORY_INHERIT](AclEntryFlag.md) flags. 

### NO_PROPAGATE_INHERIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NO_PROPAGATE_INHERIT : AclEntryFlag
```

Can be placed on a directory to indicate that the ACL entry should not be placed on the newly created directory which is inheritable by subdirectories of the created directory.
