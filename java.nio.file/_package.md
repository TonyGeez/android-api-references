# java.nio.file

# java.nio.file

## Interfaces

| [CopyOption](CopyOption.md) | An object that configures how to copy or move a file. |
| --- | --- |
| [DirectoryStream](DirectoryStream.md) | An object to iterate over the entries in a directory. |
| [FileVisitor](FileVisitor.md) | A visitor of files. |
| [OpenOption](OpenOption.md) | An object that configures how to open or create a file. |
| --- | --- |
| [Path](Path.md) | An object that may be used to locate a file in a file system. |
| [PathMatcher](PathMatcher.md) | An interface that is implemented by objects that perform match operations on paths. |
| [SecureDirectoryStream](SecureDirectoryStream.md) | A`DirectoryStream`that defines operations on files that are located relative to an open directory. |
| --- | --- |
| [Watchable](Watchable.md) | An object that may be registered with a watch service so that it can be*watched*for changes and events. |
| [WatchEvent](WatchEvent.md) | An event or a repeated event for an object that is registered with a [WatchService](WatchService.md). |
| [WatchKey](WatchKey.md) | A token representing the registration of a [watchable](Watchable.md) object with a [WatchService](WatchService.md). |
| --- | --- |
| [WatchService](WatchService.md) | A watch service that*watches*registered objects for changes and events. |

## Classes

| [Files](Files.md) | This class consists exclusively of static methods that operate on files, directories, or other types of files. |
| --- | --- |
| [FileStore](FileStore.md) | Storage for files. |
| [FileSystem](FileSystem.md) | Provides an interface to a file system and is the factory for objects to access files and other objects in the file system. |
| [FileSystems](FileSystems.md) | Factory methods for file systems. |
| --- | --- |
| [LinkPermission](LinkPermission.md) | The`Permission`class for link creation operations. |
| [Paths](Paths.md) | This class consists exclusively of static methods that return a [Path](Path.md) by converting a path string or [URI](../java.net/URI.md). |
| [SimpleFileVisitor](SimpleFileVisitor.md) | A simple visitor of files with default behavior to visit all files and to re-throw I/O errors. |
| --- | --- |
| [StandardWatchEventKinds](StandardWatchEventKinds.md) | Defines the*standard*event kinds. |

## Exceptions

| [AccessDeniedException](AccessDeniedException.md) | Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check. |
| --- | --- |
| [AtomicMoveNotSupportedException](AtomicMoveNotSupportedException.md) | Checked exception thrown when a file cannot be moved as an atomic file system operation. |
| [ClosedDirectoryStreamException](ClosedDirectoryStreamException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed. |
| [ClosedFileSystemException](ClosedFileSystemException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed. |
| --- | --- |
| [ClosedWatchServiceException](ClosedWatchServiceException.md) | Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed. |
| [DirectoryIteratorException](DirectoryIteratorException.md) | Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory. |
| [DirectoryNotEmptyException](DirectoryNotEmptyException.md) | Checked exception thrown when a file system operation fails because a directory is not empty. |
| --- | --- |
| [FileAlreadyExistsException](FileAlreadyExistsException.md) | Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists. |
| [FileSystemAlreadyExistsException](FileSystemAlreadyExistsException.md) | Runtime exception thrown when an attempt is made to create a file system that already exists. |
| [FileSystemException](FileSystemException.md) | Thrown when a file system operation fails on one or two files. |
| --- | --- |
| [FileSystemLoopException](FileSystemLoopException.md) | Checked exception thrown when a file system loop, or cycle, is encountered. |
| [FileSystemNotFoundException](FileSystemNotFoundException.md) | Runtime exception thrown when a file system cannot be found. |
| [InvalidPathException](InvalidPathException.md) | Unchecked exception thrown when path string cannot be converted into a [Path](Path.md) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons. |
| --- | --- |
| [NoSuchFileException](NoSuchFileException.md) | Checked exception thrown when an attempt is made to access a file that does not exist. |
| [NotDirectoryException](NotDirectoryException.md) | Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory. |
| [NotLinkException](NotLinkException.md) | Checked exception thrown when a file system operation fails because a file is not a symbolic link. |
| --- | --- |
| [ProviderMismatchException](ProviderMismatchException.md) | Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider. |
| [ProviderNotFoundException](ProviderNotFoundException.md) | Runtime exception thrown when a provider of the required type cannot be found. |
| [ReadOnlyFileSystemException](ReadOnlyFileSystemException.md) | Unchecked exception thrown when an attempt is made to update an object associated with a [read-only](FileSystem.md))`FileSystem`. |
| --- | --- |

## Enums

| [AccessMode](AccessMode.md) | Defines access modes used to test the accessibility of a file. |
| --- | --- |
| [FileVisitOption](FileVisitOption.md) | Defines the file tree traversal options. |
| [FileVisitResult](FileVisitResult.md) | The result type of a [FileVisitor](FileVisitor.md). |
| [LinkOption](LinkOption.md) | Defines the options as to how symbolic links are handled. |
| --- | --- |
| [StandardCopyOption](StandardCopyOption.md) | Defines the standard copy options. |
| [StandardOpenOption](StandardOpenOption.md) | Defines the standard open options. |
