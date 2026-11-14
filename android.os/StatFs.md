# StatFs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatFs

Kotlin| [Java](https://developer.android.com/reference/android/os/StatFs "View this page in Java") 
| --- | --- |

```
open class StatFs
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.StatFs](https://developer.android.com/reference/kotlin/android/os/StatFs#) |

Retrieve overall information about the space on a filesystem. This is a wrapper for Unix statvfs().

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StatFs](https://developer.android.com/reference/kotlin/android/os/StatFs#StatFs(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a new StatFs for looking at the stats of the filesystem at`path`. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableBlocks](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBlocks())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAvailableBlocksLong](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBlocksLong())`()` The number of blocks that are free on the file system and available to applications. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAvailableBytes](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBytes())`()` The number of bytes that are free on the file system and available to applications. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBlockCount](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockCount())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBlockCountLong](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockCountLong())`()` The total number of blocks on the file system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBlockSize](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockSize())`()` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBlockSizeLong](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockSizeLong())`()` The size, in bytes, of a block on the file system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFreeBlocks](https://developer.android.com/reference/kotlin/android/os/StatFs#getFreeBlocks())`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeBlocksLong](https://developer.android.com/reference/kotlin/android/os/StatFs#getFreeBlocksLong())`()` The total number of blocks that are free on the file system, including reserved blocks (that are not available to normal applications). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeBytes](https://developer.android.com/reference/kotlin/android/os/StatFs#getFreeBytes())`()` The number of bytes that are free on the file system, including reserved blocks (that are not available to normal applications). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalBytes](https://developer.android.com/reference/kotlin/android/os/StatFs#getTotalBytes())`()` The total number of bytes supported by the file system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restat](https://developer.android.com/reference/kotlin/android/os/StatFs#restat(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform a restat of the file system referenced by this object. |
| --- | --- |

## Public constructors

### StatFs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StatFs(path: String!)
```

Construct a new StatFs for looking at the stats of the filesystem at`path`. Upon construction, the stat of the file system will be performed, and the values retrieved available from the methods on this class.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:path in the desired file system to stat. |

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the file system access fails |

## Public methods

### getAvailableBlocks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableBlocks(): Int
```

**Deprecated:** *Use [getAvailableBlocksLong()](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBlocksLong())instead.* 

### getAvailableBlocksLong

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableBlocksLong(): Long
```

The number of blocks that are free on the file system and available to applications. This corresponds to the Unix`statvfs.f_bavail`field. 

### getAvailableBytes

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAvailableBytes(): Long
```

The number of bytes that are free on the file system and available to applications. 

### getBlockCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockCount(): Int
```

**Deprecated:** *Use [getBlockCountLong()](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockCountLong())instead.* 

### getBlockCountLong

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockCountLong(): Long
```

The total number of blocks on the file system. This corresponds to the Unix`statvfs.f_blocks`field. 

### getBlockSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockSize(): Int
```

**Deprecated:** *Use [getBlockSizeLong()](https://developer.android.com/reference/kotlin/android/os/StatFs#getBlockSizeLong())instead.* 

### getBlockSizeLong

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBlockSizeLong(): Long
```

The size, in bytes, of a block on the file system. This corresponds to the Unix`statvfs.f_frsize`field. 

### getFreeBlocks

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBlocks(): Int
```

**Deprecated:** *Use [getFreeBlocksLong()](https://developer.android.com/reference/kotlin/android/os/StatFs#getFreeBlocksLong())instead.* 

### getFreeBlocksLong

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBlocksLong(): Long
```

The total number of blocks that are free on the file system, including reserved blocks (that are not available to normal applications). This corresponds to the Unix`statvfs.f_bfree`field. Most applications will want to use [getAvailableBlocksLong()](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBlocksLong())instead. 

### getFreeBytes

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBytes(): Long
```

The number of bytes that are free on the file system, including reserved blocks (that are not available to normal applications). Most applications will want to use [getAvailableBytes()](https://developer.android.com/reference/kotlin/android/os/StatFs#getAvailableBytes())instead. 

### getTotalBytes

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTotalBytes(): Long
```

The total number of bytes supported by the file system. 

### restat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restat(path: String!): Unit
```

Perform a restat of the file system referenced by this object. This is the same as re-constructing the object with the same file system path, and the new stat values are available upon return.

| Exceptions ||
|--------------------------------------|---------------------------------|
| `java.lang.IllegalArgumentException` | if the file system access fails |
