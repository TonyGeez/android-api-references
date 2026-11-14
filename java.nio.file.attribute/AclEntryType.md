# AclEntryType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntryType

```
class AclEntryType
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.AclEntryType](AclEntryType.md)\> ||
| | ↳ | [java.nio.file.attribute.AclEntryType](AclEntryType.md) |

| Known Direct Subclasses [AclEntryType.ALARM](AclEntryType.md), [AclEntryType.ALLOW](AclEntryType.md), [AclEntryType.AUDIT](AclEntryType.md), [AclEntryType.DENY](AclEntryType.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------| | [AclEntryType.ALARM](AclEntryType.md) | Generate an alarm, in a system dependent way, the access specified in the permissions component of the ACL entry. | | [AclEntryType.ALLOW](AclEntryType.md) | Explicitly grants access to a file or directory. | | [AclEntryType.AUDIT](AclEntryType.md) | Log, in a system dependent way, the access specified in the permissions component of the ACL entry. | | [AclEntryType.DENY](AclEntryType.md) | Explicitly denies access to a file or directory. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A typesafe enumeration of the access control entry types.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ALARM](AclEntryType.md) Generate an alarm, in a system dependent way, the access specified in the permissions component of the ACL entry. |
| [ALLOW](AclEntryType.md) Explicitly grants access to a file or directory. |
| [AUDIT](AclEntryType.md) Log, in a system dependent way, the access specified in the permissions component of the ACL entry. |
| [DENY](AclEntryType.md) Explicitly denies access to a file or directory. |

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
