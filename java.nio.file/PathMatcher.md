# PathMatcher

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathMatcher

```
@FunctionalInterface interface PathMatcher
```

| [java.nio.file.PathMatcher](../java/nio/file/PathMatcher.md) |

An interface that is implemented by objects that perform match operations on paths.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](../java/nio/file/PathMatcher.md))`(`path:` ` [Path](../java/nio/file/Path.md)!`)` Tells if given path matches this matcher's pattern. |

## Public methods

### matches

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun matches(path: Path!): Boolean
```

Tells if given path matches this matcher's pattern.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------|
| `path` | [Path](../java/nio/file/Path.md)!:the path to match |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, the path matches this matcher's pattern |
