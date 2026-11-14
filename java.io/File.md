Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# File

```
open class File : Comparable<File!>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.File](File.md) |

An abstract representation of file and directory pathnames.

User interfaces and operating systems use system-dependent *pathname strings* to name files and directories. This class presents an abstract, system-independent view of hierarchical pathnames. An *abstract pathname* has two components:

1. An optional system-dependent *prefix* string, such as a disk-drive specifier, `"/"` for the UNIX root directory, or `"\\\\"` for a Microsoft Windows UNC pathname, and
2. A sequence of zero or more string *names*.

The first name in an abstract pathname may be a directory name or, in the case of Microsoft Windows UNC pathnames, a hostname. Each subsequent name in an abstract pathname denotes a directory; the last name may denote either a directory or a file. The *empty* abstract pathname has no prefix and an empty name sequence.

The conversion of a pathname string to or from an abstract pathname is inherently system-dependent. When an abstract pathname is converted into a pathname string, each name is separated from the next by a single copy of the default *separator character* . The default name-separator character is defined by the system property `file.separator`, and is made available in the public static fields `` `https://developer.android.com/reference/kotlin/java/io/File#separator:kotlin.String` `` and `` `https://developer.android.com/reference/kotlin/java/io/File#separatorChar:kotlin.Char` `` of this class. When a pathname string is converted into an abstract pathname, the names within it may be separated by the default name-separator character or by any other name-separator character that is supported by the underlying system.

A pathname, whether abstract or in string form, may be either *absolute* or *relative* . An absolute pathname is complete in that no other information is required in order to locate the file that it denotes. A relative pathname, in contrast, must be interpreted in terms of information taken from some other pathname. By default the classes in the `java.io` package always resolve relative pathnames against the current user directory. This directory is named by the system property `user.dir`, and is typically the directory in which the Java virtual machine was invoked.

The *parent* of an abstract pathname may be obtained by invoking the getParent method of this class and consists of the pathname's prefix and each name in the pathname's name sequence except for the last. Each directory's absolute pathname is an ancestor of any File object with an absolute abstract pathname which begins with the directory's absolute pathname. For example, the directory denoted by the abstract pathname "/usr" is an ancestor of the directory denoted by the pathname "/usr/local/bin".

The prefix concept is used to handle root directories on UNIX platforms, and drive specifiers, root directories and UNC pathnames on Microsoft Windows platforms, as follows:

- For UNIX platforms, the prefix of an absolute pathname is always `"/"`. Relative pathnames have no prefix. The abstract pathname denoting the root directory has the prefix `"/"` and an empty name sequence.
- For Microsoft Windows platforms, the prefix of a pathname that contains a drive specifier consists of the drive letter followed by `":"` and possibly followed by `"\\"` if the pathname is absolute. The prefix of a UNC pathname is `"\\\\"`; the hostname and the share name are the first two names in the name sequence. A relative pathname that does not specify a drive has no prefix.

Instances of this class may or may not denote an actual file-system object such as a file or a directory. If it does denote such an object then that object resides in a *partition* . A partition is an operating system-specific portion of storage for a file system. A single storage device (e.g. a physical disk-drive, flash memory, CD-ROM) may contain multiple partitions. The object, if any, will reside on the partition named by some ancestor of the absolute form of this pathname.

A file system may implement restrictions to certain operations on the actual file-system object, such as reading, writing, and executing. These restrictions are collectively known as *access permissions* . The file system may have multiple sets of access permissions on a single object. For example, one set may apply to the object's *owner*, and another may apply to all other users. The access permissions on an object may cause some methods in this class to fail.

Instances of the `File` class are immutable; that is, once created, the abstract pathname represented by a `File` object will never change.

### Interoperability with `java.nio.file` package

The [`java.nio.file`](../java.nio.file/_package.md) package defines interfaces and classes for the Java virtual machine to access files, file attributes, and file systems. This API may be used to overcome many of the limitations of the `java.io.File` class. The toPath method may be used to obtain a `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` that uses the abstract path represented by a `File` object to locate a file. The resulting `Path` may be used with the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class to provide more efficient and extensive access to additional file operations, file attributes, and I/O exceptions to help diagnose errors when an operation on a file fails.

On Android strings are converted to UTF-8 byte sequences when sending filenames to the operating system, and byte sequences returned by the operating system (from the various `list` methods) are converted to strings by decoding them as UTF-8 byte sequences.

## Summary

