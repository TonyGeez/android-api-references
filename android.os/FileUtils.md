Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileUtils

Kotlin | [Java](https://developer.android.com/reference/android/os/FileUtils "View this page in Java")

```
class FileUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.FileUtils](https://developer.android.com/reference/kotlin/android/os/FileUtils#) |

Utility methods useful for working with files.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener` Listener that is called periodically as progress is made. |

| Public methods ||
|---|---|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#closeQuietly(java.io.FileDescriptor)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#?)` Closes the given object quietly, ignoring any checked exceptions. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#closeQuietly(java.lang.AutoCloseable)(closeable: https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#?)` Closes the given object quietly, ignoring any checked exceptions. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#copy(java.io.FileDescriptor,%20java.io.FileDescriptor)(in: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, out: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)` Copy the contents of one FD to another. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#copy(java.io.FileDescriptor,%20java.io.FileDescriptor,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.FileUtils.ProgressListener)(in: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, out: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, listener: https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener?)` Copy the contents of one FD to another. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#copy(java.io.InputStream,%20java.io.OutputStream)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#, out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)` Copy the contents of one stream to another. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/os/FileUtils#copy(java.io.InputStream,%20java.io.OutputStream,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.FileUtils.ProgressListener)(in: https://developer.android.com/reference/kotlin/java/io/InputStream.html#, out: https://developer.android.com/reference/kotlin/java/io/OutputStream.html#, signal: https://developer.android.com/reference/kotlin/android/os/CancellationSignal?, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?, listener: https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener?)` Copy the contents of one stream to another. |

## Public methods

### closeQuietly

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun closeQuietly(fd: FileDescriptor?): Unit
```

**Deprecated:** *This method may suppress potentially significant exceptions, particularly when closing writable resources. With a writable resource, a failure thrown from `close()` should be considered as significant as a failure thrown from a write method because it may indicate a failure to flush bytes to the underlying resource.*

Closes the given object quietly, ignoring any checked exceptions. Does nothing if the given object is `null`.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)?: This value may be `null`. |

### closeQuietly

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun closeQuietly(closeable: AutoCloseable?): Unit
```

**Deprecated:** *This method may suppress potentially significant exceptions, particularly when closing writable resources. With a writable resource, a failure thrown from `close()` should be considered as significant as a failure thrown from a write method because it may indicate a failure to flush bytes to the underlying resource.*

Closes the given object quietly, ignoring any checked exceptions. Does nothing if the given object is `null`.

| Parameters ||
|---|---|
| `closeable` | [AutoCloseable](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#)?: This value may be `null`. |

### copy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copy(
    in: FileDescriptor, 
    out: FileDescriptor
): Long
```

Copy the contents of one FD to another.

Attempts to use several optimization strategies to copy the data in the kernel before falling back to a userspace copy as a last resort.

| Parameters ||
|---|---|
| `in` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): This value cannot be `null`. |
| `out` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | number of bytes copied. |

### copy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copy(
    in: FileDescriptor, 
    out: FileDescriptor, 
    signal: CancellationSignal?, 
    executor: Executor?, 
    listener: FileUtils.ProgressListener?
): Long
```

Copy the contents of one FD to another.

Attempts to use several optimization strategies to copy the data in the kernel before falling back to a userspace copy as a last resort.

| Parameters ||
|---|---|
| `in` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): This value cannot be `null`. |
| `out` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): This value cannot be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal)?: to signal if the copy should be cancelled early. This value may be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?: that listener events should be delivered via. This value may be `null`. |
| `listener` | [FileUtils.ProgressListener](https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener)?: to be periodically notified as the copy progresses. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | number of bytes copied. |

### copy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copy(
    in: InputStream, 
    out: OutputStream
): Long
```

Copy the contents of one stream to another.

Attempts to use several optimization strategies to copy the data in the kernel before falling back to a userspace copy as a last resort.

| Parameters ||
|---|---|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#): This value cannot be `null`. |
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | number of bytes copied. |

### copy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun copy(
    in: InputStream, 
    out: OutputStream, 
    signal: CancellationSignal?, 
    executor: Executor?, 
    listener: FileUtils.ProgressListener?
): Long
```

Copy the contents of one stream to another.

Attempts to use several optimization strategies to copy the data in the kernel before falling back to a userspace copy as a last resort.

| Parameters ||
|---|---|
| `in` | [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#): This value cannot be `null`. |
| `out` | [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#): This value cannot be `null`. |
| `signal` | [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal)?: to signal if the copy should be cancelled early. This value may be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)?: that listener events should be delivered via. This value may be `null`. |
| `listener` | [FileUtils.ProgressListener](https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener)?: to be periodically notified as the copy progresses. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | number of bytes copied. |
