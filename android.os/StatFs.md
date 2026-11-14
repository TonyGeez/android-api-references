# StatFs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatFs

Kotlin| [Java](../android/os/StatFs.md) 
| --- | --- |

```
open class StatFs
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.StatFs](../android/os/StatFs.md) |

Retrieve overall information about the space on a filesystem. This is a wrapper for Unix statvfs().

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StatFs](../android/os/StatFs.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Construct a new StatFs for looking at the stats of the filesystem at`path`. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAvailableBlocks](../android/os/StatFs.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAvailableBlocksLong](../android/os/StatFs.md))`()` The number of blocks that are free on the file system and available to applications. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAvailableBytes](../android/os/StatFs.md))`()` The number of bytes that are free on the file system and available to applications. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBlockCount](../android/os/StatFs.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBlockCountLong](../android/os/StatFs.md))`()` The total number of blocks on the file system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBlockSize](../android/os/StatFs.md))`()` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBlockSizeLong](../android/os/StatFs.md))`()` The size, in bytes, of a block on the file system. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFreeBlocks](../android/os/StatFs.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeBlocksLong](../android/os/StatFs.md))`()` The total number of blocks that are free on the file system, including reserved blocks (that are not available to normal applications). |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFreeBytes](../android/os/StatFs.md))`()` The number of bytes that are free on the file system, including reserved blocks (that are not available to normal applications). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalBytes](../android/os/StatFs.md))`()` The total number of bytes supported by the file system. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restat](../android/os/StatFs.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Perform a restat of the file system referenced by this object. |
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

**Deprecated:** *Use [getAvailableBlocksLong()](../android/os/StatFs.md))instead.* 

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

**Deprecated:** *Use [getBlockCountLong()](../android/os/StatFs.md))instead.* 

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

**Deprecated:** *Use [getBlockSizeLong()](../android/os/StatFs.md))instead.* 

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

**Deprecated:** *Use [getFreeBlocksLong()](../android/os/StatFs.md))instead.* 

### getFreeBlocksLong

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBlocksLong(): Long
```

The total number of blocks that are free on the file system, including reserved blocks (that are not available to normal applications). This corresponds to the Unix`statvfs.f_bfree`field. Most applications will want to use [getAvailableBlocksLong()](../android/os/StatFs.md))instead. 

### getFreeBytes

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFreeBytes(): Long
```

The number of bytes that are free on the file system, including reserved blocks (that are not available to normal applications). Most applications will want to use [getAvailableBytes()](../android/os/StatFs.md))instead. 

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