| Public constructors ||
|---|---|
| File Creates a new `File` instance from a parent abstract pathname and a child pathname string. |
| File Creates a new `File` instance by converting the given pathname string into an abstract pathname. |
| File Creates a new `File` instance from a parent pathname string and a child pathname string. |
| File Creates a new File instance by converting the given URI into an abstract pathname. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canExecute Tests whether the application can execute the file denoted by this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canRead Tests whether the application can read the file denoted by this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canWrite Tests whether the application can modify the file denoted by this abstract pathname. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | compareTo Compares two abstract pathnames lexicographically. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | createNewFile Atomically creates a new, empty file named by this abstract pathname if and only if a file with this name does not yet exist. |
| open static [File](File.md) | createTempFile Creates an empty file in the default temporary-file directory, using the given prefix and suffix to generate its name. |
| --- | --- |
| open static [File](File.md) | createTempFile Creates a new empty file in the specified directory, using the given prefix and suffix strings to generate its name. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | delete Deletes the file or directory denoted by this abstract pathname. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | deleteOnExit Requests that the file or directory denoted by this abstract pathname be deleted when the virtual machine terminates. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Tests this abstract pathname for equality with the given object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | exists Tests whether the file or directory denoted by this abstract pathname exists. |
| open [File](File.md) | getAbsoluteFile Returns the absolute form of this abstract pathname. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getAbsolutePath Returns the absolute path of this file. |
| open [File](File.md) | getCanonicalFile Returns the canonical form of this abstract pathname. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getCanonicalPath Returns the canonical pathname string of this abstract pathname. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getFreeSpace Returns the number of unallocated bytes in the partition [named](File.md) by this abstract path name. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getName Returns the name of the file or directory denoted by this abstract pathname. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getParent Returns the pathname string of this abstract pathname's parent, or `null` if this pathname does not name a parent directory. |
| --- | --- |
| open [File](File.md)? | getParentFile Returns the abstract pathname of this abstract pathname's parent, or `null` if this pathname does not name a parent directory. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getPath Converts this abstract pathname into a pathname string. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getTotalSpace Returns the size of the partition [named](File.md) by this abstract pathname. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getUsableSpace Returns the number of bytes available to this virtual machine on the partition [named](File.md) by this abstract pathname. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Computes a hash code for this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAbsolute Tests whether this abstract pathname is absolute. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDirectory Tests whether the file denoted by this abstract pathname is a directory. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isFile Tests whether the file denoted by this abstract pathname is a normal file. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isHidden Tests whether the file named by this abstract pathname is a hidden file. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | lastModified Returns the time that the file denoted by this abstract pathname was last modified. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | length Returns the length of the file denoted by this abstract pathname. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | list Returns an array of strings naming the files and directories in the directory denoted by this abstract pathname. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | list Returns an array of strings naming the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](File.md)!\>? | listFiles Returns an array of abstract pathnames denoting the files in the directory denoted by this abstract pathname. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](File.md)!\>? | listFiles Returns an array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](File.md)!\>? | listFiles Returns an array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. |
| open static [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [File](File.md)!\> | listRoots Returns the file system roots. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | mkdir Creates the directory named by this abstract pathname. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | mkdirs Creates the directory named by this abstract pathname, including any necessary but nonexistent parent directories. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | renameTo Renames the file denoted by this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setExecutable A convenience method to set the owner's execute permission for this abstract pathname. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setExecutable Sets the owner's or everybody's execute permission for this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setLastModified Sets the last-modified time of the file or directory named by this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setReadOnly Marks the file or directory named by this abstract pathname so that only read operations are allowed. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setReadable A convenience method to set the owner's read permission for this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setReadable Sets the owner's or everybody's read permission for this abstract pathname. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setWritable A convenience method to set the owner's write permission for this abstract pathname. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | setWritable Sets the owner's or everybody's write permission for this abstract pathname. |
| open [Path](../java.nio.file/Path.md) | toPath Returns a `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` object constructed from the this abstract path. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns the pathname string of this abstract pathname. |
| --- | --- |
| open [URI](../java.net/URI.md) | toURI Constructs a URI that represents this abstract pathname. |
| open [URL](../java.net/URL.md) | toURL Converts this abstract pathname into a `file:` URL. |

| Properties ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/io/File#pathSeparator:kotlin.String` The system-dependent path-separator character, represented as a string for convenience. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/io/File#pathSeparatorChar:kotlin.Char` The system-dependent path-separator character. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/io/File#separator:kotlin.String` The system-dependent default name-separator character, represented as a string for convenience. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | `https://developer.android.com/reference/kotlin/java/io/File#separatorChar:kotlin.Char` The system-dependent default name-separator character. |

## Public constructors

### File

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
File(
    parent: File?, 
    child: String)
```

Creates a new `File` instance from a parent abstract pathname and a child pathname string.

If `parent` is `null` then the new `File` instance is created as if by invoking the single-argument `File` constructor on the given `child` pathname string.

Otherwise the `parent` abstract pathname is taken to denote a directory, and the `child` pathname string is taken to denote either a directory or a file. If the `child` pathname string is absolute then it is converted into a relative pathname in a system-dependent way. If `parent` is the empty abstract pathname then the new `File` instance is created by converting `child` into an abstract pathname and resolving the result against a system-dependent default directory. Otherwise each pathname string is converted into an abstract pathname and the child abstract pathname is resolved against the parent.

| Parameters ||
|---|---|
| `parent` | [File](File.md)?: The parent abstract pathname |
| `child` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The child pathname string |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `child` is `null` |

### File

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
File(pathname: String)
```

Creates a new `File` instance by converting the given pathname string into an abstract pathname. If the given string is the empty string, then the result is the empty abstract pathname.

| Parameters ||
|---|---|
| `pathname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A pathname string |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If the `pathname` argument is `null` |

### File

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
File(
    parent: String?, 
    child: String)
```

Creates a new `File` instance from a parent pathname string and a child pathname string.

If `parent` is `null` then the new `File` instance is created as if by invoking the single-argument `File` constructor on the given `child` pathname string.

Otherwise the `parent` pathname string is taken to denote a directory, and the `child` pathname string is taken to denote either a directory or a file. If the `child` pathname string is absolute then it is converted into a relative pathname in a system-dependent way. If `parent` is the empty string then the new `File` instance is created by converting `child` into an abstract pathname and resolving the result against a system-dependent default directory. Otherwise each pathname string is converted into an abstract pathname and the child abstract pathname is resolved against the parent.

| Parameters ||
|---|---|
| `parent` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The parent pathname string |
| `child` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The child pathname string |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If `child` is `null` |

### File

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
File(uri: URI)
```

Creates a new File instance by converting the given URI into an abstract pathname.

The exact form of a file: URI is system-dependent, hence the transformation performed by this constructor is also system-dependent.

For a given abstract pathname *f* it is guaranteed that
new File(*f* .toURI()).equals(*f* .getAbsoluteFile()) so long as the original abstract pathname, the URI, and the new abstract pathname are all created in (possibly different invocations of) the same Java virtual machine. This relationship typically does not hold, however, when a file: URI that is created in a virtual machine on one operating system is converted into an abstract pathname in a virtual machine on a different operating system.

| Parameters ||
|---|---|
| `uri` | [URI](../java.net/URI.md): An absolute, hierarchical URI with a scheme equal to "file", a non-empty path component, and undefined authority, query, and fragment components |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the preconditions on the parameter do not hold |
| `java.lang.NullPointerException` | If uri is null |

**See Also**

- toURI
- `https://developer.android.com/reference/kotlin/java/net/URI.html#`

## Public methods

### canExecute

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canExecute(): Boolean
```

Tests whether the application can execute the file denoted by this abstract pathname.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the abstract pathname exists *and* the application is allowed to execute the file |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkExec `` method denies execute access to the file |

### canRead

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canRead(): Boolean
```

Tests whether the application can read the file denoted by this abstract pathname.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file specified by this abstract pathname exists *and* can be read by the application; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### canWrite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canWrite(): Boolean
```

Tests whether the application can modify the file denoted by this abstract pathname.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file system actually contains a file denoted by this abstract pathname *and* the application is allowed to write to the file; `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun compareTo(other: File): Int
```

Compares two abstract pathnames lexicographically. The ordering defined by this method depends upon the underlying system. On UNIX systems, alphabetic case is significant in comparing pathnames; on Microsoft Windows systems it is not.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `pathname` | The abstract pathname to be compared to this abstract pathname |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Zero if the argument is equal to this abstract pathname, a value less than zero if this abstract pathname is lexicographically less than the argument, or a value greater than zero if this abstract pathname is lexicographically greater than the argument |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### createNewFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun createNewFile(): Boolean
```

Atomically creates a new, empty file named by this abstract pathname if and only if a file with this name does not yet exist. The check for the existence of the file and the creation of the file if it does not exist are a single operation that is atomic with respect to all other filesystem activities that might affect the file.

Note: this method should *not* be used for file-locking, as the resulting protocol cannot be made to work reliably. The `https://developer.android.com/reference/kotlin/java/nio/channels/FileLock.html#` facility should be used instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the named file does not exist and was successfully created; `false` if the named file already exists |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurred |
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### createTempFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createTempFile(
    prefix: String, 
    suffix: String?
): File
```

Creates an empty file in the default temporary-file directory, using the given prefix and suffix to generate its name. Invoking this method is equivalent to invoking `` createTempFile ``.

The createTempFile method provides an alternative method to create an empty file in the temporary-file directory. Files created by that method may have more restrictive access permissions to files created by this method and so may be more suited to security-sensitive applications.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The prefix string to be used in generating the file's name; must be at least three characters long |
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The suffix string to be used in generating the file's name; may be `null`, in which case the suffix `".tmp"` will be used |

| Return ||
|---|---|
| File | An abstract pathname denoting a newly-created empty file |

| Exceptions ||
|---|---|
| `java.io.IOException` | If a file could not be created |
| `java.lang.IllegalArgumentException` | If the `prefix` argument contains fewer than three characters |
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method does not allow a file to be created |
| --- | --- |

**See Also**

### createTempFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun createTempFile(
    prefix: String, 
    suffix: String?, 
    directory: File?
): File
```

