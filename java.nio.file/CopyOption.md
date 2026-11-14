# CopyOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CopyOption

```
interface CopyOption
```

| [java.nio.file.CopyOption](CopyOption.md) |

| Known Direct Subclasses [LinkOption](LinkOption.md), [StandardCopyOption](StandardCopyOption.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [LinkOption](LinkOption.md) | Defines the options as to how symbolic links are handled. | | [StandardCopyOption](StandardCopyOption.md) | Defines the standard copy options. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkOption.NOFOLLOW_LINKS](LinkOption.md), [StandardCopyOption.ATOMIC_MOVE](StandardCopyOption.md), [StandardCopyOption.COPY_ATTRIBUTES](StandardCopyOption.md), [StandardCopyOption.REPLACE_EXISTING](StandardCopyOption.md) |----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------| | [LinkOption.NOFOLLOW_LINKS](LinkOption.md) | Do not follow symbolic links. | | [StandardCopyOption.ATOMIC_MOVE](StandardCopyOption.md) | Move the file as an atomic file system operation. | | [StandardCopyOption.COPY_ATTRIBUTES](StandardCopyOption.md) | Copy attributes to the new file. | | [StandardCopyOption.REPLACE_EXISTING](StandardCopyOption.md) | Replace an existing file if it exists. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that configures how to copy or move a file.

Objects of this type may be used with the [Files.copy(Path,Path,CopyOption...)](Files.md)), [Files.copy(InputStream,Path,CopyOption...)](Files.md))and [Files.move(Path,Path,CopyOption...)](Files.md))methods to configure how a file is copied or moved.

The [StandardCopyOption](StandardCopyOption.md) enumeration type defines the*standard*options.

## Summary
