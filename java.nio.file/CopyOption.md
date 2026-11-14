# CopyOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CopyOption

```
interface CopyOption
```

| [java.nio.file.CopyOption](../java/nio/file/CopyOption.md) |

| Known Direct Subclasses [LinkOption](../java/nio/file/LinkOption.md), [StandardCopyOption](../java/nio/file/StandardCopyOption.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [LinkOption](../java/nio/file/LinkOption.md) | Defines the options as to how symbolic links are handled. | | [StandardCopyOption](../java/nio/file/StandardCopyOption.md) | Defines the standard copy options. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkOption.NOFOLLOW_LINKS](../java/nio/file/LinkOption.md), [StandardCopyOption.ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md), [StandardCopyOption.COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md), [StandardCopyOption.REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) |----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------| | [LinkOption.NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) | Do not follow symbolic links. | | [StandardCopyOption.ATOMIC_MOVE](../java/nio/file/StandardCopyOption.md) | Move the file as an atomic file system operation. | | [StandardCopyOption.COPY_ATTRIBUTES](../java/nio/file/StandardCopyOption.md) | Copy attributes to the new file. | | [StandardCopyOption.REPLACE_EXISTING](../java/nio/file/StandardCopyOption.md) | Replace an existing file if it exists. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that configures how to copy or move a file.

Objects of this type may be used with the [Files.copy(Path,Path,CopyOption...)](../java/nio/file/Files.md)), [Files.copy(InputStream,Path,CopyOption...)](../java/nio/file/Files.md))and [Files.move(Path,Path,CopyOption...)](../java/nio/file/Files.md))methods to configure how a file is copied or moved.

The [StandardCopyOption](../java/nio/file/StandardCopyOption.md) enumeration type defines the*standard*options.

## Summary
