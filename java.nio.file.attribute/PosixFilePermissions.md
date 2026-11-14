# PosixFilePermissions

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PosixFilePermissions

```
class PosixFilePermissions
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.attribute.PosixFilePermissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#) |

This class consists exclusively of static methods that operate on sets of [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission) objects.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute)\< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!\>!\>! | [asFileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#asFileAttribute(kotlin.collections.MutableSet))`(`perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!>!`)` Creates a [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute), encapsulating a copy of the given file permissions, suitable for passing to the [createFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createFile(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))or [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))methods. |
| static [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!\>! | [fromString](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#fromString(kotlin.String))`(`perms:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the set of permissions corresponding to a given`String`representation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#toString(kotlin.collections.MutableSet))`(`perms:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!>!`)` Returns the`String`representation of a set of permissions. |
| --- | --- |

## Public methods

### asFileAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun asFileAttribute(perms: MutableSet<PosixFilePermission!>!): FileAttribute<MutableSet<PosixFilePermission!>!>!
```

Creates a [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute), encapsulating a copy of the given file permissions, suitable for passing to the [createFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createFile(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))or [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))methods.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!\>!:the set of permissions |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute)< [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!>!>! | an attribute encapsulating the given file permissions with [name](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute#name())`"posix:permissions"` |

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
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!>! | the resulting set of permissions |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the string cannot be converted to a set of permissions |

**See Also**

- [#toString(Set)](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#toString(kotlin.collections.MutableSet)) 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun toString(perms: MutableSet<PosixFilePermission!>!): String!
```

Returns the`String`representation of a set of permissions. It is guaranteed that the returned`String`can be parsed by the [fromString](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions#fromString(kotlin.String))method.

If the set contains`null`or elements that are not of type`PosixFilePermission`then these elements are ignored.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `perms` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission)!\>!:the set of permissions |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string representation of the permission set |
