# OpenOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OpenOption

```
interface OpenOption
```

| [java.nio.file.OpenOption](OpenOption.md) |

| Known Direct Subclasses [LinkOption](LinkOption.md), [StandardOpenOption](StandardOpenOption.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [LinkOption](LinkOption.md) | Defines the options as to how symbolic links are handled. | | [StandardOpenOption](StandardOpenOption.md) | Defines the standard open options. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkOption.NOFOLLOW_LINKS](LinkOption.md), [StandardOpenOption.APPEND](StandardOpenOption.md), [StandardOpenOption.CREATE](StandardOpenOption.md), [StandardOpenOption.CREATE_NEW](StandardOpenOption.md), [StandardOpenOption.DELETE_ON_CLOSE](StandardOpenOption.md), [StandardOpenOption.DSYNC](StandardOpenOption.md), [StandardOpenOption.READ](StandardOpenOption.md), [StandardOpenOption.SPARSE](StandardOpenOption.md), [StandardOpenOption.SYNC](StandardOpenOption.md), [StandardOpenOption.TRUNCATE_EXISTING](StandardOpenOption.md), [StandardOpenOption.WRITE](StandardOpenOption.md) |------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LinkOption.NOFOLLOW_LINKS](LinkOption.md) | Do not follow symbolic links. | | [StandardOpenOption.APPEND](StandardOpenOption.md) | If the file is opened for [WRITE](StandardOpenOption.md) access then bytes will be written to the end of the file rather than the beginning. | | [StandardOpenOption.CREATE](StandardOpenOption.md) | Create a new file if it does not exist. | | [StandardOpenOption.CREATE_NEW](StandardOpenOption.md) | Create a new file, failing if the file already exists. | | [StandardOpenOption.DELETE_ON_CLOSE](StandardOpenOption.md) | Delete on close. | | [StandardOpenOption.DSYNC](StandardOpenOption.md) | Requires that every update to the file's content be written synchronously to the underlying storage device. | | [StandardOpenOption.READ](StandardOpenOption.md) | Open for read access. | | [StandardOpenOption.SPARSE](StandardOpenOption.md) | Sparse file. | | [StandardOpenOption.SYNC](StandardOpenOption.md) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. | | [StandardOpenOption.TRUNCATE_EXISTING](StandardOpenOption.md) | If the file already exists and it is opened for [WRITE](StandardOpenOption.md) access, then its length is truncated to 0. | | [StandardOpenOption.WRITE](StandardOpenOption.md) | Open for write access. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that configures how to open or create a file.

Objects of this type are used by methods such as [newOutputStream](Files.md)), java.nio.file.Files#newByteChannel, java.nio.channels.FileChannel#open, and java.nio.channels.AsynchronousFileChannel#open when opening or creating a file.

The [StandardOpenOption](StandardOpenOption.md) enumeration type defines the*standard*options.

## Summary