Creates a new empty file in the specified directory, using the given prefix and suffix strings to generate its name. If this method returns successfully then it is guaranteed that:

1. The file denoted by the returned abstract pathname did not exist before this method was invoked, and
2. Neither this method nor any of its variants will return the same abstract pathname again in the current invocation of the virtual machine.

This method provides only part of a temporary-file facility. To arrange for a file created by this method to be deleted automatically, use the `` deleteOnExit `` method.

The `prefix` argument must be at least three characters long. It is recommended that the prefix be a short, meaningful string such as `"hjb"` or `"mail"`. The `suffix` argument may be `null`, in which case the suffix `".tmp"` will be used.

To create the new file, the prefix and the suffix may first be adjusted to fit the limitations of the underlying platform. If the prefix is too long then it will be truncated, but its first three characters will always be preserved. If the suffix is too long then it too will be truncated, but if it begins with a period character (`'.'`) then the period and the first three characters following it will always be preserved. Once these adjustments have been made the name of the new file will be generated by concatenating the prefix, five or more internally-generated characters, and the suffix.

If the `directory` argument is `null` then the system-dependent default temporary-file directory will be used. The default temporary-file directory is specified by the system property `java.io.tmpdir`. On UNIX systems the default value of this property is typically `"/tmp"` or `"/var/tmp"`; on Microsoft Windows systems it is typically `"C:\\WINNT\\TEMP"`. A different value may be given to this system property when the Java virtual machine is invoked, but programmatic changes to this property are not guaranteed to have any effect upon the temporary directory used by this method.

