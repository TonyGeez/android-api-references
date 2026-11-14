# FilenameFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FilenameFilter

```
@FunctionalInterface interface FilenameFilter
```

| [java.io.FilenameFilter](https://developer.android.com/reference/kotlin/java/io/FilenameFilter#) |

Instances of classes that implement this interface are used to filter filenames. These instances are used to filter directory listings in the`list`method of class`File`, and by the Abstract Window Toolkit's file dialog component.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [accept](https://developer.android.com/reference/kotlin/java/io/FilenameFilter#accept(java.io.File,%20kotlin.String))`(`dir:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Tests if a specified file should be included in a file list. |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(
    dir: File!, 
    name: String!
): Boolean
```

Tests if a specified file should be included in a file list.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `dir` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:the directory in which the file was found. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the file. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the name should be included in the file list;`false`otherwise. |
