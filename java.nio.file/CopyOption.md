# CopyOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CopyOption

```
interface CopyOption
```

| [java.nio.file.CopyOption](https://developer.android.com/reference/kotlin/java/nio/file/CopyOption#) |

| Known Direct Subclasses [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption), [StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [LinkOption](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) | Defines the options as to how symbolic links are handled. | | [StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption) | Defines the standard copy options. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkOption.NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#ENUM_VALUE:NOFOLLOW_LINKS), [StandardCopyOption.ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:ATOMIC_MOVE), [StandardCopyOption.COPY_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:COPY_ATTRIBUTES), [StandardCopyOption.REPLACE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:REPLACE_EXISTING) |----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------| | [LinkOption.NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption#ENUM_VALUE:NOFOLLOW_LINKS) | Do not follow symbolic links. | | [StandardCopyOption.ATOMIC_MOVE](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:ATOMIC_MOVE) | Move the file as an atomic file system operation. | | [StandardCopyOption.COPY_ATTRIBUTES](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:COPY_ATTRIBUTES) | Copy attributes to the new file. | | [StandardCopyOption.REPLACE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption#ENUM_VALUE:REPLACE_EXISTING) | Replace an existing file if it exists. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that configures how to copy or move a file.

Objects of this type may be used with the [Files.copy(Path,Path,CopyOption...)](https://developer.android.com/reference/kotlin/java/nio/file/Files#copy(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption)), [Files.copy(InputStream,Path,CopyOption...)](https://developer.android.com/reference/kotlin/java/nio/file/Files#copy(java.io.InputStream,%20java.nio.file.Path,%20java.nio.file.CopyOption))and [Files.move(Path,Path,CopyOption...)](https://developer.android.com/reference/kotlin/java/nio/file/Files#move(java.nio.file.Path,%20java.nio.file.Path,%20java.nio.file.CopyOption))methods to configure how a file is copied or moved.

The [StandardCopyOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardCopyOption) enumeration type defines the*standard*options.

## Summary