| Parameters ||
|---|---|
| `prefix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The prefix string to be used in generating the file's name; must be at least three characters long |
| `suffix` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The suffix string to be used in generating the file's name; may be `null`, in which case the suffix `".tmp"` will be used |
| `directory` | [File](File.md)?: The directory in which the file is to be created, or `null` if the default temporary-file directory is to be used |
| --- | --- |

| Return ||
|---|---|
| File | An abstract pathname denoting a newly-created empty file |

| Exceptions ||
|---|---|
| `java.io.IOException` | If a file could not be created |
| `java.lang.IllegalArgumentException` | If the `prefix` argument contains fewer than three characters |
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method does not allow a file to be created |
| --- | --- |

### delete

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(): Boolean
```

Deletes the file or directory denoted by this abstract pathname. If this pathname denotes a directory, then the directory must be empty in order to be deleted.

Note that the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines the delete method to throw an IOException when a file cannot be deleted. This is useful for error reporting and to diagnose why a file cannot be deleted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file or directory is successfully deleted; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkDelete `` method denies delete access to the file |

### deleteOnExit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun deleteOnExit(): Unit
```

Requests that the file or directory denoted by this abstract pathname be deleted when the virtual machine terminates. Files (or directories) are deleted in the reverse order that they are registered. Invoking this method to delete a file or directory that is already registered for deletion has no effect. Deletion will be attempted only for normal termination of the virtual machine, as defined by the Java Language Specification.

Once deletion has been requested, it is not possible to cancel the request. This method should therefore be used with care.

Note: this method should *not* be used for file-locking, as the resulting protocol cannot be made to work reliably. The `https://developer.android.com/reference/kotlin/java/nio/channels/FileLock.html#` facility should be used instead.

*Note that on Android, the application lifecycle does not include VM termination, so calling this method will not ensure that files are deleted*. Instead, you should use the most appropriate out of:

- Use a `finally` clause to manually invoke delete.
- Maintain your own set of files to delete, and process it at an appropriate point in your application's lifecycle.
- Use the Unix trick of deleting the file as soon as all readers and writers have opened it. No new readers/writers will be able to access the file, but all existing ones will still have access until the last one closes the file.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkDelete `` method denies delete access to the file |

**See Also**

- delete

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Tests this abstract pathname for equality with the given object. Returns `true` if and only if the argument is not `null` and is an abstract pathname that denotes the same file or directory as this abstract pathname. Whether or not two abstract pathnames are equal depends upon the underlying system. On UNIX systems, alphabetic case is significant in comparing pathnames; on Microsoft Windows systems it is not.

| Parameters ||
|---|---|
| `obj` | The object to be compared with this abstract pathname |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the objects are the same; `false` otherwise |

### exists

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun exists(): Boolean
```

Tests whether the file or directory denoted by this abstract pathname exists.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file or directory denoted by this abstract pathname exists; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file or directory |

### getAbsoluteFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAbsoluteFile(): File
```

Returns the absolute form of this abstract pathname. Equivalent to ``new File(this.getAbsolutePath)``.

| Return ||
|---|---|
| File | The absolute abstract pathname denoting the same file or directory as this abstract pathname |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a required system property value cannot be accessed. |

### getAbsolutePath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAbsolutePath(): String
```

Returns the absolute path of this file. An absolute path is a path that starts at a root of the file system. On Android, there is only one root: `/`.

A common use for absolute paths is when passing paths to a `Process` as command-line arguments, to remove the requirement implied by relative paths, that the child must have the same working directory as its parent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The absolute pathname string denoting the same file or directory as this abstract pathname |

**See Also**

- isAbsolute

### getCanonicalFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCanonicalFile(): File
```

Returns the canonical form of this abstract pathname. Equivalent to ``new File(this.getCanonicalPath)``.

| Return ||
|---|---|
| File | The canonical pathname string denoting the same file or directory as this abstract pathname |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs, which is possible because the construction of the canonical pathname may require filesystem queries |
| `java.lang.SecurityException` | If a required system property value cannot be accessed, or if a security manager exists and its `java.lang.SecurityManager#checkRead` method denies read access to the file |

**See Also**

- toRealPath

### getCanonicalPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCanonicalPath(): String
```

Returns the canonical pathname string of this abstract pathname.

A canonical pathname is both absolute and unique. The precise definition of canonical form is system-dependent. This method first converts this pathname to absolute form if necessary, as if by invoking the getAbsolutePath method, and then maps it to its unique form in a system-dependent way. This typically involves removing redundant names such as "." and ".." from the pathname, resolving symbolic links (on UNIX platforms), and converting drive letters to a standard case (on Microsoft Windows platforms).

Every pathname that denotes an existing file or directory has a unique canonical form. Every pathname that denotes a nonexistent file or directory also has a unique canonical form. The canonical form of the pathname of a nonexistent file or directory may be different from the canonical form of the same pathname after the file or directory is created. Similarly, the canonical form of the pathname of an existing file or directory may be different from the canonical form of the same pathname after the file or directory is deleted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The canonical pathname string denoting the same file or directory as this abstract pathname |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an I/O error occurs, which is possible because the construction of the canonical pathname may require filesystem queries |
| `java.lang.SecurityException` | If a required system property value cannot be accessed, or if a security manager exists and its `java.lang.SecurityManager#checkRead` method denies read access to the file |

