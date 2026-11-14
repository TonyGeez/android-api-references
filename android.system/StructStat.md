# StructStat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructStat

Kotlin| [Java](StructStat.md) 
| --- | --- |

```
class StructStat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.system.StructStat](StructStat.md) |

File information returned by [Os.fstat](Os.md)), [Os.lstat](Os.md)), and [Os.stat](Os.md)). Corresponds to C's`struct stat`from`<stat.h>`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructStat](StructStat.md))`(`st_dev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ino:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_nlink:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_gid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_rdev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_atim:` ` [StructTimespec](StructTimespec.md)!`, `st_mtim:` ` [StructTimespec](StructTimespec.md)!`, `st_ctim:` ` [StructTimespec](StructTimespec.md)!`, `st_blksize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blocks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs an instance with the given field values. |
| [StructStat](StructStat.md))`(`st_dev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ino:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_nlink:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_gid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_rdev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_atime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mtime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ctime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blksize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blocks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs an instance with the given field values. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](StructStat.md))`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StructTimespec](StructTimespec.md)! | [st_atim](StructStat.md) StructTimespec with time of last access. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_atime](StructStat.md) Seconds part of time of last access. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_blksize](StructStat.md) A file system-specific preferred I/O block size for this object. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_blocks](StructStat.md) Number of blocks allocated for this object. |
| [StructTimespec](StructTimespec.md)! | [st_ctim](StructStat.md) StructTimespec with time of last status change. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_ctime](StructStat.md) Seconds part of time of last status change |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_dev](StructStat.md) Device ID of device containing file. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_gid](StructStat.md) Group ID of file. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_ino](StructStat.md) File serial number (inode). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_mode](StructStat.md) Mode (permissions) of file. |
| [StructTimespec](StructTimespec.md)! | [st_mtim](StructStat.md) StructTimespec with time of last modification. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_mtime](StructStat.md) Seconds part of time of last data modification. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_nlink](StructStat.md) Number of hard links to the file. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_rdev](StructStat.md) Device ID (if file is character or block special). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_size](StructStat.md) For regular files, the file size in bytes. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_uid](StructStat.md) User ID of file. |

## Public constructors

### StructStat

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructStat(
    st_dev: Long, 
    st_ino: Long, 
    st_mode: Int, 
    st_nlink: Long, 
    st_uid: Int, 
    st_gid: Int, 
    st_rdev: Long, 
    st_size: Long, 
    st_atim: StructTimespec!, 
    st_mtim: StructTimespec!, 
    st_ctim: StructTimespec!, 
    st_blksize: Long, 
    st_blocks: Long)
```

Constructs an instance with the given field values. 

### StructStat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StructStat(
    st_dev: Long, 
    st_ino: Long, 
    st_mode: Int, 
    st_nlink: Long, 
    st_uid: Int, 
    st_gid: Int, 
    st_rdev: Long, 
    st_size: Long, 
    st_atime: Long, 
    st_mtime: Long, 
    st_ctime: Long, 
    st_blksize: Long, 
    st_blocks: Long)
```

Constructs an instance with the given field values.

## Public methods

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### st_atim

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_atim: StructTimespec!
```

StructTimespec with time of last access. 

### st_atime

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_atime: Long
```

Seconds part of time of last access. 

### st_blksize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_blksize: Long
```

A file system-specific preferred I/O block size for this object. For some file system types, this may vary from file to file. 

### st_blocks

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_blocks: Long
```

Number of blocks allocated for this object. 

### st_ctim

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_ctim: StructTimespec!
```

StructTimespec with time of last status change. 

### st_ctime

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_ctime: Long
```

Seconds part of time of last status change 

### st_dev

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_dev: Long
```

Device ID of device containing file. 

### st_gid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_gid: Int
```

Group ID of file. 

### st_ino

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_ino: Long
```

File serial number (inode). 

### st_mode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_mode: Int
```

Mode (permissions) of file. 

### st_mtim

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_mtim: StructTimespec!
```

StructTimespec with time of last modification. 

### st_mtime

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_mtime: Long
```

Seconds part of time of last data modification. 

### st_nlink

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_nlink: Long
```

Number of hard links to the file. 

### st_rdev

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_rdev: Long
```

Device ID (if file is character or block special). 

### st_size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_size: Long
```

For regular files, the file size in bytes. For symbolic links, the length in bytes of the pathname contained in the symbolic link. For a shared memory object, the length in bytes. For a typed memory object, the length in bytes. For other file types, the use of this field is unspecified. 

### st_uid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val st_uid: Int
```

User ID of file.
