# SecureDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureDirectoryStream

```
interface SecureDirectoryStream<T : Any!> : DirectoryStream<T>
```

| [java.nio.file.SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#) |

A`DirectoryStream`that defines operations on files that are located relative to an open directory. A`SecureDirectoryStream`is intended for use by sophisticated or security sensitive applications requiring to traverse file trees or otherwise operate on directories in a race-free manner. Race conditions can arise when a sequence of file operations cannot be carried out in isolation. Each of the file operations defined by this interface specify a relative path. All access to the file is relative to the open directory irrespective of if the directory is moved or replaced by an attacker while the directory is open. A`SecureDirectoryStream`may also be used as a virtual*working directory*.

A`SecureDirectoryStream`requires corresponding support from the underlying operating system. Where an implementation supports this features then the`DirectoryStream`returned by the java.nio.file.Files#newDirectoryStream method will be a`SecureDirectoryStream`and must be cast to that type in order to invoke the methods defined by this interface.

In the case of the default [provider](https://developer.android.com/reference/kotlin/java/nio/file/spi/FileSystemProvider), and a security manager is set, then the permission checks are performed using the path obtained by resolving the given relative path against the*original path*of the directory (irrespective of if the directory is moved since it was opened).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteDirectory](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#deleteDirectory(java.nio.file.SecureDirectoryStream.T))`(`path:` `T`)` Deletes a directory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteFile](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#deleteFile(java.nio.file.SecureDirectoryStream.T))`(`path:` `T`)` Deletes a file. |
| abstractV | [getFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#getFileAttributeView(java.lang.Class))`(`type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`)` Returns a new file attribute view to access the file attributes of this directory. |
| abstractV | [getFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#getFileAttributeView(java.nio.file.SecureDirectoryStream.T,%20java.lang.Class,%20java.nio.file.LinkOption))`(`path:` `T`, `type:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!`)` Returns a new file attribute view to access the file attributes of a file in this directory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [move](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#move(java.nio.file.SecureDirectoryStream.T,%20java.nio.file.SecureDirectoryStream,%20java.nio.file.SecureDirectoryStream.T))`(`srcpath:` `T`, `targetdir:` ` [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#)<T>!`, `targetpath:` `T`)` Move a file from this directory to another directory. |
| abstract [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel.html#)! | [newByteChannel](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#newByteChannel(java.nio.file.SecureDirectoryStream.T,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))`(`path:` `T`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption)!>!`, `vararg` `attrs:` ` [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute)<*>!`)` Opens or creates a file in this directory, returning a seekable byte channel to access the file. |
| abstract [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#)\<T\>! | [newDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#newDirectoryStream(java.nio.file.SecureDirectoryStream.T,%20java.nio.file.LinkOption))`(`path:` `T`, `vararg` `options:` ` [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!`)` Opens the directory identified by the given path, returning a`SecureDirectoryStream`to iterate over the entries in the directory. |

| Inherited functions ||
|---|---|
| From class [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable.html#) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close())`()` <br /> Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect. As noted in [AutoCloseable.close()](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close()), cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally*mark* the`Closeable`as closed, prior to throwing the`IOException`. <br /> | ||
| From class [DirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T> | [iterator](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream#iterator())`()` <br /> Returns the iterator associated with this`DirectoryStream`. <br /> | ||

## Public methods

### deleteDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deleteDirectory(path: T): Unit
```

Deletes a directory.

Unlike the [delete()](https://developer.android.com/reference/kotlin/java/nio/file/Files#delete(java.nio.file.Path))method, this method does not first examine the file to determine if the file is a directory. Whether non-directories are deleted by this method is system dependent and therefore not specified. When the parameter is a relative path then the directory to delete is relative to this open directory.

| Parameters ||
|--------|---------------------------------------|
| `path` | T:the path of the directory to delete |

| Exceptions ||
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NoSuchFileException` | if the directory does not exist*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | if the directory could not otherwise be deleted because it is not empty*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkDelete](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access to the directory |

### deleteFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deleteFile(path: T): Unit
```

Deletes a file.

Unlike the [delete()](https://developer.android.com/reference/kotlin/java/nio/file/Files#delete(java.nio.file.Path))method, this method does not first examine the file to determine if the file is a directory. Whether a directory is deleted by this method is system dependent and therefore not specified. If the file is a symbolic link, then the link itself, not the final target of the link, is deleted. When the parameter is a relative path then the file to delete is relative to this open directory.

| Parameters ||
|--------|----------------------------------|
| `path` | T:the path of the file to delete |

| Exceptions ||
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NoSuchFileException` | if the file does not exist*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkDelete](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkDelete(kotlin.String))method is invoked to check delete access to the file |

### getFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : FileAttributeView!> getFileAttributeView(type: Class<V>!): V
```

Returns a new file attribute view to access the file attributes of this directory.

The resulting file attribute view can be used to read or update the attributes of this (open) directory. The`type`parameter specifies the type of the attribute view and the method returns an instance of that type if supported. Invoking this method to obtain a [BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView) always returns an instance of that class that is bound to this open directory.

The state of resulting file attribute view is intimately connected to this directory stream. Once the directory stream is [closed](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close()), then all methods to read or update attributes will throw [ClosedDirectoryStreamException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedDirectoryStreamException).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>!:the`Class`object corresponding to the file attribute view |

| Return ||
|---|-------------------------------------------------------------------------------------------------------------------------------------|
| V | a new file attribute view of the specified type bound to this directory stream, or`null`if the attribute view type is not available |

### getFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : FileAttributeView!> getFileAttributeView(
    path: T, 
    type: Class<V>!, 
    vararg options: LinkOption!
): V
```

Returns a new file attribute view to access the file attributes of a file in this directory.

The resulting file attribute view can be used to read or update the attributes of file in this directory. The`type`parameter specifies the type of the attribute view and the method returns an instance of that type if supported. Invoking this method to obtain a [BasicFileAttributeView](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributeView) always returns an instance of that class that is bound to the file in the directory.

The state of resulting file attribute view is intimately connected to this directory stream. Once the directory stream [closed](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close()), then all methods to read or update attributes will throw [ClosedDirectoryStreamException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedDirectoryStreamException). The file is not required to exist at the time that the file attribute view is created but methods to read or update attributes of the file will fail when invoked and the file does not exist.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `path` | T:the path of the file |
| `type` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<V\>!:the`Class`object corresponding to the file attribute view |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!:options indicating how symbolic links are handled |

| Return ||
|---|---------------------------------------------------------------------------------------------------------------------------------------|
| V | a new file attribute view of the specified type bound to a this directory stream, or`null`if the attribute view type is not available |

### move

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun move(
    srcpath: T, 
    targetdir: SecureDirectoryStream<T>!, 
    targetpath: T
): Unit
```

Move a file from this directory to another directory.

This method works in a similar manner to [move](https://developer.android.com/reference/kotlin/java/nio/file/Files#move(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))method when the [ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption) option is specified. That is, this method moves a file as an atomic file system operation. If the`srcpath`parameter is an [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path then it locates the source file. If the parameter is a relative path then it is located relative to this open directory. If the`targetpath`parameter is absolute then it locates the target file (the`targetdir`parameter is ignored). If the parameter is a relative path it is located relative to the open directory identified by the`targetdir`parameter. In all cases, if the target file exists then it is implementation specific if it is replaced or this method fails.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `srcpath` | T:the name of the file to move |
| `targetdir` | [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#)\<T\>!:the destination directory |
| `targetpath` | T:the name to give the file in the destination directory |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if this or the target directory stream is closed |
| `java.nio.file.FileAlreadyExistsException` | if the file already exists in the target directory and cannot be replaced*(optional specific exception)* |
| `java.nio.file.AtomicMoveNotSupportedException` | if the file cannot be moved as an atomic file system operation |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to both the source and target file. |

### newByteChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newByteChannel(
    path: T, 
    options: MutableSet<out OpenOption!>!, 
    vararg attrs: FileAttribute<*>!
): SeekableByteChannel!
```

Opens or creates a file in this directory, returning a seekable byte channel to access the file.

This method works in exactly the manner specified by the java.nio.file.Files#newByteChannel method for the case that the`path`parameter is an [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path. When the parameter is a relative path then the file to open or create is relative to this open directory. In addition to the options defined by the`Files.newByteChannel`method, the [NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) option may be used to ensure that this method fails if the file is a symbolic link.

The channel, once created, is not dependent upon the directory stream used to create it. Closing this directory stream has no effect upon the channel.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | T:the path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption)!\>!:options specifying how the file is opened |
| `attrs` | [FileAttribute](https://developer.android.com/reference/kotlin/java/nio/file/attribute/FileAttribute)\<\*\>!:an optional list of attributes to set atomically when creating the file |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------|
| [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel.html#)! | the seekable byte channel |

| Exceptions ||
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.lang.IllegalArgumentException` | if the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported open option is specified or the array contains attributes that cannot be set atomically when creating the file |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists and the [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption) option is specified*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the path if the file is opened for reading. The [checkWrite](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkWrite(kotlin.String))method is invoked to check write access to the path if the file is opened for writing. |

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDirectoryStream(
    path: T, 
    vararg options: LinkOption!
): SecureDirectoryStream<T>!
```

Opens the directory identified by the given path, returning a`SecureDirectoryStream`to iterate over the entries in the directory.

This method works in exactly the manner specified by the [newDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/Files#newDirectoryStream(java.nio.file.Path))method for the case that the`path`parameter is an [absolute](https://developer.android.com/reference/kotlin/java/nio/file/Path#isAbsolute())path. When the parameter is a relative path then the directory to open is relative to this open directory. The [NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) option may be used to ensure that this method fails if the file is a symbolic link.

The new directory stream, once created, is not dependent upon the directory stream used to create it. Closing this directory stream has no effect upon newly created directory stream.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | T:the path to the directory to open |
| `options` | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption)!:options indicating how symbolic links are handled |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#)<T>! | a new and open`SecureDirectoryStream`object |

| Exceptions ||
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkRead(kotlin.String))method is invoked to check read access to the directory. |