**See Also**

- toRealPath

### getFreeSpace

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFreeSpace(): Long
```

Returns the number of unallocated bytes in the partition [named](File.md) by this abstract path name.

The returned number of unallocated bytes is a hint, but not a guarantee, that it is possible to use most or any of these bytes. The number of unallocated bytes is most likely to be accurate immediately after this call. It is likely to be made inaccurate by any external I/O operations including those made on the system outside of this virtual machine. This method makes no guarantee that write operations to this file system will succeed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The number of unallocated bytes on the partition or 0L if the abstract pathname does not name a partition. This value will be less than or equal to the total file system size returned by getTotalSpace. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`("getFileSystemAttributes") or its checkRead method denies read access to the file named by this abstract pathname |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String
```

Returns the name of the file or directory denoted by this abstract pathname. This is just the last name in the pathname's name sequence. If the pathname's name sequence is empty, then the empty string is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the file or directory denoted by this abstract pathname, or the empty string if this pathname's name sequence is empty |

### getParent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParent(): String?
```

Returns the pathname string of this abstract pathname's parent, or `null` if this pathname does not name a parent directory.

The *parent* of an abstract pathname consists of the pathname's prefix, if any, and each name in the pathname's name sequence except for the last. If the name sequence is empty then the pathname does not name a parent directory.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The pathname string of the parent directory named by this abstract pathname, or `null` if this pathname does not name a parent |

### getParentFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParentFile(): File?
```

Returns the abstract pathname of this abstract pathname's parent, or `null` if this pathname does not name a parent directory.

The *parent* of an abstract pathname consists of the pathname's prefix, if any, and each name in the pathname's name sequence except for the last. If the name sequence is empty then the pathname does not name a parent directory.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/File#?` | The abstract pathname of the parent directory named by this abstract pathname, or `null` if this pathname does not name a parent |

### getPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPath(): String
```

Converts this abstract pathname into a pathname string. The resulting string uses the `https://developer.android.com/reference/kotlin/java/io/File#separator:kotlin.String` to separate the names in the name sequence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The string form of this abstract pathname |

### getTotalSpace

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getTotalSpace(): Long
```

Returns the size of the partition [named](File.md) by this abstract pathname.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The size, in bytes, of the partition or 0L if this abstract pathname does not name a partition |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`("getFileSystemAttributes") or its checkRead method denies read access to the file named by this abstract pathname |

### getUsableSpace

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getUsableSpace(): Long
```

Returns the number of bytes available to this virtual machine on the partition [named](File.md) by this abstract pathname. When possible, this method checks for write permissions and other operating system restrictions and will therefore usually provide a more accurate estimate of how much new data can actually be written than getFreeSpace.

The returned number of available bytes is a hint, but not a guarantee, that it is possible to use most or any of these bytes. The number of unallocated bytes is most likely to be accurate immediately after this call. It is likely to be made inaccurate by any external I/O operations including those made on the system outside of this virtual machine. This method makes no guarantee that write operations to this file system will succeed.

On Android (and other Unix-based systems), this method returns the number of free bytes available to non-root users, regardless of whether you're actually running as root, and regardless of any quota or other restrictions that might apply to the user. (The `getFreeSpace` method returns the number of bytes potentially available to root.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The number of available bytes on the partition or 0L if the abstract pathname does not name a partition. On systems where this information is not available, this method will be equivalent to a call to getFreeSpace. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager has been installed and it denies `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`("getFileSystemAttributes") or its checkRead method denies read access to the file named by this abstract pathname |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Computes a hash code for this abstract pathname. Because equality of abstract pathnames is inherently system-dependent, so is the computation of their hash codes. On UNIX systems, the hash code of an abstract pathname is equal to the exclusive *or* of the hash code of its pathname string and the decimal value `1234321`. On Microsoft Windows systems, the hash code is equal to the exclusive *or* of the hash code of its pathname string converted to lower case and the decimal value `1234321`. Locale is not taken into account on lowercasing the pathname string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | A hash code for this abstract pathname |

### isAbsolute

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAbsolute(): Boolean
```

Tests whether this abstract pathname is absolute. The definition of absolute pathname is system dependent. On Android, absolute paths start with the character '/'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this abstract pathname is absolute, `false` otherwise |

### isDirectory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isDirectory(): Boolean
```

Tests whether the file denoted by this abstract pathname is a directory.

Where it is required to distinguish an I/O exception from the case that the file is not a directory, or where several attributes of the same file are required at the same time, then the java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.Class,LinkOption\[\]) method may be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file denoted by this abstract pathname exists *and* is a directory; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### isFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isFile(): Boolean
```

Tests whether the file denoted by this abstract pathname is a normal file. A file is *normal* if it is not a directory and, in addition, satisfies other system-dependent criteria. Any non-directory file created by a Java application is guaranteed to be a normal file.

