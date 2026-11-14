# FileFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileFilter

```
@FunctionalInterface interface FileFilter
```

| [java.io.FileFilter](FileFilter.md) |

A filter for abstract pathnames.

Instances of this interface may be passed to the [listFiles(FileFilter)](File.md))method of the [java.io.File](File.md) class.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [accept](FileFilter.md))`(`pathname:` ` [File](File.md)!`)` Tests whether or not the specified abstract pathname should be included in a pathname list. |

## Public methods

### accept

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(pathname: File!): Boolean
```

Tests whether or not the specified abstract pathname should be included in a pathname list.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------|
| `pathname` | [File](File.md)!:The abstract pathname to be tested |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if`pathname`should be included |
