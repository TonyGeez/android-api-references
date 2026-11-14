# AclEntryType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntryType

```
class AclEntryType
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.AclEntryType](../java/nio/file/attribute/AclEntryType.md)\> ||
| | ↳ | [java.nio.file.attribute.AclEntryType](../java/nio/file/attribute/AclEntryType.md) |

| Known Direct Subclasses [AclEntryType.ALARM](../java/nio/file/attribute/AclEntryType.md), [AclEntryType.ALLOW](../java/nio/file/attribute/AclEntryType.md), [AclEntryType.AUDIT](../java/nio/file/attribute/AclEntryType.md), [AclEntryType.DENY](../java/nio/file/attribute/AclEntryType.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [AclEntryType.ALARM](../java/nio/file/attribute/AclEntryType.md) | Generate an alarm, in a system dependent way, the access specified in the permissions component of the ACL entry. | | [AclEntryType.ALLOW](../java/nio/file/attribute/AclEntryType.md) | Explicitly grants access to a file or directory. | | [AclEntryType.AUDIT](../java/nio/file/attribute/AclEntryType.md) | Log, in a system dependent way, the access specified in the permissions component of the ACL entry. | | [AclEntryType.DENY](../java/nio/file/attribute/AclEntryType.md) | Explicitly denies access to a file or directory. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A typesafe enumeration of the access control entry types.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ALARM](../java/nio/file/attribute/AclEntryType.md) Generate an alarm, in a system dependent way, the access specified in the permissions component of the ACL entry. |
| [ALLOW](../java/nio/file/attribute/AclEntryType.md) Explicitly grants access to a file or directory. |
| [AUDIT](../java/nio/file/attribute/AclEntryType.md) Log, in a system dependent way, the access specified in the permissions component of the ACL entry. |
| [DENY](../java/nio/file/attribute/AclEntryType.md) Explicitly denies access to a file or directory. |

## Enum values

### ALARM

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ALARM : AclEntryType
```

Generate an alarm, in a system dependent way, the access specified in the permissions component of the ACL entry. 

### ALLOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ALLOW : AclEntryType
```

Explicitly grants access to a file or directory. 

### AUDIT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AUDIT : AclEntryType
```

Log, in a system dependent way, the access specified in the permissions component of the ACL entry. 

### DENY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DENY : AclEntryType
```

Explicitly denies access to a file or directory.
