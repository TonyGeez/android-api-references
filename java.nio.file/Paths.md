# Paths

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Paths

```
class Paths
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.Paths](https://developer.android.com/reference/kotlin/java/nio/file/Paths#) |

This class consists exclusively of static methods that return a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) by converting a path string or [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)! | [get](https://developer.android.com/reference/kotlin/java/nio/file/Paths#get(kotlin.String,%20kotlin.String))`(`first:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `more:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Converts a path string, or a sequence of strings that when joined form a path string, to a`Path`. |
| static [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)! | [get](https://developer.android.com/reference/kotlin/java/nio/file/Paths#get(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!`)` Converts the given URI to a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) object. |

## Public methods

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(
    first: String!, 
    vararg more: String!
): Path!
```

Converts a path string, or a sequence of strings that when joined form a path string, to a`Path`.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `first` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path string or initial part of the path string |
| `more` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:additional strings to be joined to form the path string |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)! | the resulting`Path` |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.nio.file.InvalidPathException` | if the path string cannot be converted to a`Path` |

**See Also**

- [java.nio.file.FileSystem#getPath](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#getPath(kotlin.String,%20kotlin.String))
- [java.nio.file.Path#of(String,String...)](https://developer.android.com/reference/kotlin/java/nio/file/Path#of(kotlin.String,%20kotlin.String)) 

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun get(uri: URI!): Path!
```

Converts the given URI to a [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) object.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI.html#)!:the URI to convert |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)! | the resulting`Path` |

| Exceptions ||
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if preconditions on the`uri`parameter do not hold. The format of the URI is provider specific. |
| `java.nio.file.FileSystemNotFoundException` | The file system, identified by the URI, does not exist and cannot be created automatically, or the provider identified by the URI's scheme component is not installed |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission to access the file system |
| --- | --- |

**See Also**

- [java.nio.file.Path#of(URI)](https://developer.android.com/reference/kotlin/java/nio/file/Path#of(java.net.URI))
