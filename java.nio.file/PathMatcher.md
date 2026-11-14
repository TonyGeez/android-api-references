# PathMatcher

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMatcher

```
@FunctionalInterface interface PathMatcher
```

| [java.nio.file.PathMatcher](https://developer.android.com/reference/kotlin/java/nio/file/PathMatcher#) |

An interface that is implemented by objects that perform match operations on paths.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/java/nio/file/PathMatcher#matches(java.nio.file.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!`)` Tells if given path matches this matcher's pattern. |

## Public methods

### matches

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun matches(path: Path!): Boolean
```

Tells if given path matches this matcher's pattern.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!:the path to match |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the path matches this matcher's pattern |
