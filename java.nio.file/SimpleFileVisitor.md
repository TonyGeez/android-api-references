# SimpleFileVisitor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SimpleFileVisitor

```
open class SimpleFileVisitor<T : Any!> : FileVisitor<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.SimpleFileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#) |

A simple visitor of files with default behavior to visit all files and to re-throw I/O errors.

Methods in this class may be overridden subject to their general contract.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SimpleFileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#SimpleFileVisitor())`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | [postVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#postVisitDirectory(java.nio.file.SimpleFileVisitor.T,%20java.io.IOException))`(`dir:` `T`, `exc:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!`)` Invoked for a directory after entries in the directory, and all of their descendants, have been visited. |
| open [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | [preVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#preVisitDirectory(java.nio.file.SimpleFileVisitor.T,%20java.nio.file.attribute.BasicFileAttributes))`(`dir:` `T`, `attrs:` ` [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)!`)` Invoked for a directory before entries in the directory are visited. |
| open [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | [visitFile](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#visitFile(java.nio.file.SimpleFileVisitor.T,%20java.nio.file.attribute.BasicFileAttributes))`(`file:` `T`, `attrs:` ` [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)!`)` Invoked for a file in a directory. |
| --- | --- |
| open [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | [visitFileFailed](https://developer.android.com/reference/kotlin/java/nio/file/SimpleFileVisitor#visitFileFailed(java.nio.file.SimpleFileVisitor.T,%20java.io.IOException))`(`file:` `T`, `exc:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!`)` Invoked for a file that could not be visited. |

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

Unless overridden, this method returns [CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult) if the directory iteration completes without an I/O exception; otherwise this method re-throws the I/O exception that caused the iteration of the directory to terminate prematurely.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | T:a reference to the directory |
| `exc` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!:`null`if the iteration of the directory completes without an error; otherwise the I/O exception that caused the iteration of the directory to complete prematurely |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | the visit result |

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

Unless overridden, this method returns [CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `dir` | T:a reference to the directory |
| `attrs` | [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)!:the directory's basic attributes |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | the visit result |

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

Unless overridden, this method returns [CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | T:a reference to the file |
| `attrs` | [BasicFileAttributes](https://developer.android.com/reference/kotlin/java/nio/file/attribute/BasicFileAttributes)!:the file's basic attributes |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | the visit result |

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
| `exc` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!:the I/O exception that prevented the file from being visited |

| Return ||
|--------------------------------------------------------------------------------------------------|------------------|
| [FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult)! | the visit result |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | if an I/O error occurs |
