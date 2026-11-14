# SecureDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SecureDirectoryStream

```
interface SecureDirectoryStream<T : Any!> : DirectoryStream<T>
```

| [java.nio.file.SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md) |

A`DirectoryStream`that defines operations on files that are located relative to an open directory. A`SecureDirectoryStream`is intended for use by sophisticated or security sensitive applications requiring to traverse file trees or otherwise operate on directories in a race-free manner. Race conditions can arise when a sequence of file operations cannot be carried out in isolation. Each of the file operations defined by this interface specify a relative path. All access to the file is relative to the open directory irrespective of if the directory is moved or replaced by an attacker while the directory is open. A`SecureDirectoryStream`may also be used as a virtual*working directory*.

A`SecureDirectoryStream`requires corresponding support from the underlying operating system. Where an implementation supports this features then the`DirectoryStream`returned by the java.nio.file.Files#newDirectoryStream method will be a`SecureDirectoryStream`and must be cast to that type in order to invoke the methods defined by this interface.

In the case of the default [provider](../java/nio/file/spi/FileSystemProvider.md), and a security manager is set, then the permission checks are performed using the path obtained by resolving the given relative path against the*original path*of the directory (irrespective of if the directory is moved since it was opened).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteDirectory](../java/nio/file/SecureDirectoryStream.md))`(`path:` `T`)` Deletes a directory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteFile](../java/nio/file/SecureDirectoryStream.md))`(`path:` `T`)` Deletes a file. |
| abstractV | [getFileAttributeView](../java/nio/file/SecureDirectoryStream.md))`(`type:` ` [Class](../java/lang/Class.md)<V>!`)` Returns a new file attribute view to access the file attributes of this directory. |
| --- | --- |
| abstractV | [getFileAttributeView](../java/nio/file/SecureDirectoryStream.md))`(`path:` `T`, `type:` ` [Class](../java/lang/Class.md)<V>!`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Returns a new file attribute view to access the file attributes of a file in this directory. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [move](../java/nio/file/SecureDirectoryStream.md))`(`srcpath:` `T`, `targetdir:` ` [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md)<T>!`, `targetpath:` `T`)` Move a file from this directory to another directory. |
| abstract [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | [newByteChannel](../java/nio/file/SecureDirectoryStream.md))`(`path:` `T`, `options:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<out` ` [OpenOption](../java/nio/file/OpenOption.md)!>!`, `vararg` `attrs:` ` [FileAttribute](../java/nio/file/attribute/FileAttribute.md)<*>!`)` Opens or creates a file in this directory, returning a seekable byte channel to access the file. |
| --- | --- |
| abstract [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md)\<T\>! | [newDirectoryStream](../java/nio/file/SecureDirectoryStream.md))`(`path:` `T`, `vararg` `options:` ` [LinkOption](../java/nio/file/LinkOption.md)!`)` Opens the directory identified by the given path, returning a`SecureDirectoryStream`to iterate over the entries in the directory. |

| Inherited functions ||
|---|---|
| From class [Closeable](../java/io/Closeable.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/io/Closeable.md))`()` <br /> Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect. As noted in [AutoCloseable.close()](../java/lang/AutoCloseable.md)), cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally*mark* the`Closeable`as closed, prior to throwing the`IOException`. <br /> | ||
| From class [DirectoryStream](../java/nio/file/DirectoryStream.md) |--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T> | [iterator](../java/nio/file/DirectoryStream.md))`()` <br /> Returns the iterator associated with this`DirectoryStream`. <br /> | ||

## Public methods

### deleteDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deleteDirectory(path: T): Unit
```

Deletes a directory.

Unlike the [delete()](../java/nio/file/Files.md))method, this method does not first examine the file to determine if the file is a directory. Whether non-directories are deleted by this method is system dependent and therefore not specified. When the parameter is a relative path then the directory to delete is relative to this open directory.

| Parameters ||
|--------|---------------------------------------|
| `path` | T:the path of the directory to delete |

| Exceptions ||
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NoSuchFileException` | if the directory does not exist*(optional specific exception)* |
| `java.nio.file.DirectoryNotEmptyException` | if the directory could not otherwise be deleted because it is not empty*(optional specific exception)* |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access to the directory |

### deleteFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun deleteFile(path: T): Unit
```

Deletes a file.

Unlike the [delete()](../java/nio/file/Files.md))method, this method does not first examine the file to determine if the file is a directory. Whether a directory is deleted by this method is system dependent and therefore not specified. If the file is a symbolic link, then the link itself, not the final target of the link, is deleted. When the parameter is a relative path then the file to delete is relative to this open directory.

| Parameters ||
|--------|----------------------------------|
| `path` | T:the path of the file to delete |

| Exceptions ||
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NoSuchFileException` | if the file does not exist*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkDelete](../java/lang/SecurityManager.md))method is invoked to check delete access to the file |

### getFileAttributeView

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <V : FileAttributeView!> getFileAttributeView(type: Class<V>!): V
```

Returns a new file attribute view to access the file attributes of this directory.

