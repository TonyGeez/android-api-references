# FileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileSystemException

```
open class FileSystemException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.nio.file.FileSystemException](FileSystemException.md) |

| Known Direct Subclasses [AccessDeniedException](AccessDeniedException.md), [AtomicMoveNotSupportedException](AtomicMoveNotSupportedException.md), [DirectoryNotEmptyException](DirectoryNotEmptyException.md), [FileAlreadyExistsException](FileAlreadyExistsException.md), [FileSystemLoopException](FileSystemLoopException.md), [NoSuchFileException](NoSuchFileException.md), [NotDirectoryException](NotDirectoryException.md), [NotLinkException](NotLinkException.md) |---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------| | [AccessDeniedException](AccessDeniedException.md) | Checked exception thrown when a file system operation is denied, typically due to a file permission or other access check. | | [AtomicMoveNotSupportedException](AtomicMoveNotSupportedException.md) | Checked exception thrown when a file cannot be moved as an atomic file system operation. | | [DirectoryNotEmptyException](DirectoryNotEmptyException.md) | Checked exception thrown when a file system operation fails because a directory is not empty. | | [FileAlreadyExistsException](FileAlreadyExistsException.md) | Checked exception thrown when an attempt is made to create a file or directory and a file of that name already exists. | | [FileSystemLoopException](FileSystemLoopException.md) | Checked exception thrown when a file system loop, or cycle, is encountered. | | [NoSuchFileException](NoSuchFileException.md) | Checked exception thrown when an attempt is made to access a file that does not exist. | | [NotDirectoryException](NotDirectoryException.md) | Checked exception thrown when a file system operation, intended for a directory, fails because the file is not a directory. | | [NotLinkException](NotLinkException.md) | Checked exception thrown when a file system operation fails because a file is not a symbolic link. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown when a file system operation fails on one or two files. This class is the general class for file system exceptions.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileSystemException](FileSystemException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |
| [FileSystemException](FileSystemException.md))`(`file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `other:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFile](FileSystemException.md))`()` Returns the file used to create this exception. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getOtherFile](FileSystemException.md))`()` Returns the other file used to create this exception. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getReason](FileSystemException.md))`()` Returns the string explaining why the file system operation failed. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](FileSystemException.md) Returns the detail message string. |

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
| --- | --- |

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
