# java.nio.file.attribute

# java.nio.file.attribute

## Interfaces

| [AclFileAttributeView](AclFileAttributeView.md) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. |
| --- | --- |
| [AttributeView](AttributeView.md) | An object that provides a read-only or updatable*view*of non-opaque values associated with an object in a filesystem. |
| [BasicFileAttributes](BasicFileAttributes.md) | Basic attributes associated with a file in a file system. |
| [BasicFileAttributeView](BasicFileAttributeView.md) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. |
| --- | --- |
| [DosFileAttributes](DosFileAttributes.md) | File attributes associated with a file in a file system that supports legacy "DOS" attributes. |
| [DosFileAttributeView](DosFileAttributeView.md) | A file attribute view that provides a view of the legacy "DOS" file attributes. |
| [FileAttribute](FileAttribute.md) | An object that encapsulates the value of a file attribute that can be set atomically when creating a new file or directory by invoking the [createFile](../java.nio.file/Files.md))or [createDirectory](../java.nio.file/Files.md))methods. |
| --- | --- |
| [FileAttributeView](FileAttributeView.md) | An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. |
| [FileOwnerAttributeView](FileOwnerAttributeView.md) | A file attribute view that supports reading or updating the owner of a file. |
| [FileStoreAttributeView](FileStoreAttributeView.md) | An attribute view that is a read-only or updatable view of the attributes of a [java.nio.file.FileStore](../java.nio.file/FileStore.md). |
| --- | --- |
| [GroupPrincipal](GroupPrincipal.md) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. |
| [PosixFileAttributes](PosixFileAttributes.md) | File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| [PosixFileAttributeView](PosixFileAttributeView.md) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| --- | --- |
| [UserDefinedFileAttributeView](UserDefinedFileAttributeView.md) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. |
| [UserPrincipal](UserPrincipal.md) | A`Principal`representing an identity used to determine access rights to objects in a file system. |

## Classes

| [AclEntry](AclEntry.md) | An entry in an access control list (ACL). |
| --- | --- |
| [FileTime](FileTime.md) | Represents the value of a file's time stamp attribute. |
| [PosixFilePermissions](PosixFilePermissions.md) | This class consists exclusively of static methods that operate on sets of [PosixFilePermission](PosixFilePermission.md) objects. |
| [UserPrincipalLookupService](UserPrincipalLookupService.md) | An object to lookup user and group principals by name. |
| --- | --- |

## Exceptions

| [UserPrincipalNotFoundException](UserPrincipalNotFoundException.md) | Checked exception thrown when a lookup of [UserPrincipal](UserPrincipal.md) fails because the principal does not exist. |
| --- | --- |

## Enums

| [AclEntryFlag](AclEntryFlag.md) | Defines the flags for used by the flags component of an ACL [entry](AclEntry.md). |
| --- | --- |
| [AclEntryPermission](AclEntryPermission.md) | Defines the permissions for use with the permissions component of an ACL [entry](AclEntry.md). |
| [AclEntryType](AclEntryType.md) | A typesafe enumeration of the access control entry types. |
| [PosixFilePermission](PosixFilePermission.md) | Defines the bits for use with the [permissions](PosixFileAttributes.md))attribute. |
| --- | --- |