Where it is required to distinguish an I/O exception from the case that the file is not a normal file, or where several attributes of the same file are required at the same time, then the java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.Class,LinkOption\[\]) method may be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file denoted by this abstract pathname exists *and* is a normal file; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### isHidden

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isHidden(): Boolean
```

Tests whether the file named by this abstract pathname is a hidden file. The exact definition of *hidden* is system-dependent. On UNIX systems, a file is considered to be hidden if its name begins with a period character (`'.'`). On Microsoft Windows systems, a file is considered to be hidden if it has been marked as such in the filesystem.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the file denoted by this abstract pathname is hidden according to the conventions of the underlying platform |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### lastModified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastModified(): Long
```

Returns the time that the file denoted by this abstract pathname was last modified.

Where it is required to distinguish an I/O exception from the case where `0L` is returned, or where several attributes of the same file are required at the same time, or where the time of last access or the creation time are required, then the java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.Class,LinkOption\[\]) method may be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | A `long` value representing the time the file was last modified, measured in milliseconds since the epoch (00:00:00 GMT, January 1, 1970), or `0L` if the file does not exist or if an I/O error occurs |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun length(): Long
```

Returns the length of the file denoted by this abstract pathname. The return value is unspecified if this pathname denotes a directory.

Where it is required to distinguish an I/O exception from the case that `0L` is returned, or where several attributes of the same file are required at the same time, then the java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.Class,LinkOption\[\]) method may be used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The length, in bytes, of the file denoted by this abstract pathname, or `0L` if the file does not exist. Some operating systems may return `0L` for pathnames denoting system-dependent entities such as devices or pipes. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method denies read access to the file |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun list(): Array<String!>?
```

Returns an array of strings naming the files and directories in the directory denoted by this abstract pathname.

If this abstract pathname does not denote a directory, then this method returns `null`. Otherwise an array of strings is returned, one for each file or directory in the directory. Names denoting the directory itself and the directory's parent directory are not included in the result. Each string is a file name rather than a complete path.

There is no guarantee that the name strings in the resulting array will appear in any specific order; they are not, in particular, guaranteed to appear in alphabetical order.

Note that the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines the newDirectoryStream method to open a directory and iterate over the names of the files in the directory. This may use less resources when working with very large directories, and may be more responsive when working with remote directories.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | An array of strings naming the files and directories in the directory denoted by this abstract pathname. The array will be empty if the directory is empty. Returns `null` if this abstract pathname does not denote a directory, or if an I/O error occurs. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its checkRead method denies read access to the directory |

### list

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun list(filter: FilenameFilter?): Array<String!>?
```

Returns an array of strings naming the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. The behavior of this method is the same as that of the list method, except that the strings in the returned array must satisfy the filter. If the given `filter` is `null` then all names are accepted. Otherwise, a name satisfies the filter if and only if the value `true` results when the accept method of the filter is invoked on this abstract pathname and the name of a file or directory in the directory that it denotes.

| Parameters ||
|---|---|
| `filter` | [FilenameFilter](FilenameFilter.md)?: A filename filter |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>?` | An array of strings naming the files and directories in the directory denoted by this abstract pathname that were accepted by the given `filter`. The array will be empty if the directory is empty or if no names were accepted by the filter. Returns `null` if this abstract pathname does not denote a directory, or if an I/O error occurs. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its checkRead method denies read access to the directory |

**See Also**

- newDirectoryStream

### listFiles

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listFiles(): Array<File!>?
```

Returns an array of abstract pathnames denoting the files in the directory denoted by this abstract pathname.

If this abstract pathname does not denote a directory, then this method returns `null`. Otherwise an array of `File` objects is returned, one for each file or directory in the directory. Pathnames denoting the directory itself and the directory's parent directory are not included in the result. Each resulting abstract pathname is constructed from this abstract pathname using the File constructor. Therefore if this pathname is absolute then each resulting pathname is absolute; if this pathname is relative then each resulting pathname will be relative to the same directory.

There is no guarantee that the name strings in the resulting array will appear in any specific order; they are not, in particular, guaranteed to appear in alphabetical order.

Note that the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines the newDirectoryStream method to open a directory and iterate over the names of the files in the directory. This may use less resources when working with very large directories.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File#!>?` | An array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname. The array will be empty if the directory is empty. Returns `null` if this abstract pathname does not denote a directory, or if an I/O error occurs. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its checkRead method denies read access to the directory |

### listFiles

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listFiles(filter: FileFilter?): Array<File!>?
```

Returns an array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. The behavior of this method is the same as that of the listFiles method, except that the pathnames in the returned array must satisfy the filter. If the given `filter` is `null` then all pathnames are accepted. Otherwise, a pathname satisfies the filter if and only if the value `true` results when the accept method of the filter is invoked on the pathname.

| Parameters ||
|---|---|
| `filter` | [FileFilter](FileFilter.md)?: A file filter |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File#!>?` | An array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname. The array will be empty if the directory is empty. Returns `null` if this abstract pathname does not denote a directory, or if an I/O error occurs. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its checkRead method denies read access to the directory |

**See Also**

- newDirectoryStream

