# FileFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileFilter

```
@FunctionalInterface interface FileFilter
```

| [java.io.FileFilter](https://developer.android.com/reference/kotlin/java/io/FileFilter#) |

A filter for abstract pathnames.

Instances of this interface may be passed to the [listFiles(FileFilter)](https://developer.android.com/reference/kotlin/java/io/File#listFiles(java.io.FileFilter))method of the [java.io.File](https://developer.android.com/reference/kotlin/java/io/File) class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [accept](https://developer.android.com/reference/kotlin/java/io/FileFilter#accept(java.io.File))`(`pathname:` ` [File](https://developer.android.com/reference/kotlin/java/io/File)!`)` Tests whether or not the specified abstract pathname should be included in a pathname list. |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(pathname: File!): Boolean
```

Tests whether or not the specified abstract pathname should be included in a pathname list.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `pathname` | [File](https://developer.android.com/reference/kotlin/java/io/File)!:The abstract pathname to be tested |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if`pathname`should be included |
