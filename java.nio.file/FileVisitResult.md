# FileVisitResult

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileVisitResult

```
class FileVisitResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#)\> ||
| | ↳ | [java.nio.file.FileVisitResult](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#) |

| Known Direct Subclasses [FileVisitResult.CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:CONTINUE), [FileVisitResult.SKIP_SIBLINGS](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SIBLINGS), [FileVisitResult.SKIP_SUBTREE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SUBTREE), [FileVisitResult.TERMINATE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:TERMINATE) |----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------| | [FileVisitResult.CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:CONTINUE) | Continue. | | [FileVisitResult.SKIP_SIBLINGS](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SIBLINGS) | Continue without visiting the*siblings*of this file or directory. | | [FileVisitResult.SKIP_SUBTREE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SUBTREE) | Continue without visiting the entries in this directory. | | [FileVisitResult.TERMINATE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:TERMINATE) | Terminate. | |

The result type of a [FileVisitor](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor).

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:CONTINUE) Continue. |
| [SKIP_SIBLINGS](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SIBLINGS) Continue without visiting the*siblings*of this file or directory. |
| [SKIP_SUBTREE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:SKIP_SUBTREE) Continue without visiting the entries in this directory. |
| [TERMINATE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#ENUM_VALUE:TERMINATE) Terminate. |

## Enum values

### CONTINUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CONTINUE : FileVisitResult
```

Continue. When returned from a [preVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor#preVisitDirectory(java.nio.file.FileVisitor.T,%20java.nio.file.attribute.BasicFileAttributes))method then the entries in the directory should also be visited. 

### SKIP_SIBLINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SKIP_SIBLINGS : FileVisitResult
```

Continue without visiting the*siblings* of this file or directory. If returned from the [preVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor#preVisitDirectory(java.nio.file.FileVisitor.T,%20java.nio.file.attribute.BasicFileAttributes))method then the entries in the directory are also skipped and the [postVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor#postVisitDirectory(java.nio.file.FileVisitor.T,%20java.io.IOException))method is not invoked. 

### SKIP_SUBTREE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SKIP_SUBTREE : FileVisitResult
```

Continue without visiting the entries in this directory. This result is only meaningful when returned from the [preVisitDirectory](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitor#preVisitDirectory(java.nio.file.FileVisitor.T,%20java.nio.file.attribute.BasicFileAttributes))method; otherwise this result type is the same as returning [CONTINUE](https://developer.android.com/reference/kotlin/java/nio/file/FileVisitResult#). 

### TERMINATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TERMINATE : FileVisitResult
```

Terminate.