### listFiles

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listFiles(filter: FilenameFilter?): Array<File!>?
```

Returns an array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname that satisfy the specified filter. The behavior of this method is the same as that of the listFiles method, except that the pathnames in the returned array must satisfy the filter. If the given `filter` is `null` then all pathnames are accepted. Otherwise, a pathname satisfies the filter if and only if the value `true` results when the accept method of the filter is invoked on this abstract pathname and the name of a file or directory in the directory that it denotes.

| Parameters ||
|---|---|
| `filter` | [FilenameFilter](FilenameFilter.md)?: A filename filter |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/io/File#!>?` | An array of abstract pathnames denoting the files and directories in the directory denoted by this abstract pathname. The array will be empty if the directory is empty. Returns `null` if this abstract pathname does not denote a directory, or if an I/O error occurs. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its checkRead method denies read access to the directory |

**See Also**

- newDirectoryStream

### listRoots

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun listRoots(): Array<File!>
```

Returns the file system roots. On Android and other Unix systems, there is a single root, `/`.

### mkdir

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mkdir(): Boolean
```

Creates the directory named by this abstract pathname.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the directory was created; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method does not permit the named directory to be created |

### mkdirs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun mkdirs(): Boolean
```

Creates the directory named by this abstract pathname, including any necessary but nonexistent parent directories. Note that if this operation fails it may have succeeded in creating some of the necessary parent directories.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the directory was created, along with all necessary parent directories; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkRead `` method does not permit verification of the existence of the named directory and all necessary parent directories; or if the `` checkWrite `` method does not permit the named directory and all necessary parent directories to be created |

### renameTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun renameTo(dest: File): Boolean
```

Renames the file denoted by this abstract pathname.

Many failures are possible. Some of the more likely failures include:

- Write permission is required on the directories containing both the source and destination paths.
- Search permission is required for all parents of both paths.
- Both paths be on the same mount point. On Android, applications are most likely to hit this restriction when attempting to copy between internal storage and an SD card.

The return value should always be checked to make sure that the rename operation was successful.

Note that the `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines the move method to move or rename a file in a platform independent manner.

| Parameters ||
|---|---|
| `dest` | [File](File.md): The new abstract pathname for the named file |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the renaming succeeded; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | If parameter `dest` is `null` |
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to either the old or new pathnames |

### setExecutable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExecutable(executable: Boolean): Boolean
```

A convenience method to set the owner's execute permission for this abstract pathname.

An invocation of this method of the form file.setExcutable(arg) behaves in exactly the same way as the invocation

```kotlin
file.setExecutable(arg, true) 
```

| Parameters ||
|---|---|
| `executable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow execute operations; if `false` to disallow execute operations |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. If `executable` is `false` and the underlying file system does not implement an execute permission, then the operation will fail. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### setExecutable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExecutable(
    executable: Boolean, 
    ownerOnly: Boolean
): Boolean
```

Sets the owner's or everybody's execute permission for this abstract pathname.

The `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines methods that operate on file attributes including file permissions. This may be used when finer manipulation of file permissions is required.

| Parameters ||
|---|---|
| `executable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow execute operations; if `false` to disallow execute operations |
| `ownerOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, the execute permission applies only to the owner's execute permission; otherwise, it applies to everybody. If the underlying file system can not distinguish the owner's execute permission from that of others, then the permission will apply to everybody, regardless of this value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. If `executable` is `false` and the underlying file system does not implement an execute permission, then the operation will fail. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### setLastModified

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setLastModified(time: Long): Boolean
```

Sets the last-modified time of the file or directory named by this abstract pathname.

All platforms support file-modification times to the nearest second, but some provide more precision. The argument will be truncated to fit the supported precision. If the operation succeeds and no intervening operations on the file take place, then the next invocation of the `` lastModified `` method will return the (possibly truncated) `time` argument that was passed to this method.

| Parameters ||
|---|---|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The new last-modified time, measured in milliseconds since the epoch (00:00:00 GMT, January 1, 1970) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the argument is negative |
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the named file |

### setReadOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReadOnly(): Boolean
```

Marks the file or directory named by this abstract pathname so that only read operations are allowed. After invoking this method the file or directory will not change until it is either deleted or marked to allow write access. Whether or not a read-only file or directory may be deleted depends upon the underlying system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the named file |

### setReadable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReadable(readable: Boolean): Boolean
```

A convenience method to set the owner's read permission for this abstract pathname.

An invocation of this method of the form file.setReadable(arg) behaves in exactly the same way as the invocation

```kotlin
file.setReadable(arg, true) 
```

| Parameters ||
|---|---|
| `readable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow read operations; if `false` to disallow read operations |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. If `readable` is `false` and the underlying file system does not implement a read permission, then the operation will fail. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### setReadable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setReadable(
    readable: Boolean, 
    ownerOnly: Boolean
): Boolean
```

Sets the owner's or everybody's read permission for this abstract pathname.

The `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines methods that operate on file attributes including file permissions. This may be used when finer manipulation of file permissions is required.

| Parameters ||
|---|---|
| `readable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow read operations; if `false` to disallow read operations |
| `ownerOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, the read permission applies only to the owner's read permission; otherwise, it applies to everybody. If the underlying file system can not distinguish the owner's read permission from that of others, then the permission will apply to everybody, regardless of this value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. If `readable` is `false` and the underlying file system does not implement a read permission, then the operation will fail. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### setWritable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWritable(writable: Boolean): Boolean
```

A convenience method to set the owner's write permission for this abstract pathname.

An invocation of this method of the form file.setWritable(arg) behaves in exactly the same way as the invocation

```kotlin
file.setWritable(arg, true) 
```

