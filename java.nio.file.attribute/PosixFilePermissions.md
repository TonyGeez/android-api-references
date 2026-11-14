# PosixFilePermissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFilePermissions

```
class PosixFilePermissions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.PosixFilePermissions](../java/nio/file/attribute/PosixFilePermissions.md) |

This class consists exclusively of static methods that operate on sets of [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md) objects.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>!\>! | [asFileAttribute](../java/nio/file/attribute/PosixFilePermissions.md))`(`perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>!`)` Creates a [FileAttribute](../java/nio/file/attribute/FileAttribute.md), encapsulating a copy of the given file permissions, suitable for passing to the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>! | [fromString](../java/nio/file/attribute/PosixFilePermissions.md))`(`perms:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the set of permissions corresponding to a given`String`representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](../java/nio/file/attribute/PosixFilePermissions.md))`(`perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>!`)` Returns the`String`representation of a set of permissions. |
| --- | --- |

## Public methods

### asFileAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun asFileAttribute(perms: MutableSet<PosixFilePermission!>!): FileAttribute<MutableSet<PosixFilePermission!>!>!
```

Creates a [FileAttribute](../java/nio/file/attribute/FileAttribute.md), encapsulating a copy of the given file permissions, suitable for passing to the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>!:the set of permissions |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileAttribute](../java/nio/file/attribute/FileAttribute.md)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>!>! | an attribute encapsulating the given file permissions with [name](../java/nio/file/attribute/FileAttribute.md))`"posix:permissions"` |

| Exceptions ||
|--------------------------------|------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the set contains elements that are not of type`PosixFilePermission` |

### fromString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromString(perms: String!): MutableSet<PosixFilePermission!>!
```

Returns the set of permissions corresponding to a given`String`representation.

The`perms`parameter is a`String`representing the permissions. It has 9 characters that are interpreted as three sets of three. The first set refers to the owner's permissions; the next to the group permissions and the last to others. Within each set, the first character is`'r'`to indicate permission to read, the second character is`'w'`to indicate permission to write, and the third character is`'x'`for execute permission. Where a permission is not set then the corresponding character is set to`'-'`.

**Usage Example:**Suppose we require the set of permissions that indicate the owner has read, write, and execute permissions, the group has read and execute permissions and others have none. 

```kotlin
Set<PosixFilePermission> perms = PosixFilePermissions.fromString("rwxr-x---");
  
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `perms` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:string representing a set of permissions |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!>! | the resulting set of permissions |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the string cannot be converted to a set of permissions |

**See Also**

- [#toString(Set)](../java/nio/file/attribute/PosixFilePermissions.md)) 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(perms: MutableSet<PosixFilePermission!>!): String!
```

Returns the`String`representation of a set of permissions. It is guaranteed that the returned`String`can be parsed by the [fromString](../java/nio/file/attribute/PosixFilePermissions.md))method.

If the set contains`null`or elements that are not of type`PosixFilePermission`then these elements are ignored.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md)!\>!:the set of permissions |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string representation of the permission set |
