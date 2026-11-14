# PosixFilePermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFilePermission

```
class PosixFilePermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#)\> ||
| | ↳ | [java.nio.file.attribute.PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#) |

| Known Direct Subclasses [PosixFilePermission.GROUP_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_EXECUTE), [PosixFilePermission.GROUP_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_READ), [PosixFilePermission.GROUP_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_WRITE), [PosixFilePermission.OTHERS_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_EXECUTE), [PosixFilePermission.OTHERS_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_READ), [PosixFilePermission.OTHERS_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_WRITE), [PosixFilePermission.OWNER_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_EXECUTE), [PosixFilePermission.OWNER_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_READ), [PosixFilePermission.OWNER_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_WRITE) |------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------| | [PosixFilePermission.GROUP_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_EXECUTE) | Execute/search permission, group. | | [PosixFilePermission.GROUP_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_READ) | Read permission, group. | | [PosixFilePermission.GROUP_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_WRITE) | Write permission, group. | | [PosixFilePermission.OTHERS_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_EXECUTE) | Execute/search permission, others. | | [PosixFilePermission.OTHERS_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_READ) | Read permission, others. | | [PosixFilePermission.OTHERS_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_WRITE) | Write permission, others. | | [PosixFilePermission.OWNER_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_EXECUTE) | Execute/search permission, owner. | | [PosixFilePermission.OWNER_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_READ) | Read permission, owner. | | [PosixFilePermission.OWNER_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_WRITE) | Write permission, owner. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the bits for use with the [permissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#permissions())attribute.

The [PosixFilePermissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions) class defines methods for manipulating set of permissions.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GROUP_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_EXECUTE) Execute/search permission, group. |
| [GROUP_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_READ) Read permission, group. |
| [GROUP_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:GROUP_WRITE) Write permission, group. |
| [OTHERS_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_EXECUTE) Execute/search permission, others. |
| [OTHERS_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_READ) Read permission, others. |
| [OTHERS_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OTHERS_WRITE) Write permission, others. |
| [OWNER_EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_EXECUTE) Execute/search permission, owner. |
| [OWNER_READ](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_READ) Read permission, owner. |
| [OWNER_WRITE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission#ENUM_VALUE:OWNER_WRITE) Write permission, owner. |

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