| Parameters ||
|---|---|
| `writable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow write operations; if `false` to disallow write operations |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the file |

### setWritable

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWritable(
    writable: Boolean, 
    ownerOnly: Boolean
): Boolean
```

Sets the owner's or everybody's write permission for this abstract pathname.

The `https://developer.android.com/reference/kotlin/java/nio/file/Files.html#` class defines methods that operate on file attributes including file permissions. This may be used when finer manipulation of file permissions is required.

| Parameters ||
|---|---|
| `writable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, sets the access permission to allow write operations; if `false` to disallow write operations |
| `ownerOnly` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If `true`, the write permission applies only to the owner's write permission; otherwise, it applies to everybody. If the underlying file system can not distinguish the owner's write permission from that of others, then the permission will apply to everybody, regardless of this value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if and only if the operation succeeded. The operation will fail if the user does not have permission to change the access permissions of this abstract pathname. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a security manager exists and its `` checkWrite `` method denies write access to the named file |

### toPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toPath(): Path
```

Returns a `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` object constructed from the this abstract path. The resulting is associated with the getDefault

The first invocation of this method works as if invoking it were equivalent to evaluating the expression:

```kotlin
<code><a docref="java.nio.file.FileSystems$getDefault()">FileSystems.getDefault</a></code>().<code><a docref="java.nio.file.FileSystem$getPath(kotlin.String, kotlin.Array((kotlin.String)))">getPath</a></code>(this.<code><a docref="java.io.File$getPath()">getPath</a></code>());
  
```
Subsequent invocations of this method return the same `Path`.

If this abstract pathname is the empty abstract pathname then this method returns a `Path` that may be used to access the current user directory.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` | a `Path` constructed from this abstract path |

| Exceptions ||
|---|---|
| `java.nio.file.InvalidPathException` | if a `Path` object cannot be constructed from the abstract path (see getPath) |

**See Also**

- toFile

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns the pathname string of this abstract pathname. This is just the string returned by the `` getPath `` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The string form of this abstract pathname |

### toURI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toURI(): URI
```

Constructs a URI that represents this abstract pathname.

The exact form of the URI is system-dependent. If it can be determined that the file denoted by this abstract pathname is a directory, then the resulting URI will end with a slash.

For a given abstract pathname *f*, it is guaranteed that
new File(*f* .toURI()).equals(*f* .getAbsoluteFile()) so long as the original abstract pathname, the URI, and the new abstract pathname are all created in (possibly different invocations of) the same Java virtual machine. Due to the system-dependent nature of abstract pathnames, however, this relationship typically does not hold when a file: URI that is created in a virtual machine on one operating system is converted into an abstract pathname in a virtual machine on a different operating system.

Note that when this abstract pathname represents a UNC pathname then all components of the UNC (including the server name component) are encoded in the `URI` path. The authority component is undefined, meaning that it is represented as `null`. The `https://developer.android.com/reference/kotlin/java/nio/file/Path.html#` class defines the toUri method to encode the server name in the authority component of the resulting `URI`. The toPath method may be used to obtain a `Path` representing this abstract pathname.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URI.html#` | An absolute, hierarchical URI with a scheme equal to "file", a path representing this abstract pathname, and undefined authority, query, and fragment components |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | If a required system property value cannot be accessed. |

**See Also**

- File
- `https://developer.android.com/reference/kotlin/java/net/URI.html#`
- toURL

### toURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toURL(): URL
```

**Deprecated:** *This method does not automatically escape characters that are illegal in URLs. It is recommended that new code convert an abstract pathname into a URL by first converting it into a URI, via the toURI method, and then converting the URI into a URL via the toURL method.*

Converts this abstract pathname into a `file:` URL. The exact form of the URL is system-dependent. If it can be determined that the file denoted by this abstract pathname is a directory, then the resulting URL will end with a slash.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/URL.html#` | A URL object representing the equivalent file URL |

| Exceptions ||
|---|---|
| `java.net.MalformedURLException` | If the path cannot be parsed as a URL |

**See Also**

- toURI
- `https://developer.android.com/reference/kotlin/java/net/URI.html#`
- toURL
- `https://developer.android.com/reference/kotlin/java/net/URL.html#`

## Properties

### pathSeparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val pathSeparator: String
```

The system-dependent path-separator character, represented as a string for convenience. This string contains a single character, namely `` `https://developer.android.com/reference/kotlin/java/io/File#pathSeparatorChar:kotlin.Char` ``.

### pathSeparatorChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val pathSeparatorChar: Char
```

The system-dependent path-separator character. This field is initialized to contain the first character of the value of the system property `path.separator`. This character is used to separate filenames in a sequence of files given as a *path list* . On UNIX systems, this character is `':'`; on Microsoft Windows systems it is `';'`.
**See Also**

- getProperty

### separator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val separator: String
```

The system-dependent default name-separator character, represented as a string for convenience. This string contains a single character, namely `` `https://developer.android.com/reference/kotlin/java/io/File#separatorChar:kotlin.Char` ``.

### separatorChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val separatorChar: Char
```

The system-dependent default name-separator character. This field is initialized to contain the first character of the value of the system property `file.separator`. On UNIX systems the value of this field is `'/'`; on Microsoft Windows systems it is `'\\'`.
**See Also**

- getProperty
