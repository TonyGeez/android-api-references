# FileVisitResult

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileVisitResult

```
class FileVisitResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.FileVisitResult](FileVisitResult.md)\> ||
| | ↳ | [java.nio.file.FileVisitResult](FileVisitResult.md) |

| Known Direct Subclasses [FileVisitResult.CONTINUE](FileVisitResult.md), [FileVisitResult.SKIP_SIBLINGS](FileVisitResult.md), [FileVisitResult.SKIP_SUBTREE](FileVisitResult.md), [FileVisitResult.TERMINATE](FileVisitResult.md) |----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------| | [FileVisitResult.CONTINUE](FileVisitResult.md) | Continue. | | [FileVisitResult.SKIP_SIBLINGS](FileVisitResult.md) | Continue without visiting the*siblings*of this file or directory. | | [FileVisitResult.SKIP_SUBTREE](FileVisitResult.md) | Continue without visiting the entries in this directory. | | [FileVisitResult.TERMINATE](FileVisitResult.md) | Terminate. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The result type of a [FileVisitor](FileVisitor.md).

## Summary

| Enum values ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CONTINUE](FileVisitResult.md) Continue. |
| [SKIP_SIBLINGS](FileVisitResult.md) Continue without visiting the*siblings*of this file or directory. |
| [SKIP_SUBTREE](FileVisitResult.md) Continue without visiting the entries in this directory. |
| [TERMINATE](FileVisitResult.md) Terminate. |

## Enum values

### CONTINUE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CONTINUE : FileVisitResult
```

Continue. When returned from a [preVisitDirectory](FileVisitor.md))method then the entries in the directory should also be visited. 

### SKIP_SIBLINGS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SKIP_SIBLINGS : FileVisitResult
```

Continue without visiting the*siblings* of this file or directory. If returned from the [preVisitDirectory](FileVisitor.md))method then the entries in the directory are also skipped and the [postVisitDirectory](FileVisitor.md))method is not invoked. 

### SKIP_SUBTREE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SKIP_SUBTREE : FileVisitResult
```

Continue without visiting the entries in this directory. This result is only meaningful when returned from the [preVisitDirectory](FileVisitor.md))method; otherwise this result type is the same as returning [CONTINUE](FileVisitResult.md). 

### TERMINATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TERMINATE : FileVisitResult
```

Terminate.
