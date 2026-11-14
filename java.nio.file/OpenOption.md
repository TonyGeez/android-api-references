# OpenOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OpenOption

```
interface OpenOption
```

| [java.nio.file.OpenOption](../java/nio/file/OpenOption.md) |

| Known Direct Subclasses [LinkOption](../java/nio/file/LinkOption.md), [StandardOpenOption](../java/nio/file/StandardOpenOption.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [LinkOption](../java/nio/file/LinkOption.md) | Defines the options as to how symbolic links are handled. | | [StandardOpenOption](../java/nio/file/StandardOpenOption.md) | Defines the standard open options. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkOption.NOFOLLOW_LINKS](../java/nio/file/LinkOption.md), [StandardOpenOption.APPEND](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.CREATE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.CREATE_NEW](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.DSYNC](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.READ](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.SPARSE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.SYNC](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.WRITE](../java/nio/file/StandardOpenOption.md) |------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LinkOption.NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) | Do not follow symbolic links. | | [StandardOpenOption.APPEND](../java/nio/file/StandardOpenOption.md) | If the file is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access then bytes will be written to the end of the file rather than the beginning. | | [StandardOpenOption.CREATE](../java/nio/file/StandardOpenOption.md) | Create a new file if it does not exist. | | [StandardOpenOption.CREATE_NEW](../java/nio/file/StandardOpenOption.md) | Create a new file, failing if the file already exists. | | [StandardOpenOption.DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md) | Delete on close. | | [StandardOpenOption.DSYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content be written synchronously to the underlying storage device. | | [StandardOpenOption.READ](../java/nio/file/StandardOpenOption.md) | Open for read access. | | [StandardOpenOption.SPARSE](../java/nio/file/StandardOpenOption.md) | Sparse file. | | [StandardOpenOption.SYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. | | [StandardOpenOption.TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md) | If the file already exists and it is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access, then its length is truncated to 0. | | [StandardOpenOption.WRITE](../java/nio/file/StandardOpenOption.md) | Open for write access. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An object that configures how to open or create a file.

Objects of this type are used by methods such as [newOutputStream](../java/nio/file/Files.md)), java.nio.file.Files#newByteChannel, java.nio.channels.FileChannel#open, and java.nio.channels.AsynchronousFileChannel#open when opening or creating a file.

The [StandardOpenOption](../java/nio/file/StandardOpenOption.md) enumeration type defines the*standard*options.

## Summary
