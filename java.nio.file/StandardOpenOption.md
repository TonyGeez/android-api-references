# StandardOpenOption

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardOpenOption

```
class StandardOpenOption : OpenOption
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.nio.file.StandardOpenOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#)\> ||
| | ↳ | [java.nio.file.StandardOpenOption](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) |

| Known Direct Subclasses [StandardOpenOption.APPEND](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:APPEND), [StandardOpenOption.CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE), [StandardOpenOption.CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE_NEW), [StandardOpenOption.DELETE_ON_CLOSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DELETE_ON_CLOSE), [StandardOpenOption.DSYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DSYNC), [StandardOpenOption.READ](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:READ), [StandardOpenOption.SPARSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SPARSE), [StandardOpenOption.SYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SYNC), [StandardOpenOption.TRUNCATE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:TRUNCATE_EXISTING), [StandardOpenOption.WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:WRITE) |------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [StandardOpenOption.APPEND](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:APPEND) | If the file is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access then bytes will be written to the end of the file rather than the beginning. | | [StandardOpenOption.CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE) | Create a new file if it does not exist. | | [StandardOpenOption.CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE_NEW) | Create a new file, failing if the file already exists. | | [StandardOpenOption.DELETE_ON_CLOSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DELETE_ON_CLOSE) | Delete on close. | | [StandardOpenOption.DSYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DSYNC) | Requires that every update to the file's content be written synchronously to the underlying storage device. | | [StandardOpenOption.READ](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:READ) | Open for read access. | | [StandardOpenOption.SPARSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SPARSE) | Sparse file. | | [StandardOpenOption.SYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SYNC) | Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. | | [StandardOpenOption.TRUNCATE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:TRUNCATE_EXISTING) | If the file already exists and it is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access, then its length is truncated to 0. | | [StandardOpenOption.WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:WRITE) | Open for write access. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Defines the standard open options.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [APPEND](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:APPEND) If the file is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access then bytes will be written to the end of the file rather than the beginning. |
| [CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE) Create a new file if it does not exist. |
| [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:CREATE_NEW) Create a new file, failing if the file already exists. |
| [DELETE_ON_CLOSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DELETE_ON_CLOSE) Delete on close. |
| [DSYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:DSYNC) Requires that every update to the file's content be written synchronously to the underlying storage device. |
| [READ](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:READ) Open for read access. |
| [SPARSE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SPARSE) Sparse file. |
| [SYNC](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:SYNC) Requires that every update to the file's content or metadata be written synchronously to the underlying storage device. |
| [TRUNCATE_EXISTING](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:TRUNCATE_EXISTING) If the file already exists and it is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access, then its length is truncated to 0. |
| [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#ENUM_VALUE:WRITE) Open for write access. |

## Enum values

### APPEND

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val APPEND : StandardOpenOption
```

If the file is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access then bytes will be written to the end of the file rather than the beginning.

If the file is opened for write access by other programs, then it is file system specific if writing to the end of the file is atomic. 

### CREATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CREATE : StandardOpenOption
```

Create a new file if it does not exist. This option is ignored if the [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) option is also set. The check for the existence of the file and the creation of the file if it does not exist is atomic with respect to other file system operations. 

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

For security reasons, this option may imply the [java.nio.file.LinkOption#NOFOLLOW_LINKS](https://developer.android.com/reference/kotlin/java/nio/file/LinkOption) option. In other words, if the option is present when opening an existing file that is a symbolic link then it may fail (by throwing [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)). 

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

Sparse file. When used with the [CREATE_NEW](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) option then this option provides a*hint*that the new file will be sparse. The option is ignored when the file system does not support the creation of sparse files. 

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

If the file already exists and it is opened for [WRITE](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access, then its length is truncated to 0. This option is ignored if the file is opened only for [READ](https://developer.android.com/reference/kotlin/java/nio/file/StandardOpenOption#) access. 

### WRITE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val WRITE : StandardOpenOption
```

Open for write access.
