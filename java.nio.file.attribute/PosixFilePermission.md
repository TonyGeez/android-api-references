# PosixFilePermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFilePermission

```
class PosixFilePermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.PosixFilePermission](PosixFilePermission.md)\> ||
| | ↳ | [java.nio.file.attribute.PosixFilePermission](PosixFilePermission.md) |

| Known Direct Subclasses [PosixFilePermission.GROUP_EXECUTE](PosixFilePermission.md), [PosixFilePermission.GROUP_READ](PosixFilePermission.md), [PosixFilePermission.GROUP_WRITE](PosixFilePermission.md), [PosixFilePermission.OTHERS_EXECUTE](PosixFilePermission.md), [PosixFilePermission.OTHERS_READ](PosixFilePermission.md), [PosixFilePermission.OTHERS_WRITE](PosixFilePermission.md), [PosixFilePermission.OWNER_EXECUTE](PosixFilePermission.md), [PosixFilePermission.OWNER_READ](PosixFilePermission.md), [PosixFilePermission.OWNER_WRITE](PosixFilePermission.md) |------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------| | [PosixFilePermission.GROUP_EXECUTE](PosixFilePermission.md) | Execute/search permission, group. | | [PosixFilePermission.GROUP_READ](PosixFilePermission.md) | Read permission, group. | | [PosixFilePermission.GROUP_WRITE](PosixFilePermission.md) | Write permission, group. | | [PosixFilePermission.OTHERS_EXECUTE](PosixFilePermission.md) | Execute/search permission, others. | | [PosixFilePermission.OTHERS_READ](PosixFilePermission.md) | Read permission, others. | | [PosixFilePermission.OTHERS_WRITE](PosixFilePermission.md) | Write permission, others. | | [PosixFilePermission.OWNER_EXECUTE](PosixFilePermission.md) | Execute/search permission, owner. | | [PosixFilePermission.OWNER_READ](PosixFilePermission.md) | Read permission, owner. | | [PosixFilePermission.OWNER_WRITE](PosixFilePermission.md) | Write permission, owner. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the bits for use with the [permissions](PosixFileAttributes.md))attribute.

The [PosixFilePermissions](PosixFilePermissions.md) class defines methods for manipulating set of permissions.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GROUP_EXECUTE](PosixFilePermission.md) Execute/search permission, group. |
| [GROUP_READ](PosixFilePermission.md) Read permission, group. |
| [GROUP_WRITE](PosixFilePermission.md) Write permission, group. |
| [OTHERS_EXECUTE](PosixFilePermission.md) Execute/search permission, others. |
| [OTHERS_READ](PosixFilePermission.md) Read permission, others. |
| [OTHERS_WRITE](PosixFilePermission.md) Write permission, others. |
| [OWNER_EXECUTE](PosixFilePermission.md) Execute/search permission, owner. |
| [OWNER_READ](PosixFilePermission.md) Read permission, owner. |
| [OWNER_WRITE](PosixFilePermission.md) Write permission, owner. |

## Enum values

### GROUP_EXECUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val GROUP_EXECUTE : PosixFilePermission
```

Execute/search permission, group. 

### GROUP_READ

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val GROUP_READ : PosixFilePermission
```

Read permission, group. 

### GROUP_WRITE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val GROUP_WRITE : PosixFilePermission
```

Write permission, group. 

### OTHERS_EXECUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OTHERS_EXECUTE : PosixFilePermission
```

Execute/search permission, others. 

### OTHERS_READ

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OTHERS_READ : PosixFilePermission
```

Read permission, others. 

### OTHERS_WRITE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OTHERS_WRITE : PosixFilePermission
```

Write permission, others. 

### OWNER_EXECUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OWNER_EXECUTE : PosixFilePermission
```

Execute/search permission, owner. 

### OWNER_READ

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OWNER_READ : PosixFilePermission
```

Read permission, owner. 

### OWNER_WRITE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val OWNER_WRITE : PosixFilePermission
```

Write permission, owner.
