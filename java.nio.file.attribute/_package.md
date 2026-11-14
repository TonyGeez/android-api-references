# java.nio.file.attribute

# java.nio.file.attribute

## Interfaces

| [AclFileAttributeView](../java/nio/file/attribute/AclFileAttributeView.md) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. |
| --- | --- |
| [AttributeView](../java/nio/file/attribute/AttributeView.md) | An object that provides a read-only or updatable*view*of non-opaque values associated with an object in a filesystem. |
| [BasicFileAttributes](../java/nio/file/attribute/BasicFileAttributes.md) | Basic attributes associated with a file in a file system. |
| [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. |
| --- | --- |
| [DosFileAttributes](../java/nio/file/attribute/DosFileAttributes.md) | File attributes associated with a file in a file system that supports legacy "DOS" attributes. |
| [DosFileAttributeView](../java/nio/file/attribute/DosFileAttributeView.md) | A file attribute view that provides a view of the legacy "DOS" file attributes. |
| [FileAttribute](../java/nio/file/attribute/FileAttribute.md) | An object that encapsulates the value of a file attribute that can be set atomically when creating a new file or directory by invoking the [createFile](../java/nio/file/Files.md))or [createDirectory](../java/nio/file/Files.md))methods. |
| --- | --- |
| [FileAttributeView](../java/nio/file/attribute/FileAttributeView.md) | An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. |
| [FileOwnerAttributeView](../java/nio/file/attribute/FileOwnerAttributeView.md) | A file attribute view that supports reading or updating the owner of a file. |
| [FileStoreAttributeView](../java/nio/file/attribute/FileStoreAttributeView.md) | An attribute view that is a read-only or updatable view of the attributes of a [java.nio.file.FileStore](../java/nio/file/FileStore.md). |
| --- | --- |
| [GroupPrincipal](../java/nio/file/attribute/GroupPrincipal.md) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. |
| [PosixFileAttributes](../java/nio/file/attribute/PosixFileAttributes.md) | File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| [PosixFileAttributeView](../java/nio/file/attribute/PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| --- | --- |
| [UserDefinedFileAttributeView](../java/nio/file/attribute/UserDefinedFileAttributeView.md) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. |
| [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) | A`Principal`representing an identity used to determine access rights to objects in a file system. |

## Classes

| [AclEntry](../java/nio/file/attribute/AclEntry.md) | An entry in an access control list (ACL). |
| --- | --- |
| [FileTime](../java/nio/file/attribute/FileTime.md) | Represents the value of a file's time stamp attribute. |
| [PosixFilePermissions](../java/nio/file/attribute/PosixFilePermissions.md) | This class consists exclusively of static methods that operate on sets of [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md) objects. |
| [UserPrincipalLookupService](../java/nio/file/attribute/UserPrincipalLookupService.md) | An object to lookup user and group principals by name. |
| --- | --- |

## Exceptions

| [UserPrincipalNotFoundException](../java/nio/file/attribute/UserPrincipalNotFoundException.md) | Checked exception thrown when a lookup of [UserPrincipal](../java/nio/file/attribute/UserPrincipal.md) fails because the principal does not exist. |
| --- | --- |

## Enums

| [AclEntryFlag](../java/nio/file/attribute/AclEntryFlag.md) | Defines the flags for used by the flags component of an ACL [entry](../java/nio/file/attribute/AclEntry.md). |
| --- | --- |
| [AclEntryPermission](../java/nio/file/attribute/AclEntryPermission.md) | Defines the permissions for use with the permissions component of an ACL [entry](../java/nio/file/attribute/AclEntry.md). |
| [AclEntryType](../java/nio/file/attribute/AclEntryType.md) | A typesafe enumeration of the access control entry types. |
| [PosixFilePermission](../java/nio/file/attribute/PosixFilePermission.md) | Defines the bits for use with the [permissions](../java/nio/file/attribute/PosixFileAttributes.md))attribute. |
| --- | --- |
