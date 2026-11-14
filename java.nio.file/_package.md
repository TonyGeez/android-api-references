# java.nio.file

# java.nio.file

## Interfaces

| [CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption) | An object that configures how to copy or move a file. |
| [DirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream) | An object to iterate over the entries in a directory. |
| [FileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor) | A visitor of files. |
| [OpenOption](https://developer.android.com/reference/kotlin/java/nio/file/OpenOption) | An object that configures how to open or create a file. |
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) | An object that may be used to locate a file in a file system. |
| [PathMatcher](https://developer.android.com/reference/kotlin/java/nio/file/PathMatcher) | An interface that is implemented by objects that perform match operations on paths. |
| [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream) | A`DirectoryStream`that defines operations on files that are located relative to an open directory. |
| [Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable) | An object that may be registered with a watch service so that it can be*watched*for changes and events. |
| [WatchEvent](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent) | An event or a repeated event for an object that is registered with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService). |
| [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey) | A token representing the registration of a [watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable) object with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService). |
| [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService) | A watch service that*watches*registered objects for changes and events. |

## Classes

| [Files](https://developer.android.com/reference/kotlin/java/nio/file/Files) | This class consists exclusively of static methods that operate on files, directories, or other types of files. |
| [FileStore](https://developer.android.com/reference/kotlin/java/nio/file/FileStore) | Storage for files. |
| [FileSystem](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem) | Provides an interface to a file system and is the factory for objects to access files and other objects in the file system. |
| [FileSystems](https://developer.android.com/reference/kotlin/java/nio/file/FileSystems) | Factory methods for file systems. |
| [LinkPermission](https://developer.android.com/reference/kotlin/java/nio/file/LinkPermission) | The`Permission`class for link creation operations. |
| [Paths](https://developer.android.com/reference/kotlin/java/nio/file/Paths) | This class consists exclusively of static methods that return a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) by converting a path string or [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#). |
| [SimpleFileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor) | A simple visitor of files with default behavior to visit all files and to re-throw I/O errors. |
| [StandardWatchEventKinds](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds) | Defines the*standard*event kinds. |

## Exceptions

| [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException) | Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check. |
| [AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException) | Checked exception thrown when a file cannot be moved as an atomic file system operation. |
| [ClosedDirectoryStreamException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedDirectoryStreamException) | Unchecked exception thrown when an attempt is made to invoke an operation on a directory stream that is closed. |
| [ClosedFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedFileSystemException) | Unchecked exception thrown when an attempt is made to invoke an operation on a file and the file system is closed. |
| [ClosedWatchServiceException](https://developer.android.com/reference/kotlin/java/nio/file/ClosedWatchServiceException) | Unchecked exception thrown when an attempt is made to invoke an operation on a watch service that is closed. |
| [DirectoryIteratorException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException) | Runtime exception thrown if an I/O error is encountered when iterating over the entries in a directory. |
| [DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException) | Checked exception thrown when a file system operation fails because a directory is not empty. |
| [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException) | Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists. |
| [FileSystemAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemAlreadyExistsException) | Runtime exception thrown when an attempt is made to create a file system that already exists. |
| [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException) | Thrown when a file system operation fails on one or two files. |
| [FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException) | Checked exception thrown when a file system loop, or cycle, is encountered. |
| [FileSystemNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemNotFoundException) | Runtime exception thrown when a file system cannot be found. |
| [InvalidPathException](https://developer.android.com/reference/kotlin/java/nio/file/InvalidPathException) | Unchecked exception thrown when path string cannot be converted into a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) because the path string contains invalid characters, or the path string is invalid for other file system specific reasons. |
| [NoSuchFileException](https://developer.android.com/reference/kotlin/java/nio/file/NoSuchFileException) | Checked exception thrown when an attempt is made to access a file that does not exist. |
| [NotDirectoryException](https://developer.android.com/reference/kotlin/java/nio/file/NotDirectoryException) | Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory. |
| [NotLinkException](https://developer.android.com/reference/kotlin/java/nio/file/NotLinkException) | Checked exception thrown when a file system operation fails because a file is not a symbolic link. |
| [ProviderMismatchException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderMismatchException) | Unchecked exception thrown when an attempt is made to invoke a method on an object created by one file system provider with a parameter created by a different file system provider. |
| [ProviderNotFoundException](https://developer.android.com/reference/kotlin/java/nio/file/ProviderNotFoundException) | Runtime exception thrown when a provider of the required type cannot be found. |
| [ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException) | Unchecked exception thrown when an attempt is made to update an object associated with a [read-only](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#isReadOnly())`FileSystem`. |

## Enums

| [AccessMode](https://developer.android.com/reference/kotlin/java/nio/file/AccessMode) | Defines access modes used to test the accessibility of a file. |
| [FileVisitOption](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitOption) | Defines the file tree traversal options. |
| [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult) | The result type of a [FileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor). |
| [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) | Defines the options as to how symbolic links are handled. |
| [StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption) | Defines the standard copy options. |
| [StandardOpenOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption) | Defines the standard open options. |
