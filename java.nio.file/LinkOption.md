# LinkOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkOption

```
class LinkOption : CopyOption, OpenOption
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#)\> ||
| | ↳ | [java.nio.file.LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#) |

| Known Direct Subclasses [LinkOption.NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#ENUM_VALUE:NOFOLLOW_LINKS) |--------------------------------------------------------------------------------------------------------------------------------|-------------------------------| | [LinkOption.NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#ENUM_VALUE:NOFOLLOW_LINKS) | Do not follow symbolic links. | |

Defines the options as to how symbolic links are handled.

## Summary

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#ENUM_VALUE:NOFOLLOW_LINKS) Do not follow symbolic links. |

## Enum values

### NOFOLLOW_LINKS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val NOFOLLOW_LINKS : LinkOption
```

Do not follow symbolic links. 
**See Also**

- [java.nio.file.Files#getFileAttributeView(Path,Class,LinkOption[])](https://developer.android.com/reference/kotlin/java/nio/file/Files#getFileAttributeView(java.nio.file.Path,%20java.lang.Class,%20java.nio.file.LinkOption))
- [java.nio.file.SecureDirectoryStream#newByteChannel](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream#newByteChannel(java.nio.file.SecureDirectoryStream.T,%20kotlin.collections.MutableSet,%20java.nio.file.attribute.FileAttribute))
