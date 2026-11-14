# AclEntryPermission

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AclEntryPermission

```
class AclEntryPermission
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.attribute.AclEntryPermission](AclEntryPermission.md)\> ||
| | ↳ | [java.nio.file.attribute.AclEntryPermission](AclEntryPermission.md) |

| Known Direct Subclasses [AclEntryPermission.APPEND_DATA](AclEntryPermission.md), [AclEntryPermission.DELETE](AclEntryPermission.md), [AclEntryPermission.DELETE_CHILD](AclEntryPermission.md), [AclEntryPermission.EXECUTE](AclEntryPermission.md), [AclEntryPermission.READ_ACL](AclEntryPermission.md), [AclEntryPermission.READ_ATTRIBUTES](AclEntryPermission.md), [AclEntryPermission.READ_DATA](AclEntryPermission.md), [AclEntryPermission.READ_NAMED_ATTRS](AclEntryPermission.md), [AclEntryPermission.SYNCHRONIZE](AclEntryPermission.md), [AclEntryPermission.WRITE_ACL](AclEntryPermission.md), [AclEntryPermission.WRITE_ATTRIBUTES](AclEntryPermission.md), [AclEntryPermission.WRITE_DATA](AclEntryPermission.md), and 2 others. |----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [AclEntryPermission.APPEND_DATA](AclEntryPermission.md) | Permission to append data to a file. | | [AclEntryPermission.DELETE](AclEntryPermission.md) | Permission to delete the file. | | [AclEntryPermission.DELETE_CHILD](AclEntryPermission.md) | Permission to delete a file or directory within a directory. | | [AclEntryPermission.EXECUTE](AclEntryPermission.md) | Permission to execute a file. | | [AclEntryPermission.READ_ACL](AclEntryPermission.md) | Permission to read the ACL attribute. | | [AclEntryPermission.READ_ATTRIBUTES](AclEntryPermission.md) | The ability to read (non-acl) file attributes. | | [AclEntryPermission.READ_DATA](AclEntryPermission.md) | Permission to read the data of the file. | | [AclEntryPermission.READ_NAMED_ATTRS](AclEntryPermission.md) | Permission to read the named attributes of a file. | | [AclEntryPermission.SYNCHRONIZE](AclEntryPermission.md) | Permission to access file locally at the server with synchronous reads and writes. | | [AclEntryPermission.WRITE_ACL](AclEntryPermission.md) | Permission to write the ACL attribute. | | [AclEntryPermission.WRITE_ATTRIBUTES](AclEntryPermission.md) | The ability to write (non-acl) file attributes. | | [AclEntryPermission.WRITE_DATA](AclEntryPermission.md) | Permission to modify the file's data. | | [AclEntryPermission.WRITE_NAMED_ATTRS](AclEntryPermission.md) | Permission to write the named attributes of a file. | | [AclEntryPermission.WRITE_OWNER](AclEntryPermission.md) | Permission to change the owner. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the permissions for use with the permissions component of an ACL [entry](AclEntry.md).

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [APPEND_DATA](AclEntryPermission.md) Permission to append data to a file. |
| [DELETE](AclEntryPermission.md) Permission to delete the file. |
| [DELETE_CHILD](AclEntryPermission.md) Permission to delete a file or directory within a directory. |
| [EXECUTE](AclEntryPermission.md) Permission to execute a file. |
| [READ_ACL](AclEntryPermission.md) Permission to read the ACL attribute. |
| [READ_ATTRIBUTES](AclEntryPermission.md) The ability to read (non-acl) file attributes. |
| [READ_DATA](AclEntryPermission.md) Permission to read the data of the file. |
| [READ_NAMED_ATTRS](AclEntryPermission.md) Permission to read the named attributes of a file. |
| [SYNCHRONIZE](AclEntryPermission.md) Permission to access file locally at the server with synchronous reads and writes. |
| [WRITE_ACL](AclEntryPermission.md) Permission to write the ACL attribute. |
| [WRITE_ATTRIBUTES](AclEntryPermission.md) The ability to write (non-acl) file attributes. |
| [WRITE_DATA](AclEntryPermission.md) Permission to modify the file's data. |
| [WRITE_NAMED_ATTRS](AclEntryPermission.md) Permission to write the named attributes of a file. |
| [WRITE_OWNER](AclEntryPermission.md) Permission to change the owner. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AclEntryPermission](AclEntryPermission.md)! | [ADD_FILE](AclEntryPermission.md) Permission to add a new file to a directory (equal to [WRITE_DATA](AclEntryPermission.md)) |
| static [AclEntryPermission](AclEntryPermission.md)! | [ADD_SUBDIRECTORY](AclEntryPermission.md) Permission to create a subdirectory to a directory (equal to [APPEND_DATA](AclEntryPermission.md)) |
| static [AclEntryPermission](AclEntryPermission.md)! | [LIST_DIRECTORY](AclEntryPermission.md) Permission to list the entries of a directory (equal to [READ_DATA](AclEntryPermission.md)) |
| --- | --- |

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

Permission to add a new file to a directory (equal to [WRITE_DATA](AclEntryPermission.md)) 

### ADD_SUBDIRECTORY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ADD_SUBDIRECTORY: AclEntryPermission!
```

Permission to create a subdirectory to a directory (equal to [APPEND_DATA](AclEntryPermission.md)) 

### LIST_DIRECTORY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LIST_DIRECTORY: AclEntryPermission!
```

Permission to list the entries of a directory (equal to [READ_DATA](AclEntryPermission.md))
