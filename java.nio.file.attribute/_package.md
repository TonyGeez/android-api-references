# java.nio.file.attribute

# java.nio.file.attribute

## Interfaces

| [AclFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclFileAttributeView) | A file attribute view that supports reading or updating a file's Access Control Lists (ACL) or file owner attributes. |
| --- | --- |
| [AttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AttributeView) | An object that provides a read-only or updatable*view*of non-opaque values associated with an object in a filesystem. |
| [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes) | Basic attributes associated with a file in a file system. |
| [BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView) | A file attribute view that provides a view of a*basic set*of file attributes common to many file systems. |
| --- | --- |
| [DosFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributes) | File attributes associated with a file in a file system that supports legacy "DOS" attributes. |
| [DosFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/DosFileAttributeView) | A file attribute view that provides a view of the legacy "DOS" file attributes. |
| [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute) | An object that encapsulates the value of a file attribute that can be set atomically when creating a new file or directory by invoking the [createFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createFile(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))or [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))methods. |
| --- | --- |
| [FileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttributeView) | An attribute view that is a read-only or updatable view of non-opaque values associated with a file in a filesystem. |
| [FileOwnerAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileOwnerAttributeView) | A file attribute view that supports reading or updating the owner of a file. |
| [FileStoreAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileStoreAttributeView) | An attribute view that is a read-only or updatable view of the attributes of a [java.nio.file.FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#). |
| --- | --- |
| [GroupPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/GroupPrincipal) | A`UserPrincipal`representing a*group identity*, used to determine access rights to objects in a file system. |
| [PosixFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes) | File attributes associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| [PosixFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributeView) | A file attribute view that provides a view of the file attributes commonly associated with files on file systems used by operating systems that implement the Portable Operating System Interface (POSIX) family of standards. |
| --- | --- |
| [UserDefinedFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserDefinedFileAttributeView) | A file attribute view that provides a view of a file's user-defined attributes, sometimes known as*extended attributes*. |
| [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) | A`Principal`representing an identity used to determine access rights to objects in a file system. |

## Classes

| [AclEntry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry) | An entry in an access control list (ACL). |
| --- | --- |
| [FileTime](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileTime) | Represents the value of a file's time stamp attribute. |
| [PosixFilePermissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermissions) | This class consists exclusively of static methods that operate on sets of [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission) objects. |
| [UserPrincipalLookupService](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalLookupService) | An object to lookup user and group principals by name. |
| --- | --- |

## Exceptions

| [UserPrincipalNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipalNotFoundException) | Checked exception thrown when a lookup of [UserPrincipal](https://developer.android.com/reference/kotlin/java/nio/file/attribute/UserPrincipal) fails because the principal does not exist. |
| --- | --- |

## Enums

| [AclEntryFlag](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryFlag) | Defines the flags for used by the flags component of an ACL [entry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry). |
| --- | --- |
| [AclEntryPermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryPermission) | Defines the permissions for use with the permissions component of an ACL [entry](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntry). |
| [AclEntryType](https://developer.android.com/reference/kotlin/java/nio/file/attribute/AclEntryType) | A typesafe enumeration of the access control entry types. |
| [PosixFilePermission](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFilePermission) | Defines the bits for use with the [permissions](https://developer.android.com/reference/kotlin/java/nio/file/attribute/PosixFileAttributes#permissions())attribute. |
| --- | --- |
