# StructStat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StructStat

Kotlin| [Java](https://developer.android.com/reference/android/system/StructStat "View this page in Java") 

```
class StructStat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.system.StructStat](https://developer.android.com/reference/kotlin/android/system/StructStat#) |

File information returned by [Os.fstat](https://developer.android.com/reference/kotlin/android/system/Os#fstat(java.io.FileDescriptor)), [Os.lstat](https://developer.android.com/reference/kotlin/android/system/Os#lstat(kotlin.String)), and [Os.stat](https://developer.android.com/reference/kotlin/android/system/Os#stat(kotlin.String)). Corresponds to C's`struct stat`from`<stat.h>`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StructStat](https://developer.android.com/reference/kotlin/android/system/StructStat#StructStat(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20kotlin.Long,%20android.system.StructTimespec,%20android.system.StructTimespec,%20android.system.StructTimespec,%20kotlin.Long,%20kotlin.Long))`(`st_dev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ino:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_nlink:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_gid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_rdev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_atim:` ` [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)!`, `st_mtim:` ` [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)!`, `st_ctim:` ` [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)!`, `st_blksize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blocks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs an instance with the given field values. |
| [StructStat](https://developer.android.com/reference/kotlin/android/system/StructStat#StructStat(kotlin.Long,%20kotlin.Long,%20kotlin.Int,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`st_dev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ino:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_nlink:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_uid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_gid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st_rdev:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_atime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_mtime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_ctime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blksize:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `st_blocks:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs an instance with the given field values. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/system/StructStat#toString())`()` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)! | [st_atim](https://developer.android.com/reference/kotlin/android/system/StructStat#st_atim:android.system.StructTimespec) StructTimespec with time of last access. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_atime](https://developer.android.com/reference/kotlin/android/system/StructStat#st_atime:kotlin.Long) Seconds part of time of last access. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_blksize](https://developer.android.com/reference/kotlin/android/system/StructStat#st_blksize:kotlin.Long) A file system-specific preferred I/O block size for this object. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_blocks](https://developer.android.com/reference/kotlin/android/system/StructStat#st_blocks:kotlin.Long) Number of blocks allocated for this object. |
| [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)! | [st_ctim](https://developer.android.com/reference/kotlin/android/system/StructStat#st_ctim:android.system.StructTimespec) StructTimespec with time of last status change. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_ctime](https://developer.android.com/reference/kotlin/android/system/StructStat#st_ctime:kotlin.Long) Seconds part of time of last status change |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_dev](https://developer.android.com/reference/kotlin/android/system/StructStat#st_dev:kotlin.Long) Device ID of device containing file. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_gid](https://developer.android.com/reference/kotlin/android/system/StructStat#st_gid:kotlin.Int) Group ID of file. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_ino](https://developer.android.com/reference/kotlin/android/system/StructStat#st_ino:kotlin.Long) File serial number (inode). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_mode](https://developer.android.com/reference/kotlin/android/system/StructStat#st_mode:kotlin.Int) Mode (permissions) of file. |
| [StructTimespec](https://developer.android.com/reference/kotlin/android/system/StructTimespec)! | [st_mtim](https://developer.android.com/reference/kotlin/android/system/StructStat#st_mtim:android.system.StructTimespec) StructTimespec with time of last modification. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_mtime](https://developer.android.com/reference/kotlin/android/system/StructStat#st_mtime:kotlin.Long) Seconds part of time of last data modification. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_nlink](https://developer.android.com/reference/kotlin/android/system/StructStat#st_nlink:kotlin.Long) Number of hard links to the file. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_rdev](https://developer.android.com/reference/kotlin/android/system/StructStat#st_rdev:kotlin.Long) Device ID (if file is character or block special). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [st_size](https://developer.android.com/reference/kotlin/android/system/StructStat#st_size:kotlin.Long) For regular files, the file size in bytes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [st_uid](https://developer.android.com/reference/kotlin/android/system/StructStat#st_uid:kotlin.Int) User ID of file. |

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
