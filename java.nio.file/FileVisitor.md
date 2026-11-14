# FileVisitor

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileVisitor

```
interface FileVisitor<T : Any!>
```

| [java.nio.file.FileVisitor](FileVisitor.md) |

| Known Direct Subclasses [SimpleFileVisitor](SimpleFileVisitor.md) |-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------| | [SimpleFileVisitor](SimpleFileVisitor.md) | A simple visitor of files with default behavior to visit all files and to re-throw I/O errors. | |
| --- | --- | --- | --- | --- | --- | --- |

A visitor of files. An implementation of this interface is provided to the java.nio.file.Files#walkFileTree methods to visit each file in a file tree.

**Usage Examples:**Suppose we want to delete a file tree. In that case, each directory should be deleted after the entries in the directory are deleted. 

```kotlin
Path start = ...
      Files.walkFileTree(start, new SimpleFileVisitor<Path>() {
          @Override
          public FileVisitResult visitFile(Path file, BasicFileAttributes attrs)
              throws IOException
          {
              Files.delete(file);
              return FileVisitResult.CONTINUE;
          }
          @Override
          public FileVisitResult postVisitDirectory(Path dir, IOException e)
              throws IOException
          {
              if (e == null) {
                  Files.delete(dir);
                  return FileVisitResult.CONTINUE;
              } else {
                  // directory iteration failed
                  throw e;
              }
          }
      });
  
```

Furthermore, suppose we want to copy a file tree to a target location. In that case, symbolic links should be followed and the target directory should be created before the entries in the directory are copied. 

```kotlin
final Path source = ...
      final Path target = ...
 
      Files.walkFileTree(source, EnumSet.of(FileVisitOption.FOLLOW_LINKS), Integer.MAX_VALUE,
          new SimpleFileVisitor<Path>() {
              @Override
              public FileVisitResult preVisitDirectory(Path dir, BasicFileAttributes attrs)
                  throws IOException
              {
                  Path targetdir = target.resolve(source.relativize(dir));
                  try {
                      Files.copy(dir, targetdir);
                  } catch (FileAlreadyExistsException e) {
                       if (!Files.isDirectory(targetdir))
                           throw e;
                  }
                  return CONTINUE;
              }
              @Override
              public FileVisitResult visitFile(Path file, BasicFileAttributes attrs)
                  throws IOException
              {
                  Files.copy(file, target.resolve(source.relativize(file)));
                  return CONTINUE;
              }
          });
  
```

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [FileVisitResult](FileVisitResult.md)! | [postVisitDirectory](FileVisitor.md))`(`dir:` `T`, `exc:` ` [IOException](../java.io/IOException.md)!`)` Invoked for a directory after entries in the directory, and all of their descendants, have been visited. |
| abstract [FileVisitResult](FileVisitResult.md)! | [preVisitDirectory](FileVisitor.md))`(`dir:` `T`, `attrs:` ` [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!`)` Invoked for a directory before entries in the directory are visited. |
| abstract [FileVisitResult](FileVisitResult.md)! | [visitFile](FileVisitor.md))`(`file:` `T`, `attrs:` ` [BasicFileAttributes](../java.nio.file.attribute/BasicFileAttributes.md)!`)` Invoked for a file in a directory. |
| --- | --- |
| abstract [FileVisitResult](FileVisitResult.md)! | [visitFileFailed](FileVisitor.md))`(`file:` `T`, `exc:` ` [IOException](../java.io/IOException.md)!`)` Invoked for a file that could not be visited. |

## Public methods

### postVisitDirectory

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun postVisitDirectory(
    dir: T, 
    exc: IOException!
): FileVisitResult!
```

Invoked for a directory after entries in the directory, and all of their descendants, have been visited. This method is also invoked when iteration of the directory completes prematurely (by a [visitFile](FileVisitor.md))method returning [SKIP_SIBLINGS](FileVisitResult.md), or an I/O error when iterating over the directory).

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
abstract fun preVisitDirectory(
    dir: T, 
    attrs: BasicFileAttributes!
): FileVisitResult!
```

Invoked for a directory before entries in the directory are visited.

If this method returns [CONTINUE](FileVisitResult.md), then entries in the directory are visited. If this method returns [SKIP_SUBTREE](FileVisitResult.md) or [SKIP_SIBLINGS](FileVisitResult.md) then entries in the directory (and any descendants) will not be visited.

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
abstract fun visitFile(
    file: T, 
    attrs: BasicFileAttributes!
): FileVisitResult!
```

Invoked for a file in a directory.

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
abstract fun visitFileFailed(
    file: T, 
    exc: IOException!
): FileVisitResult!
```

Invoked for a file that could not be visited. This method is invoked if the file's attributes could not be read, the file is a directory that could not be opened, and other reasons.

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
