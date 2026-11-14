Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileUtils

Kotlin | [Java](FileUtils.md)
| --- | --- |

```
class FileUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.FileUtils](FileUtils.md) |

Utility methods useful for working with files.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/FileUtils.ProgressListener` Listener that is called periodically as progress is made. |

| Public methods ||
|---|---|
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | closeQuietly Closes the given object quietly, ignoring any checked exceptions. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | closeQuietly Closes the given object quietly, ignoring any checked exceptions. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | copy Copy the contents of one FD to another. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | copy Copy the contents of one FD to another. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | copy Copy the contents of one stream to another. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | copy Copy the contents of one stream to another. |
| --- | --- |

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
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md)?: This value may be `null`. |

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
| `closeable` | [AutoCloseable](../java.lang/AutoCloseable.md)?: This value may be `null`. |

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
| `in` | [FileDescriptor](../java.io/FileDescriptor.md): This value cannot be `null`. |
| `out` | [FileDescriptor](../java.io/FileDescriptor.md): This value cannot be `null`. |

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
| `in` | [FileDescriptor](../java.io/FileDescriptor.md): This value cannot be `null`. |
| `out` | [FileDescriptor](../java.io/FileDescriptor.md): This value cannot be `null`. |
| `signal` | [CancellationSignal](CancellationSignal.md)?: to signal if the copy should be cancelled early. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: that listener events should be delivered via. This value may be `null`. |
| `listener` | [FileUtils.ProgressListener](../android/os/FileUtils.ProgressListener.md)?: to be periodically notified as the copy progresses. This value may be `null`. |

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
| `in` | [InputStream](../java.io/InputStream.md): This value cannot be `null`. |
| `out` | [OutputStream](../java.io/OutputStream.md): This value cannot be `null`. |

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
| `in` | [InputStream](../java.io/InputStream.md): This value cannot be `null`. |
| `out` | [OutputStream](../java.io/OutputStream.md): This value cannot be `null`. |
| `signal` | [CancellationSignal](CancellationSignal.md)?: to signal if the copy should be cancelled early. This value may be `null`. |
| --- | --- |
| `executor` | [Executor](../java.util.concurrent/Executor.md)?: that listener events should be delivered via. This value may be `null`. |
| `listener` | [FileUtils.ProgressListener](../android/os/FileUtils.ProgressListener.md)?: to be periodically notified as the copy progresses. This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | number of bytes copied. |
