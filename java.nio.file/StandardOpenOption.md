# StandardOpenOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardOpenOption

```
class StandardOpenOption : OpenOption
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.StandardOpenOption](../java/nio/file/StandardOpenOption.md)\> ||
| | ↳ | [java.nio.file.StandardOpenOption](../java/nio/file/StandardOpenOption.md) |

| Known Direct Subclasses [StandardOpenOption.APPEND](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.CREATE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.CREATE_NEW](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.DSYNC](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.READ](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.SPARSE](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.SYNC](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md), [StandardOpenOption.WRITE](../java/nio/file/StandardOpenOption.md) |------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [StandardOpenOption.APPEND](../java/nio/file/StandardOpenOption.md) | If the file is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access then bytes will be written to the end of the file rather than the beginning. | | [StandardOpenOption.CREATE](../java/nio/file/StandardOpenOption.md) | Create a new file if it does not exist. | | [StandardOpenOption.CREATE_NEW](../java/nio/file/StandardOpenOption.md) | Create a new file, failing if the file already exists. | | [StandardOpenOption.DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md) | Delete on close. | | [StandardOpenOption.DSYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content be written synchronously to the underlying storage device. | | [StandardOpenOption.READ](../java/nio/file/StandardOpenOption.md) | Open for read access. | | [StandardOpenOption.SPARSE](../java/nio/file/StandardOpenOption.md) | Sparse file. | | [StandardOpenOption.SYNC](../java/nio/file/StandardOpenOption.md) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. | | [StandardOpenOption.TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md) | If the file already exists and it is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access, then its length is truncated to 0. | | [StandardOpenOption.WRITE](../java/nio/file/StandardOpenOption.md) | Open for write access. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the standard open options.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [APPEND](../java/nio/file/StandardOpenOption.md) If the file is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access then bytes will be written to the end of the file rather than the beginning. |
| [CREATE](../java/nio/file/StandardOpenOption.md) Create a new file if it does not exist. |
| [CREATE_NEW](../java/nio/file/StandardOpenOption.md) Create a new file, failing if the file already exists. |
| [DELETE_ON_CLOSE](../java/nio/file/StandardOpenOption.md) Delete on close. |
| [DSYNC](../java/nio/file/StandardOpenOption.md) Requires that every update to the file's content be written synchronously to the underlying storage device. |
| [READ](../java/nio/file/StandardOpenOption.md) Open for read access. |
| [SPARSE](../java/nio/file/StandardOpenOption.md) Sparse file. |
| [SYNC](../java/nio/file/StandardOpenOption.md) Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. |
| [TRUNCATE_EXISTING](../java/nio/file/StandardOpenOption.md) If the file already exists and it is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access, then its length is truncated to 0. |
| [WRITE](../java/nio/file/StandardOpenOption.md) Open for write access. |

## Enum values

### APPEND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val APPEND : StandardOpenOption
```

If the file is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access then bytes will be written to the end of the file rather than the beginning.

If the file is opened for write access by other programs, then it is file system specific if writing to the end of the file is atomic. 

### CREATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CREATE : StandardOpenOption
```

Create a new file if it does not exist. This option is ignored if the [CREATE_NEW](../java/nio/file/StandardOpenOption.md) option is also set. The check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. 

### CREATE_NEW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CREATE_NEW : StandardOpenOption
```

Create a new file, failing if the file already exists. The check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. 

### DELETE_ON_CLOSE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DELETE_ON_CLOSE : StandardOpenOption
```

Delete on close. When this option is present then the implementation makes a*best effort* attempt to delete the file when closed by the appropriate`close`method. If the`close`method is not invoked then a*best effort* attempt is made to delete the file when the Java virtual machine terminates (either normally, as defined by the Java Language Specification, or where possible, abnormally). This option is primarily intended for use with*work files*that are used solely by a single instance of the Java virtual machine. This option is not recommended for use when opening files that are open concurrently by other entities. Many of the details as to when and how the file is deleted are implementation specific and therefore not specified. In particular, an implementation may be unable to guarantee that it deletes the expected file when replaced by an attacker while the file is open. Consequently, security sensitive applications should take care when using this option.

For security reasons, this option may imply the [java.nio.file.LinkOption#NOFOLLOW_LINKS](../java/nio/file/LinkOption.md) option. In other words, if the option is present when opening an existing file that is a symbolic link then it may fail (by throwing [java.io.IOException](../java/io/IOException.md)). 

### DSYNC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DSYNC : StandardOpenOption
```

Requires that every update to the file's content be written synchronously to the underlying storage device. 
**See Also**

### READ

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val READ : StandardOpenOption
```

Open for read access. 

### SPARSE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SPARSE : StandardOpenOption
```

Sparse file. When used with the [CREATE_NEW](../java/nio/file/StandardOpenOption.md) option then this option provides a*hint*that the new file will be sparse. The option is ignored when the file system does not support the creation of sparse files. 

### SYNC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SYNC : StandardOpenOption
```

Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. 
**See Also**

### TRUNCATE_EXISTING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TRUNCATE_EXISTING : StandardOpenOption
```

If the file already exists and it is opened for [WRITE](../java/nio/file/StandardOpenOption.md) access, then its length is truncated to 0. This option is ignored if the file is opened only for [READ](../java/nio/file/StandardOpenOption.md) access. 

### WRITE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE : StandardOpenOption
```

Open for write access.
