# AclEntryPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntryPermission

```
class AclEntryPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)\> ||
| | ↳ | [java.nio.file.attribute.AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#) |

| Known Direct Subclasses [AclEntryPermission.APPEND_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:APPEND_DATA), [AclEntryPermission.DELETE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE), [AclEntryPermission.DELETE_CHILD](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE_CHILD), [AclEntryPermission.EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:EXECUTE), [AclEntryPermission.READ_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ACL), [AclEntryPermission.READ_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ATTRIBUTES), [AclEntryPermission.READ_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_DATA), [AclEntryPermission.READ_NAMED_ATTRS](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_NAMED_ATTRS), [AclEntryPermission.SYNCHRONIZE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:SYNCHRONIZE), [AclEntryPermission.WRITE_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ACL), [AclEntryPermission.WRITE_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ATTRIBUTES), [AclEntryPermission.WRITE_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_DATA), and 2 others. |----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [AclEntryPermission.APPEND_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:APPEND_DATA) | Permission to append data to a file. | | [AclEntryPermission.DELETE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE) | Permission to delete the file. | | [AclEntryPermission.DELETE_CHILD](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE_CHILD) | Permission to delete a file or directory within a directory. | | [AclEntryPermission.EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:EXECUTE) | Permission to execute a file. | | [AclEntryPermission.READ_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ACL) | Permission to read the ACL attribute. | | [AclEntryPermission.READ_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ATTRIBUTES) | The ability to read (non-acl) file attributes. | | [AclEntryPermission.READ_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_DATA) | Permission to read the data of the file. | | [AclEntryPermission.READ_NAMED_ATTRS](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_NAMED_ATTRS) | Permission to read the named attributes of a file. | | [AclEntryPermission.SYNCHRONIZE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:SYNCHRONIZE) | Permission to access file locally at the server with synchronous reads and writes. | | [AclEntryPermission.WRITE_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ACL) | Permission to write the ACL attribute. | | [AclEntryPermission.WRITE_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ATTRIBUTES) | The ability to write (non-acl) file attributes. | | [AclEntryPermission.WRITE_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_DATA) | Permission to modify the file's data. | | [AclEntryPermission.WRITE_NAMED_ATTRS](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_NAMED_ATTRS) | Permission to write the named attributes of a file. | | [AclEntryPermission.WRITE_OWNER](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_OWNER) | Permission to change the owner. | |

Defines the permissions for use with the permissions component of an ACL [entry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry).

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [APPEND_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:APPEND_DATA) Permission to append data to a file. |
| [DELETE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE) Permission to delete the file. |
| [DELETE_CHILD](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:DELETE_CHILD) Permission to delete a file or directory within a directory. |
| [EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:EXECUTE) Permission to execute a file. |
| [READ_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ACL) Permission to read the ACL attribute. |
| [READ_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_ATTRIBUTES) The ability to read (non-acl) file attributes. |
| [READ_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_DATA) Permission to read the data of the file. |
| [READ_NAMED_ATTRS](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:READ_NAMED_ATTRS) Permission to read the named attributes of a file. |
| [SYNCHRONIZE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:SYNCHRONIZE) Permission to access file locally at the server with synchronous reads and writes. |
| [WRITE_ACL](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ACL) Permission to write the ACL attribute. |
| [WRITE_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_ATTRIBUTES) The ability to write (non-acl) file attributes. |
| [WRITE_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_DATA) Permission to modify the file's data. |
| [WRITE_NAMED_ATTRS](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_NAMED_ATTRS) Permission to write the named attributes of a file. |
| [WRITE_OWNER](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ENUM_VALUE:WRITE_OWNER) Permission to change the owner. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)! | [ADD_FILE](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ADD_FILE:java.nio.file.attribute.AclEntryPermission) Permission to add a new file to a directory (equal to [WRITE_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)) |
| static [AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)! | [ADD_SUBDIRECTORY](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#ADD_SUBDIRECTORY:java.nio.file.attribute.AclEntryPermission) Permission to create a subdirectory to a directory (equal to [APPEND_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)) |
| static [AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)! | [LIST_DIRECTORY](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#LIST_DIRECTORY:java.nio.file.attribute.AclEntryPermission) Permission to list the entries of a directory (equal to [READ_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)) |

## Enum values

### APPEND_DATA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val APPEND_DATA : AclEntryPermission
```

Permission to append data to a file. 

### DELETE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DELETE : AclEntryPermission
```

Permission to delete the file. 

### DELETE_CHILD

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DELETE_CHILD : AclEntryPermission
```

Permission to delete a file or directory within a directory. 

### EXECUTE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val EXECUTE : AclEntryPermission
```

Permission to execute a file. 

### READ_ACL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val READ_ACL : AclEntryPermission
```

Permission to read the ACL attribute. 

### READ_ATTRIBUTES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val READ_ATTRIBUTES : AclEntryPermission
```

The ability to read (non-acl) file attributes. 

### READ_DATA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val READ_DATA : AclEntryPermission
```

Permission to read the data of the file. 

### READ_NAMED_ATTRS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val READ_NAMED_ATTRS : AclEntryPermission
```

Permission to read the named attributes of a file.

[RFC 3530: Network File System (NFS) version 4 Protocol](http://www.ietf.org/rfc/rfc3530.txt) defines*named attributes*as opaque files associated with a file in the file system. 

### SYNCHRONIZE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SYNCHRONIZE : AclEntryPermission
```

Permission to access file locally at the server with synchronous reads and writes. 

### WRITE_ACL

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE_ACL : AclEntryPermission
```

Permission to write the ACL attribute. 

### WRITE_ATTRIBUTES

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE_ATTRIBUTES : AclEntryPermission
```

The ability to write (non-acl) file attributes. 

### WRITE_DATA

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE_DATA : AclEntryPermission
```

Permission to modify the file's data. 

### WRITE_NAMED_ATTRS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE_NAMED_ATTRS : AclEntryPermission
```

Permission to write the named attributes of a file.

[RFC 3530: Network File System (NFS) version 4 Protocol](http://www.ietf.org/rfc/rfc3530.txt) defines*named attributes*as opaque files associated with a file in the file system. 

### WRITE_OWNER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE_OWNER : AclEntryPermission
```

Permission to change the owner.

## Properties

### ADD_FILE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADD_FILE: AclEntryPermission!
```

Permission to add a new file to a directory (equal to [WRITE_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)) 

### ADD_SUBDIRECTORY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADD_SUBDIRECTORY: AclEntryPermission!
```

Permission to create a subdirectory to a directory (equal to [APPEND_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#)) 

### LIST_DIRECTORY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIST_DIRECTORY: AclEntryPermission!
```

Permission to list the entries of a directory (equal to [READ_DATA](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission#))
