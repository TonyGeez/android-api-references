# FileSystemProvider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemProvider

```
abstract class FileSystemProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.file.spi.FileSystemProvider](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#) |

Service-provider class for file systems. The methods defined by the class will typically delegate to an instance of this class.

A file system provider is a concrete implementation of this class that implements the abstract methods defined by this class. A provider is identified by a`URI` [scheme](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getScheme()). The default provider is identified by the URI scheme "file". It creates the [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#) that provides access to the file systems accessible to the Java virtual machine. The [FileSystems](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#) class defines how file system providers are located and loaded. The default provider is typically a system-default provider but may be overridden if the system property`java.nio.file.spi.DefaultFileSystemProvider`is set. In that case, the provider has a one argument constructor whose formal parameter type is`FileSystemProvider`. All other providers have a zero argument constructor that initializes the provider.

A provider is a factory for one or more [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#) instances. Each file system is identified by a`URI`where the URI's scheme matches the provider's [scheme](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getScheme()). The default file system, for example, is identified by the URI`"file:///"`. A memory-based file system, for example, may be identified by a URI such as`"memory:///?name=logfs"`. The #newFileSystem method may be used to create a file system, and the [getFileSystem](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getFileSystem(java.net.URI))method may be used to obtain a reference to an existing file system created by the provider. Where a provider is the factory for a single file system then it is provider dependent if the file system is created when the provider is initialized, or later when the`newFileSystem`method is invoked. In the case of the default provider, the`FileSystem`is created when the provider is initialized.

All of the methods in this class are safe for use by multiple concurrent threads.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemProvider](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#FileSystemProvider())`()` Initializes a new instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [checkAccess](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#checkAccess(java.nio.file.Path,%20java.nio.file.AccessMode))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `modes:` ` [AccessMode](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode.html#)!`)` Checks the existence, and optionally the accessibility, of a file. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [copy](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#copy(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))`(`source:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `target:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `options:` ` [CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption.html#)!`)` Copy a file to a target file. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))`(`dir:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Creates a new directory. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createLink](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#createLink(java.nio.file.Path,%20java.nio.file.Path))`(`link:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `existing:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Creates a new link (directory entry) for an existing file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [createSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#createSymbolicLink(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))`(`link:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `target:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Creates a symbolic link to a target. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [delete](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#delete(java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Deletes a file. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deleteIfExists](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#deleteIfExists(java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Deletes a file if it exists. |
| abstractV | [getFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getFileAttributeView(java.nio.file.Path,%20java.lang.Class,%20java.nio.file.LinkOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!`)` Returns a file attribute view of a given type. |
| abstract [FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#)! | [getFileStore](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getFileStore(java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Returns the [FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#) representing the file store where a file is located. |
| abstract [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | [getFileSystem](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getFileSystem(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`)` Returns an existing`FileSystem`created by this provider. |
| abstract [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)! | [getPath](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getPath(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`)` Return a`Path`object by converting the given [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#). |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getScheme](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#getScheme())`()` Returns the URI scheme that identifies this provider. |
| openstatic [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FileSystemProvider](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#)!\>! | [installedProviders](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#installedProviders())`()` Returns a list of the installed file system providers. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHidden](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#isHidden(java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Tells whether or not a file is considered*hidden*. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSameFile](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#isSameFile(java.nio.file.Path,%20java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `path2:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Tests if two paths locate the same file. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [move](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#move(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))`(`source:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `target:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `options:` ` [CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption.html#)!`)` Move or rename a file to a target file. |
| open [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel.html#)! | [newAsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newAsynchronousFileChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.util.concurrent.ExecutorService,%20java.nio.file.attribute.FileAttribute))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!>!`, `executor:` ` [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file. |
| abstract [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel.html#)! | [newByteChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newByteChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!>!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Opens or creates a file, returning a seekable byte channel to access the file. |
| abstract [DirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream.html#)\< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!\>! | [newDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newDirectoryStream(java.nio.file.Path,%20java.nio.file.DirectoryStream.Filter))`(`dir:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `filter:` ` [DirectoryStream.Filter](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream.Filter.html#)<in` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!>!`)` Opens a directory, returning a`DirectoryStream`to iterate over the entries in the directory. |
| open [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#)! | [newFileChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!>!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)<*>!`)` Opens or creates a file for reading and/or writing, returning a file channel to access the file. |
| abstract [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | [newFileSystem](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`, `env:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!`)` Constructs a new`FileSystem`object identified by a URI. |
| open [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | [newFileSystem](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `env:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` `*>!`)` Constructs a new`FileSystem`to access the contents of a file as a file system. |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [newInputStream](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newInputStream(java.nio.file.Path,%20java.nio.file.OpenOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `options:` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!`)` Opens a file, returning an input stream to read from the file. |
| open [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [newOutputStream](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newOutputStream(java.nio.file.Path,%20java.nio.file.OpenOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `vararg` `options:` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!`)` Opens or creates a file, returning an output stream that may be used to write bytes to the file. |
| abstractA | [readAttributes](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#readAttributes(java.nio.file.Path,%20java.lang.Class,%20java.nio.file.LinkOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<A>!`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!`)` Reads a file's attributes as a bulk operation. |
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [readAttributes](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#readAttributes(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `attributes:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!`)` Reads a set of file attributes as a bulk operation. |
| open [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)! | [readSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#readSymbolicLink(java.nio.file.Path))`(`link:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`)` Reads the target of a symbolic link. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!`, `attribute:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!`)` Sets the value of a file attribute. |

## Protected constructors

### FileSystemProvider

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected FileSystemProvider()
```

Initializes a new instance of this class.

During construction a provider may safely access files associated with the default provider but care needs to be taken to avoid circular loading of other installed providers. If circular loading of installed providers is detected then an unspecified error is thrown.

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("fileSystemProvider")` |

## Public methods

### checkAccess

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun checkAccess(
    path: Path!, 
    vararg modes: AccessMode!
): Unit
```

Checks the existence, and optionally the accessibility, of a file.

This method may be used by the [isReadable](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isReadable(java.nio.file.Path)), [isWritable](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isWritable(java.nio.file.Path))and [isExecutable](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isExecutable(java.nio.file.Path))methods to check the accessibility of a file.

This method checks the existence of a file and that this Java virtual machine has appropriate privileges that would allow it access the file according to all of access modes specified in the`modes`parameter as follows:

| Value | Description |
| [READ](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode.html#) | Checks that the file exists and that the Java virtual machine has permission to read the file. |
| [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode.html#) | Checks that the file exists and that the Java virtual machine has permission to write to the file, |
| [EXECUTE](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode.html#) | Checks that the file exists and that the Java virtual machine has permission to java.lang.Runtime#exec the file. The semantics may differ when checking access to a directory. For example, on UNIX systems, checking for`EXECUTE`access checks that the Java virtual machine has permission to search the directory in order to access file or subdirectories. |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

If the`modes`parameter is of length zero, then the existence of the file is checked.

This method follows symbolic links if the file referenced by this object is a symbolic link. Depending on the implementation, this method may require to read file permissions, access control lists, or other file attributes in order to check the effective access to the file. To determine the effective access to a file may require access to several attributes and so in some implementations this method may not be atomic with respect to other file system operations.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to check |
| `modes` | [AccessMode](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode.html#)!:The access modes to check; may have zero elements |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | an implementation is required to support checking for`READ`,`WRITE`, and`EXECUTE`access. This exception is specified to allow for the`Access`enum to be extended in future releases. |
| `java.nio.file.NoSuchFileException` | if a file does not exist*(optional specific exception)* |
| `java.nio.file.AccessDeniedException` | the requested access would be denied or the access cannot be determined because the Java virtual machine has insufficient privileges or other reasons.*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))is invoked when checking read access to the file or only the existence of the file, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))is invoked when checking write access to the file, and [checkExec](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkExec(kotlin.String))is invoked when checking execute access. |

### copy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun copy(
    source: Path!, 
    target: Path!, 
    vararg options: CopyOption!
): Unit
```

Copy a file to a target file. This method works in exactly the manner specified by the[Files.copy(Path,Path,CopyOption[])](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#copy(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))method except that both the source and target paths must be associated with this provider.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to copy |
| `target` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the target file |
| `options` | [CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption.html#)!:options specifying how the copy should be done |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains a copy option that is not supported |
| `java.nio.file.FileAlreadyExistsException` | if the target file exists but cannot be replaced because the`REPLACE_EXISTING`option is not specified*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | the`REPLACE_EXISTING`option is specified but the file cannot be replaced because it is a non-empty directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the source file, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))is invoked to check write access to the target file. If a symbolic link is copied the security manager is invoked to check [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#)`("symbolic")`. |

### createDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun createDirectory(
    dir: Path!, 
    vararg attrs: FileAttribute<*>!
): Unit
```

Creates a new directory. This method works in exactly the manner specified by the [Files.createDirectory](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createDirectory(java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))method.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the directory to create |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:an optional list of file attributes to set atomically when creating the directory |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains an attribute that cannot be set atomically when creating the directory |
| `java.nio.file.FileAlreadyExistsException` | if a directory could not otherwise be created because a file of that name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs or the parent directory does not exist |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to the new directory. |

### createLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createLink(
    link: Path!, 
    existing: Path!
): Unit
```

Creates a new link (directory entry) for an existing file. This method works in exactly the manner specified by the [Files.createLink](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createLink(java.nio.file.Path,%20java.nio.file.Path))method.

The default implementation of this method throws`UnsupportedOperationException`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------|
| `link` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the link (directory entry) to create |
| `existing` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:a path to an existing file |

| Exceptions ||
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support adding an existing file to a directory |
| `java.nio.file.FileAlreadyExistsException` | if the entry could not otherwise be created because a file of that name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#)`("hard")`or its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method denies write access to either the link or the existing file. |

### createSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSymbolicLink(
    link: Path!, 
    target: Path!, 
    vararg attrs: FileAttribute<*>!
): Unit
```

Creates a symbolic link to a target. This method works in exactly the manner specified by the [Files.createSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#createSymbolicLink(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.attribute.FileAttribute))method.

The default implementation of this method throws`UnsupportedOperationException`.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `link` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path of the symbolic link to create |
| `target` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the target of the symbolic link |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:the array of attributes to set atomically when creating the symbolic link |

| Exceptions ||
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support symbolic links or the array contains an attribute that cannot be set atomically when creating the symbolic link |
| `java.nio.file.FileAlreadyExistsException` | if a file with the name already exists*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it denies [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission.html#)`("symbolic")`or its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method denies write access to the path of the symbolic link. |

### delete

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun delete(path: Path!): Unit
```

Deletes a file. This method works in exactly the manner specified by the [Files.delete](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#delete(java.nio.file.Path))method.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to delete |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NoSuchFileException` | if the file does not exist*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | if the file is a directory and could not otherwise be deleted because the directory is not empty*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [SecurityManager.checkDelete(String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access to the file |

### deleteIfExists

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteIfExists(path: Path!): Boolean
```

Deletes a file if it exists. This method works in exactly the manner specified by the [Files.deleteIfExists](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#deleteIfExists(java.nio.file.Path))method.

The default implementation of this method simply invokes [delete](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#delete(java.nio.file.Path))ignoring the`NoSuchFileException`when the file does not exist. It may be overridden where appropriate.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to delete |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file was deleted by this method;`false`if the file could not be deleted because it did not exist |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.DirectoryNotEmptyException` | if the file is a directory and could not otherwise be deleted because the directory is not empty*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [SecurityManager.checkDelete(String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access to the file |

### getFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : FileAttributeView!> getFileAttributeView(
    path: Path!, 
    type: Class<V>!, 
    vararg options: LinkOption!
): V
```

Returns a file attribute view of a given type. This method works in exactly the manner specified by the [Files.getFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getFileAttributeView(java.nio.file.Path,%20java.lang.Class,%20java.nio.file.LinkOption))method.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>!:the`Class`object corresponding to the file attribute view |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!:options indicating how symbolic links are handled |

| Return ||
|---|--------------------------------------------------------------------------------------------------|
| V | a file attribute view of the specified type, or`null`if the attribute view type is not available |

### getFileStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFileStore(path: Path!): FileStore!
```

Returns the [FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#) representing the file store where a file is located. This method works in exactly the manner specified by the [Files.getFileStore](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#getFileStore(java.nio.file.Path))method.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------|
| [FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore.html#)! | the file store where the file is stored |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file, and in addition it checks [RuntimePermission](https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#)`("getFileStoreAttributes")` |

### getFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getFileSystem(uri: URI!): FileSystem!
```

Returns an existing`FileSystem`created by this provider.

This method returns a reference to a`FileSystem`that was created by invoking the [newFileSystem(URI,Map)](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap))method. File systems created the [newFileSystem(Path,Map)](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newFileSystem(java.nio.file.Path,%20kotlin.collections.MutableMap))method are not returned by this method. The file system is identified by its`URI`. Its exact form is highly provider dependent. In the case of the default provider the URI's path component is`"/"`and the authority, query and fragment components are undefined (Undefined components are represented by`null`).

Once a file system created by this provider is java.nio.file.FileSystem#close it is provider-dependent if this method returns a reference to the closed file system or throws [FileSystemNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemNotFoundException.html#). If the provider allows a new file system to be created with the same URI as a file system it previously created then this method throws the exception if invoked after the file system is closed (and before a new instance is created by the #newFileSystem method).

If a security manager is installed then a provider implementation may require to check a permission before returning a reference to an existing file system. In the case of the [default](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#getDefault())file system, no permission check is required.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:URI reference |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------|
| [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | The file system |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the pre-conditions for the`uri`parameter aren't met |
| `java.nio.file.FileSystemNotFoundException` | If the file system does not exist |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission. |

### getPath

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPath(uri: URI!): Path!
```

Return a`Path`object by converting the given [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#). The resulting`Path`is associated with a [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#) that already exists or is constructed automatically.

The exact form of the URI is file system provider dependent. In the case of the default provider, the URI scheme is`"file"`and the given URI has a non-empty path component, and undefined query, and fragment components. The resulting`Path`is associated with the default [default](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#getDefault())`FileSystem`.

If a security manager is installed then a provider implementation may require to check a permission. In the case of the [default](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#getDefault())file system, no permission check is required.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:The URI to convert |

| Return ||
|----------------------------------------------------------------------------------|---------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)! | The resulting`Path` |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the URI scheme does not identify this provider or other preconditions on the uri parameter do not hold |
| `java.nio.file.FileSystemNotFoundException` | The file system, identified by the URI, does not exist and cannot be created automatically |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission. |

### getScheme

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getScheme(): String!
```

Returns the URI scheme that identifies this provider.

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The URI scheme |

### installedProviders

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun installedProviders(): MutableList<FileSystemProvider!>!
```

Returns a list of the installed file system providers.

The first invocation of this method causes the default provider to be initialized (if not already initialized) and loads any other installed providers as described by the [FileSystems](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#) class.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FileSystemProvider](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#)!>! | An unmodifiable list of the installed file system providers. The list contains at least one element, that is the default file system provider |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------|
| `java.util.ServiceConfigurationError` | When an error occurs while loading a service provider |

### isHidden

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isHidden(path: Path!): Boolean
```

Tells whether or not a file is considered*hidden* . This method works in exactly the manner specified by the [Files.isHidden](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isHidden(java.nio.file.Path))method.

This method is invoked by the [isHidden](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isHidden(java.nio.file.Path))method.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to test |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file is considered hidden |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file. |

### isSameFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isSameFile(
    path: Path!, 
    path2: Path!
): Boolean
```

Tests if two paths locate the same file. This method works in exactly the manner specified by the [Files.isSameFile](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#isSameFile(java.nio.file.Path,%20java.nio.file.Path))method.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:one path to the file |
| `path2` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the other path |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the two paths locate the same file |

| Exceptions ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to both files. |

### move

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun move(
    source: Path!, 
    target: Path!, 
    vararg options: CopyOption!
): Unit
```

Move or rename a file to a target file. This method works in exactly the manner specified by the [Files.move](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#move(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))method except that both the source and target paths must be associated with this provider.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `source` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to move |
| `target` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the target file |
| `options` | [CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption.html#)!:options specifying how the move should be done |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the array contains a copy option that is not supported |
| `java.nio.file.FileAlreadyExistsException` | if the target file exists but cannot be replaced because the`REPLACE_EXISTING`option is not specified*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | the`REPLACE_EXISTING`option is specified but the file cannot be replaced because it is a non-empty directory*(optional specific exception)* |
| `java.nio.file.AtomicMoveNotSupportedException` | if the options array contains the`ATOMIC_MOVE`option but the file cannot be moved as an atomic file system operation. |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to both the source and target file. |

### newAsynchronousFileChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newAsynchronousFileChannel(
    path: Path!, 
    options: MutableSet<out OpenOption!>!, 
    executor: ExecutorService!, 
    vararg attrs: FileAttribute<*>!
): AsynchronousFileChannel!
```

Opens or creates a file for reading and/or writing, returning an asynchronous file channel to access the file. This method works in exactly the manner specified by the [AsynchronousFileChannel.open](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel.html#open(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.util.concurrent.ExecutorService,%20java.nio.file.attribute.FileAttribute))method. A provider that does not support all the features required to construct an asynchronous file channel throws`UnsupportedOperationException`. The default provider is required to support the creation of asynchronous file channels. When not overridden, the default implementation of this method throws`UnsupportedOperationException`.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!\>!:options specifying how the file is opened |
| `executor` | [ExecutorService](https://developer.android.com/reference/kotlin/java/util/concurrent/ExecutorService.html#)!:the thread pool or`null`to associate the channel with the default thread pool |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:an optional list of file attributes to set atomically when creating the file |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [AsynchronousFileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousFileChannel.html#)! | a new asynchronous file channel |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If this provider that does not support creating asynchronous file channels, or an unsupported open option or file attribute is specified |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default file system, the [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access if the file is opened for writing |

### newByteChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newByteChannel(
    path: Path!, 
    options: MutableSet<out OpenOption!>!, 
    vararg attrs: FileAttribute<*>!
): SeekableByteChannel!
```

Opens or creates a file, returning a seekable byte channel to access the file. This method works in exactly the manner specified by the[java.nio.file.Files#newByteChannel(java.nio.file.Path,java.util.Set,java.nio.file.attribute.FileAttribute[])](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#newByteChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))method.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!\>!:options specifying how the file is opened |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:an optional list of file attributes to set atomically when creating the file |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel.html#)! | a new seekable byte channel |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported open option is specified or the array contains attributes that cannot be set atomically when creating the file |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists and the [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption.html#) option is specified*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the path if the file is opened for reading. The [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to the path if the file is opened for writing. The [checkDelete](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDirectoryStream(
    dir: Path!, 
    filter: DirectoryStream.Filter<in Path!>!
): DirectoryStream<Path!>!
```

Opens a directory, returning a`DirectoryStream`to iterate over the entries in the directory. This method works in exactly the manner specified by the [java.nio.file.Files#newDirectoryStream(java.nio.file.Path,java.nio.file.DirectoryStream.Filter)](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#newDirectoryStream(java.nio.file.Path,%20java.nio.file.DirectoryStream.Filter))method.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the directory |
| `filter` | [DirectoryStream.Filter](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream.Filter.html#)\<in [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!\>!:the directory stream filter |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [DirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream.html#)< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!>! | a new and open`DirectoryStream`object |

| Exceptions ||
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the directory. |

### newFileChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newFileChannel(
    path: Path!, 
    options: MutableSet<out OpenOption!>!, 
    vararg attrs: FileAttribute<*>!
): FileChannel!
```

Opens or creates a file for reading and/or writing, returning a file channel to access the file. This method works in exactly the manner specified by the [FileChannel.open](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#open(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))method. A provider that does not support all the features required to construct a file channel throws`UnsupportedOperationException`. The default provider is required to support the creation of file channels. When not overridden, the default implementation throws`UnsupportedOperationException`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!\>!:options specifying how the file is opened |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute.html#)\<\*\>!:an optional list of file attributes to set atomically when creating the file |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------|
| [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#)! | a new file channel |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | If this provider that does not support creating file channels, or an unsupported open option or file attribute is specified |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default file system, the [java.lang.SecurityManager#checkRead(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access if the file is opened for reading. The [java.lang.SecurityManager#checkWrite(java.lang.String)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access if the file is opened for writing |

### newFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newFileSystem(
    uri: URI!, 
    env: MutableMap<String!, *>!
): FileSystem!
```

Constructs a new`FileSystem`object identified by a URI. This method is invoked by the [FileSystems.newFileSystem(URI,Map)](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems.html#newFileSystem(java.net.URI,%20kotlin.collections.MutableMap))method to open a new file system identified by a URI.

The`uri`parameter is an absolute, hierarchical URI, with a scheme equal (without regard to case) to the scheme supported by this provider. The exact form of the URI is highly provider dependent. The`env`parameter is a map of provider specific properties to configure the file system.

This method throws [FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException.html#) if the file system already exists because it was previously created by an invocation of this method. Once a file system is java.nio.file.FileSystem#close it is provider-dependent if the provider allows a new file system to be created with the same URI as a file system it previously created.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:URI reference |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!:A map of provider specific properties to configure the file system; may be empty |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------|
| [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | A new file system |

| Exceptions ||
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the pre-conditions for the`uri`parameter aren't met, or the`env`parameter does not contain properties required by the provider, or a property value is invalid |
| `java.io.IOException` | An I/O error occurs creating the file system |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission required by the file system provider implementation |
| `java.nio.file.FileSystemAlreadyExistsException` | If the file system has already been created |

### newFileSystem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newFileSystem(
    path: Path!, 
    env: MutableMap<String!, *>!
): FileSystem!
```

Constructs a new`FileSystem`to access the contents of a file as a file system.

This method is intended for specialized providers of pseudo file systems where the contents of one or more files is treated as a file system. The`env`parameter is a map of provider specific properties to configure the file system.

If this provider does not support the creation of such file systems or if the provider does not recognize the file type of the given file then it throws`UnsupportedOperationException`. The default implementation of this method throws`UnsupportedOperationException`.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:The path to the file |
| `env` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,\*\>!:A map of provider specific properties to configure the file system; may be empty |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------|
| [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#)! | A new file system |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If this provider does not support access to the contents as a file system or it does not recognize the file type of the given file |
| `java.lang.IllegalArgumentException` | If the`env`parameter does not contain properties required by the provider, or a property value is invalid |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is installed and it denies an unspecified permission. |

### newInputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newInputStream(
    path: Path!, 
    vararg options: OpenOption!
): InputStream!
```

Opens a file, returning an input stream to read from the file. This method works in exactly the manner specified by the [java.nio.file.Files#newInputStream](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#newInputStream(java.nio.file.Path,%20java.nio.file.OpenOption))method.

The default implementation of this method opens a channel to the file as if by invoking the [newByteChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newByteChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))method and constructs a stream that reads bytes from the channel. This method should be overridden where appropriate.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to open |
| `options` | [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!:options specifying how the file is opened |

| Return ||
|------------------------------------------------------------------------------------------|--------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | a new input stream |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if an invalid combination of options is specified |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file. |

### newOutputStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newOutputStream(
    path: Path!, 
    vararg options: OpenOption!
): OutputStream!
```

Opens or creates a file, returning an output stream that may be used to write bytes to the file. This method works in exactly the manner specified by the [Files.newOutputStream](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#newOutputStream(java.nio.file.Path,%20java.nio.file.OpenOption))method.

The default implementation of this method opens a channel to the file as if by invoking the [newByteChannel](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider#newByteChannel(java.nio.file.Path,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))method and constructs a stream that writes bytes to the channel. This method should be overridden where appropriate.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file to open or create |
| `options` | [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption.html#)!:options specifying how the file is opened |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | a new output stream |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`options`contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported option is specified |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to the file. The [checkDelete](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access if the file is opened with the`DELETE_ON_CLOSE`option. |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <A : BasicFileAttributes!> readAttributes(
    path: Path!, 
    type: Class<A>!, 
    vararg options: LinkOption!
): A
```

Reads a file's attributes as a bulk operation. This method works in exactly the manner specified by the[java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.Class,java.nio.file.LinkOption[])](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#readAttributes(java.nio.file.Path,%20java.lang.Class,%20java.nio.file.LinkOption))method.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `<A>` | The`BasicFileAttributes`type |
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<A\>!:the`Class`of the file attributes required to read |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!:options indicating how symbolic links are handled |

| Return ||
|---|---------------------|
| A | the file attributes |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if an attributes of the given type are not supported |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, a security manager is installed, its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the file |

### readAttributes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAttributes(
    path: Path!, 
    attributes: String!, 
    vararg options: LinkOption!
): MutableMap<String!, Any!>!
```

Reads a set of file attributes as a bulk operation. This method works in exactly the manner specified by the[java.nio.file.Files#readAttributes(java.nio.file.Path,java.lang.String,java.nio.file.LinkOption[])](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#readAttributes(java.nio.file.Path,%20kotlin.String,%20java.nio.file.LinkOption))method.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file |
| `attributes` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attributes to read |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!:options indicating how symbolic links are handled |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | a map of the attributes returned; may be empty. The map's keys are the attribute names, its values are the attribute values |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available |
| `java.lang.IllegalArgumentException` | if no attributes are specified or an unrecognized attributes is specified |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method denies read access to the file. If this method is invoked to read security sensitive attributes then the security manager may be invoke to check for additional permissions. |

### readSymbolicLink

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readSymbolicLink(link: Path!): Path!
```

Reads the target of a symbolic link. This method works in exactly the manner specified by the [Files.readSymbolicLink](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#readSymbolicLink(java.nio.file.Path))method.

The default implementation of this method throws`UnsupportedOperationException`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `link` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the symbolic link |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)! | The target of the symbolic link |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the implementation does not support symbolic links |
| `java.nio.file.NotLinkException` | if the target could otherwise not be read because the file is not a symbolic link*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, it checks that`FilePermission`has been granted with the "`readlink`" action to read the link. |

### setAttribute

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAttribute(
    path: Path!, 
    attribute: String!, 
    value: Any!, 
    vararg options: LinkOption!
): Unit
```

Sets the value of a file attribute. This method works in exactly the manner specified by the [Files.setAttribute](https://developer.android.com/reference/kotlin/java/nio/file/Files.html#setAttribute(java.nio.file.Path,%20kotlin.String,%20kotlin.Any,%20java.nio.file.LinkOption))method.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path.html#)!:the path to the file |
| `attribute` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the attribute to set |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the attribute value |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption.html#)!:options indicating how symbolic links are handled |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the attribute view is not available |
| `java.lang.IllegalArgumentException` | if the attribute name is not specified, or is not recognized, or the attribute value is of the correct type but has an inappropriate value |
| `java.lang.ClassCastException` | If the attribute value is not of the expected type or is a collection containing elements that are not of the expected type |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, its [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method denies write access to the file. If this method is invoked to set security sensitive attributes then the security manager may be invoked to check for additional permissions. |
