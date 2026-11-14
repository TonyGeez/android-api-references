# SimpleFileVisitor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleFileVisitor

```
open class SimpleFileVisitor<T : Any!> : FileVisitor<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.SimpleFileVisitor](SimpleFileVisitor.md) |

A simple visitor of files with default behavior to visit all files and to re-throw I/O errors.

Methods in this class may be overridden subject to their general contract.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleFileVisitor](SimpleFileVisitor.md))`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [FileVisitResult](FileVisitResult.md)! | [postVisitDirectory](SimpleFileVisitor.md))`(`dir:` `T`, `exc:` ` [IOException](../java.io/IOException.md)!`)` Invoked for a directory after entries in the directory, and all of their descendants, have been visited. |
| open [FileVisitResult](FileVisitResult.md)! | [preVisitDirectory](SimpleFileVisitor.md))`(`dir:` `T`, `attrs:` ` [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!`)` Invoked for a directory before entries in the directory are visited. |
| open [FileVisitResult](FileVisitResult.md)! | [visitFile](SimpleFileVisitor.md))`(`file:` `T`, `attrs:` ` [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!`)` Invoked for a file in a directory. |
| --- | --- |
| open [FileVisitResult](FileVisitResult.md)! | [visitFileFailed](SimpleFileVisitor.md))`(`file:` `T`, `exc:` ` [IOException](../java.io/IOException.md)!`)` Invoked for a file that could not be visited. |

## Protected constructors

### SimpleFileVisitor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SimpleFileVisitor()
```

Initializes a new instance of this class.

## Public methods

### postVisitDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postVisitDirectory(
    dir: T, 
    exc: IOException!
): FileVisitResult!
```

Invoked for a directory after entries in the directory, and all of their descendants, have been visited.

Unless overridden, this method returns [CONTINUE](FileVisitResult.md) if the directory iteration completes without an I/O exception; otherwise this method re-throws the I/O exception that caused the iteration of the directory to terminate prematurely.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | T:a reference to the directory |
| `exc` | [IOException](../java.io/IOException.md)!:`null`if the iteration of the directory completes without an error; otherwise the I/O exception that caused the iteration of the directory to complete prematurely |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](FileVisitResult.md)! | the visit result |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### preVisitDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun preVisitDirectory(
    dir: T, 
    attrs: BasicFileAttributes!
): FileVisitResult!
```

Invoked for a directory before entries in the directory are visited.

Unless overridden, this method returns [CONTINUE](FileVisitResult.md).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | T:a reference to the directory |
| `attrs` | [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!:the directory's basic attributes |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](FileVisitResult.md)! | the visit result |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### visitFile

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun visitFile(
    file: T, 
    attrs: BasicFileAttributes!
): FileVisitResult!
```

Invoked for a file in a directory.

Unless overridden, this method returns [CONTINUE](FileVisitResult.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | T:a reference to the file |
| `attrs` | [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!:the file's basic attributes |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](FileVisitResult.md)! | the visit result |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |

### visitFileFailed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun visitFileFailed(
    file: T, 
    exc: IOException!
): FileVisitResult!
```

Invoked for a file that could not be visited.

Unless overridden, this method re-throws the I/O exception that prevented the file from being visited.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | T:a reference to the file |
| `exc` | [IOException](../java.io/IOException.md)!:the I/O exception that prevented the file from being visited |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](FileVisitResult.md)! | the visit result |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |
