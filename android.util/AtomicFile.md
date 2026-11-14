Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicFile

Kotlin | [Java](../android/util/AtomicFile.md)
| --- | --- |

```
open class AtomicFile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.AtomicFile](../android/util/AtomicFile.md) |

Helper class for performing atomic operations on a file by writing to a new file and renaming it into the place of the original file after the write has successfully completed. If you need this on older versions of the platform you can use androidx.core.util.AtomicFile in AndroidX.

Atomic file guarantees file integrity by ensuring that a file has been completely written and sync'd to disk before renaming it to the original file. Previously this is done by renaming the original file to a backup file beforehand, but this approach couldn't handle the case where the file is created for the first time. This class will also handle the backup file created by the old implementation properly.

Atomic file does not confer any file locking semantics. Do not use this class when the file may be accessed or modified concurrently by multiple threads or processes. The caller is responsible for ensuring appropriate mutual exclusion invariants whenever it accesses the file.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/AtomicFile#AtomicFile(java.io.File)(baseName: https://developer.android.com/reference/kotlin/java/io/File.html#!)` Create a new AtomicFile for a file located at the given File path. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#delete()()` Delete the atomic file. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#failWrite(java.io.FileOutputStream)(str: https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!)` Call when you have failed for some reason at writing to the stream returned by `https://developer.android.com/reference/kotlin/android/util/AtomicFile#startWrite()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#finishWrite(java.io.FileOutputStream)(str: https://developer.android.com/reference/kotlin/java/io/FileOutputStream.html#!)` Call when you have successfully finished writing to the stream returned by `https://developer.android.com/reference/kotlin/android/util/AtomicFile#startWrite()`. |
| --- | --- |
| open [File](../java/io/File.md)! | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#getBaseFile()()` Return the path to the base file. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#getLastModifiedTime()()` Gets the last modified time of the atomic file. |
| open [FileInputStream](../java/io/FileInputStream.md)! | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#openRead()()` Open the atomic file for reading. |
| --- | --- |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#readFully()()` A convenience for `https://developer.android.com/reference/kotlin/android/util/AtomicFile#openRead()` that also reads all of the file contents into a byte array which is returned. |
| open [FileOutputStream](../java/io/FileOutputStream.md)! | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#startWrite()()` Start a new write operation on the file. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/util/AtomicFile#toString()()` Returns a string representation of the object. |
| --- | --- |

## Public constructors

### AtomicFile

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AtomicFile(baseName: File!)
```

Create a new AtomicFile for a file located at the given File path. The new file created when writing will be the same file path with ".new" appended.

## Public methods

### delete

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun delete(): Unit
```

Delete the atomic file. This deletes both the base and new files.

### failWrite

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun failWrite(str: FileOutputStream!): Unit
```

Call when you have failed for some reason at writing to the stream returned by `https://developer.android.com/reference/kotlin/android/util/AtomicFile#startWrite()`. This will close the current write stream, and delete the new file.

### finishWrite

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishWrite(str: FileOutputStream!): Unit
```

Call when you have successfully finished writing to the stream returned by `https://developer.android.com/reference/kotlin/android/util/AtomicFile#startWrite()`. This will close, sync, and commit the new data. The next attempt to read the atomic file will return the new file stream.

### getBaseFile

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBaseFile(): File!
```

Return the path to the base file. You should not generally use this, as the data at that path may not be valid.

### getLastModifiedTime

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLastModifiedTime(): Long
```

Gets the last modified time of the atomic file. 
Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | last modified time in milliseconds since epoch. Returns zero if the file does not exist or an I/O error is encountered. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |

### openRead

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openRead(): FileInputStream!
```

Open the atomic file for reading. You should call close() on the FileInputStream when you are done reading from it.

You must do your own threading protection for access to AtomicFile.

### readFully

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun readFully(): ByteArray!
```

A convenience for `https://developer.android.com/reference/kotlin/android/util/AtomicFile#openRead()` that also reads all of the file contents into a byte array which is returned.

### startWrite

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun startWrite(): FileOutputStream!
```

Start a new write operation on the file. This returns a FileOutputStream to which you can write the new file data. The existing file is replaced with the new data. You *must not* directly close the given FileOutputStream; instead call either `https://developer.android.com/reference/kotlin/android/util/AtomicFile#finishWrite(java.io.FileOutputStream)` or `https://developer.android.com/reference/kotlin/android/util/AtomicFile#failWrite(java.io.FileOutputStream)`.

Note that if another thread is currently performing a write, this will simply replace whatever that thread is writing with the new file being written by this thread, and when the other thread finishes the write the new write operation will no longer be safe (or will be lost). You must do your own threading protection for access to AtomicFile.

### toString

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