The resulting file attribute view can be used to read or update the attributes of this (open) directory. The`type`parameter specifies the type of the attribute view and the method returns an instance of that type if supported. Invoking this method to obtain a [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) always returns an instance of that class that is bound to this open directory.

The state of resulting file attribute view is intimately connected to this directory stream. Once the directory stream is [closed](../java/io/Closeable.md)), then all methods to read or update attributes will throw [ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `type` | [Class](../java/lang/Class.md)\<V\>!:the`Class`object corresponding to the file attribute view |

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

The resulting file attribute view can be used to read or update the attributes of file in this directory. The`type`parameter specifies the type of the attribute view and the method returns an instance of that type if supported. Invoking this method to obtain a [BasicFileAttributeView](../java/nio/file/attribute/BasicFileAttributeView.md) always returns an instance of that class that is bound to the file in the directory.

The state of resulting file attribute view is intimately connected to this directory stream. Once the directory stream [closed](../java/io/Closeable.md)), then all methods to read or update attributes will throw [ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md). The file is not required to exist at the time that the file attribute view is created but methods to read or update attributes of the file will fail when invoked and the file does not exist.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `<V>` | The`FileAttributeView`type |
| `path` | T:the path of the file |
| `type` | [Class](../java/lang/Class.md)\<V\>!:the`Class`object corresponding to the file attribute view |
| --- | --- |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

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

This method works in a similar manner to [move](../java/nio/file/Files.md))method when the [ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md) option is specified. That is, this method moves a file as an atomic file system operation. If the`srcpath`parameter is an [absolute](../java/nio/file/Path.md))path then it locates the source file. If the parameter is a relative path then it is located relative to this open directory. If the`targetpath`parameter is absolute then it locates the target file (the`targetdir`parameter is ignored). If the parameter is a relative path it is located relative to the open directory identified by the`targetdir`parameter. In all cases, if the target file exists then it is implementation specific if it is replaced or this method fails.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `srcpath` | T:the name of the file to move |
| `targetdir` | [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md)\<T\>!:the destination directory |
| `targetpath` | T:the name to give the file in the destination directory |
| --- | --- |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if this or the target directory stream is closed |
| `java.nio.file.FileAlreadyExistsException` | if the file already exists in the target directory and cannot be replaced*(optional specific exception)* |
| `java.nio.file.AtomicMoveNotSupportedException` | if the file cannot be moved as an atomic file system operation |
| --- | --- |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to both the source and target file. |

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

This method works in exactly the manner specified by the java.nio.file.Files#newByteChannel method for the case that the`path`parameter is an [absolute](../java/nio/file/Path.md))path. When the parameter is a relative path then the file to open or create is relative to this open directory. In addition to the options defined by the`Files.newByteChannel`method, the [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) option may be used to ensure that this method fails if the file is a symbolic link.

The channel, once created, is not dependent upon the directory stream used to create it. Closing this directory stream has no effect upon the channel.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | T:the path of the file to open or create |
| `options` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<out [OpenOption](../java/nio/file/OpenOption.md)!\>!:options specifying how the file is opened |
| `attrs` | [FileAttribute](../java/nio/file/attribute/FileAttribute.md)\<\*\>!:an optional list of attributes to set atomically when creating the file |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------|
| [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md)! | the seekable byte channel |

| Exceptions ||
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.lang.IllegalArgumentException` | if the set contains an invalid combination of options |
| `java.lang.UnsupportedOperationException` | if an unsupported open option is specified or the array contains attributes that cannot be set atomically when creating the file |
| --- | --- |
| `java.nio.file.FileAlreadyExistsException` | if a file of that name already exists and the [CREATE_NEW](../java/nio/file/StandardOpenOption.md) option is specified*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the path if the file is opened for reading. The [checkWrite](../java/lang/SecurityManager.md))method is invoked to check write access to the path if the file is opened for writing. |
| --- | --- |

### newDirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newDirectoryStream(
    path: T, 
    vararg options: LinkOption!
): SecureDirectoryStream<T>!
```

Opens the directory identified by the given path, returning a`SecureDirectoryStream`to iterate over the entries in the directory.

This method works in exactly the manner specified by the [newDirectoryStream](../java/nio/file/Files.md))method for the case that the`path`parameter is an [absolute](../java/nio/file/Path.md))path. When the parameter is a relative path then the directory to open is relative to this open directory. The [NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) option may be used to ensure that this method fails if the file is a symbolic link.

The new directory stream, once created, is not dependent upon the directory stream used to create it. Closing this directory stream has no effect upon newly created directory stream.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | T:the path to the directory to open |
| `options` | [LinkOption](../java/nio/file/LinkOption.md)!:options indicating how symbolic links are handled |

| Return ||
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md)<T>! | a new and open`SecureDirectoryStream`object |

| Exceptions ||
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.file.ClosedDirectoryStreamException` | if the directory stream is closed |
| `java.nio.file.NotDirectoryException` | if the file could not otherwise be opened because it is not a directory*(optional specific exception)* |
| `java.io.IOException` | if an I/O error occurs |
| --- | --- |
| `java.lang.SecurityException` | In the case of the default provider, and a security manager is installed, the [checkRead](../java/lang/SecurityManager.md))method is invoked to check read access to the directory. |
