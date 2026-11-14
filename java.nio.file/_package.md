# java.nio.file

# java.nio.file

## Interfaces

| [CopyOption](../java/nio/file/CopyOption.md) | An object that configures how to copy or move a file. |
| --- | --- |
| [DirectoryStream](../java/nio/file/DirectoryStream.md) | An object to iterate over the entries in a directory. |
| [FileVisitor](../java/nio/file/FileVisitor.md) | A visitor of files. |
| [OpenOption](../java/nio/file/OpenOption.md) | An object that configures how to open or create a file. |
| --- | --- |
| [Path](../java/nio/file/Path.md) | An object that may be used to locate a file in a file system. |
| [PathMatcher](../java/nio/file/PathMatcher.md) | An interface that is implemented by objects that perform match operations on paths. |
| [SecureDirectoryStream](../java/nio/file/SecureDirectoryStream.md) | A`DirectoryStream`that defines operations on files that are located relative to an open directory. |
| --- | --- |
| [Watchable](../java/nio/file/Watchable.md) | An object that may be registered with a watch service so that it can be*watched*for changes and events. |
| [WatchEvent](../java/nio/file/WatchEvent.md) | An event or a repeated event for an object that is registered with a [WatchService](../java/nio/file/WatchService.md). |
| [WatchKey](../java/nio/file/WatchKey.md) | A token representing the registration of a [watchable](../java/nio/file/Watchable.md) object with a [WatchService](../java/nio/file/WatchService.md). |
| --- | --- |
| [WatchService](../java/nio/file/WatchService.md) | A watch service that*watches*registered objects for changes and events. |

## Classes

| [Files](../java/nio/file/Files.md) | This class consists exclusively of static methods that operate on files, directories, or other types of files. |
| --- | --- |
| [FileStore](../java/nio/file/FileStore.md) | Storage for files. |
| [FileSystem](../java/nio/file/FileSystem.md) | Provides an interface to a file system and is the factory for objects to access files and other objects in the file system. |
| [FileSystems](../java/nio/file/FileSystems.md) | Factory methods for file systems. |
| --- | --- |
| [LinkPermission](../java/nio/file/LinkPermission.md) | The`Permission`class for link creation operations. |
| [Paths](../java/nio/file/Paths.md) | This class consists exclusively of static methods that return a [Path](../java/nio/file/Path.md) by converting a path string or [URI](../java/net/URI.md). |
| [SimpleFileVisitor](../java/nio/file/SimpleFileVisitor.md) | A simple visitor of files with default behavior to visit all files and to re-throw I/O errors. |
| --- | --- |
| [StandardWatchEventKinds](../java/nio/file/StandardWatchEventKinds.md) | Defines the*standard*event kinds. |

## Exceptions

| [AccessDeniedException](../java/nio/file/AccessDeniedException.md) | Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check. |
| --- | --- |
| [AtomicMoveNotSupportedException](../java/nio/file/AtomicMoveNotSupportedException.md) | Checked exception thrown when a file cannot be moved as an atomic file system operation. |
| [ClosedDirectoryStreamException](../java/nio/file/ClosedDirectoryStreamException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed. |
| [ClosedFileSystemException](../java/nio/file/ClosedFileSystemException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed. |
| --- | --- |
| [ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed. |
| [DirectoryIteratorException](../java/nio/file/DirectoryIteratorException.md) | Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory. |
| [DirectoryNotEmptyException](../java/nio/file/DirectoryNotEmptyException.md) | Checked exception thrown when a file system operation fails because a directory is not empty. |
| --- | --- |
| [FileAlreadyExistsException](../java/nio/file/FileAlreadyExistsException.md) | Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists. |
| [FileSystemAlreadyExistsException](../java/nio/file/FileSystemAlreadyExistsException.md) | Runtime exception thrown when an attempt is made to create a file system that already exists. |
| [FileSystemException](../java/nio/file/FileSystemException.md) | Thrown when a file system operation fails on one or two files. |
| --- | --- |
| [FileSystemLoopException](../java/nio/file/FileSystemLoopException.md) | Checked exception thrown when a file system loop, or cycle, is encountered. |
| [FileSystemNotFoundException](../java/nio/file/FileSystemNotFoundException.md) | Runtime exception thrown when a file system cannot be found. |
| [InvalidPathException](../java/nio/file/InvalidPathException.md) | Unchecked exception thrown when path string cannot be converted into a [Path](../java/nio/file/Path.md) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons. |
| --- | --- |
| [NoSuchFileException](../java/nio/file/NoSuchFileException.md) | Checked exception thrown when an attempt is made to access a file that does not exist. |
| [NotDirectoryException](../java/nio/file/NotDirectoryException.md) | Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory. |
| [NotLinkException](../java/nio/file/NotLinkException.md) | Checked exception thrown when a file system operation fails because a file is not a symbolic link. |
| --- | --- |
| [ProviderMismatchException](../java/nio/file/ProviderMismatchException.md) | Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider. |
| [ProviderNotFoundException](../java/nio/file/ProviderNotFoundException.md) | Runtime exception thrown when a provider of the required type cannot be found. |
| [ReadOnlyFileSystemException](../java/nio/file/ReadOnlyFileSystemException.md) | Unchecked exception thrown when an attempt is made to update an object associated with a [read-only](../java/nio/file/FileSystem.md))`FileSystem`. |
| --- | --- |

## Enums

| [AccessMode](../java/nio/file/AccessMode.md) | Defines access modes used to test the accessibility of a file. |
| --- | --- |
| [FileVisitOption](../java/nio/file/FileVisitOption.md) | Defines the file tree traversal options. |
| [FileVisitResult](../java/nio/file/FileVisitResult.md) | The result type of a [FileVisitor](../java/nio/file/FileVisitor.md). |
| [LinkOption](../java/nio/file/LinkOption.md) | Defines the options as to how symbolic links are handled. |
| --- | --- |
| [StandardCopyOption](../java/nio/file/StandardCopyOption.md) | Defines the standard copy options. |
| [StandardOpenOption](../java/nio/file/StandardOpenOption.md) | Defines the standard open options. |
