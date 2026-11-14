# FileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileDescriptor

```
class FileDescriptor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.io.FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#) |

Instances of the file descriptor class serve as an opaque handle to the underlying machine-specific structure representing an open file, an open socket, or another source or sink of bytes. The main practical use for a file descriptor is to create a`FileInputStream`or`FileOutputStream`to contain it.

Applications should not create their own file descriptors.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#FileDescriptor())`()` Constructs an (invalid) FileDescriptor object. |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sync](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#sync())`()` Force all system buffers to synchronize with the underlying device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [valid](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#valid())`()` Tests if this file descriptor object is valid. |

| Properties ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#)! | [err](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#err:java.io.FileDescriptor) A handle to the standard error stream. |
| static [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#)! | [in](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#in:java.io.FileDescriptor) A handle to the standard input stream. |
| static [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#)! | [out](https://developer.android.com/reference/kotlin/java/io/FileDescriptor#out:java.io.FileDescriptor) A handle to the standard output stream. |
| --- | --- |

## Public constructors

### FileDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileDescriptor()
```

Constructs an (invalid) FileDescriptor object.

## Public methods

### sync

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sync(): Unit
```

Force all system buffers to synchronize with the underlying device. This method returns after all modified data and attributes of this FileDescriptor have been written to the relevant device(s). In particular, if this FileDescriptor refers to a physical storage medium, such as a file in a file system, sync will not return until all in-memory modified copies of buffers associated with this FileDescriptor have been written to the physical medium. sync is meant to be used by code that requires physical storage (such as a file) to be in a known state For example, a class that provided a simple transaction facility might use sync to ensure that all changes to a file caused by a given transaction were recorded on a storage medium. sync only affects buffers downstream of this FileDescriptor. If any in-memory buffering is being done by the application (for example, by a BufferedOutputStream object), those buffers must be flushed into the FileDescriptor (for example, by invoking OutputStream.flush) before that data will be affected by sync.

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.SyncFailedException` | Thrown when the buffers cannot be flushed, or because the system cannot guarantee that all the buffers have been synchronized with physical media. |

### valid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun valid(): Boolean
```

Tests if this file descriptor object is valid.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the file descriptor object represents a valid, open file, socket, or other active I/O connection;`false`otherwise. |

## Properties

### err

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val err: FileDescriptor!
```

A handle to the standard error stream. Usually, this file descriptor is not used directly, but rather via the output stream known as`System.err`. 
**See Also**

- [java.lang.System#err](https://developer.android.com/reference/kotlin/java/lang/System.html#err:java.io.PrintStream) 

### in

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val in: FileDescriptor!
```

A handle to the standard input stream. Usually, this file descriptor is not used directly, but rather via the input stream known as`System.in`. 
**See Also**

- [java.lang.System#in](https://developer.android.com/reference/kotlin/java/lang/System.html#in:java.io.InputStream) 

### out

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val out: FileDescriptor!
```

A handle to the standard output stream. Usually, this file descriptor is not used directly, but rather via the output stream known as`System.out`. 
**See Also**

- [java.lang.System#out](https://developer.android.com/reference/kotlin/java/lang/System.html#out:java.io.PrintStream)
