# FileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemException

```
open class FileSystemException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [java.nio.file.FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#) |

| Known Direct Subclasses [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException), [AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException), [DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException), [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException), [FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException), [NoSuchFileException](https://developer.android.com/reference/kotlin/java/nio/file/NoSuchFileException), [NotDirectoryException](https://developer.android.com/reference/kotlin/java/nio/file/NotDirectoryException), [NotLinkException](https://developer.android.com/reference/kotlin/java/nio/file/NotLinkException) |---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------| | [AccessDeniedException](https://developer.android.com/reference/kotlin/java/nio/file/AccessDeniedException) | Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check. | | [AtomicMoveNotSupportedException](https://developer.android.com/reference/kotlin/java/nio/file/AtomicMoveNotSupportedException) | Checked exception thrown when a file cannot be moved as an atomic file system operation. | | [DirectoryNotEmptyException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryNotEmptyException) | Checked exception thrown when a file system operation fails because a directory is not empty. | | [FileAlreadyExistsException](https://developer.android.com/reference/kotlin/java/nio/file/FileAlreadyExistsException) | Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists. | | [FileSystemLoopException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemLoopException) | Checked exception thrown when a file system loop, or cycle, is encountered. | | [NoSuchFileException](https://developer.android.com/reference/kotlin/java/nio/file/NoSuchFileException) | Checked exception thrown when an attempt is made to access a file that does not exist. | | [NotDirectoryException](https://developer.android.com/reference/kotlin/java/nio/file/NotDirectoryException) | Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory. | | [NotLinkException](https://developer.android.com/reference/kotlin/java/nio/file/NotLinkException) | Checked exception thrown when a file system operation fails because a file is not a symbolic link. | |

Thrown when a file system operation fails on one or two files. This class is the general class for file system exceptions.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#FileSystemException(kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |
| [FileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#FileSystemException(kotlin.String,%20kotlin.String,%20kotlin.String))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getFile())`()` Returns the file used to create this exception. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getOtherFile())`()` Returns the other file used to create this exception. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#getReason())`()` Returns the string explaining why the file system operation failed. |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/java/nio/file/FileSystemException#message:kotlin.String) Returns the detail message string. |

## Public constructors

### FileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemException(file: String!)
```

Constructs an instance of this class. This constructor should be used when an operation involving one file fails and there isn't any additional information to explain the reason.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known. |

### FileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileSystemException(
    file: String!, 
    other: String!, 
    reason: String!)
```

Constructs an instance of this class. This constructor should be used when an operation involving two files fails, or there is additional information to explain the reason.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the file or`null`if not known. |
| `other` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a string identifying the other file or`null`if there isn't another file or if not known |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a reason message with additional information or`null` |

## Public methods

### getFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFile(): String!
```

Returns the file used to create this exception.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the file (can be`null`) |

### getOtherFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOtherFile(): String!
```

Returns the other file used to create this exception.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the other file (can be`null`) |

### getReason

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReason(): String!
```

Returns the string explaining why the file system operation failed.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the string explaining why the file system operation failed |

## Properties

### message

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val message: String?
```

Returns the detail message string.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
