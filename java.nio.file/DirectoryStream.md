# DirectoryStream

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DirectoryStream

```
interface DirectoryStream<T : Any!> : Closeable, MutableIterable<T>
```

| [java.nio.file.DirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream#) |

| Known Direct Subclasses [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [SecureDirectoryStream](https://developer.android.com/reference/kotlin/java/nio/file/SecureDirectoryStream) | A`DirectoryStream`that defines operations on files that are located relative to an open directory. | |

An object to iterate over the entries in a directory. A directory stream allows for the convenient use of the for-each construct to iterate over a directory.

**While`DirectoryStream`extends`Iterable`, it is not a general-purpose`Iterable`as it supports only a single`Iterator`; invoking the [iterator](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream#iterator())method to obtain a second or subsequent iterator throws`IllegalStateException`.**

An important property of the directory stream's`Iterator`is that its [hasNext](https://developer.android.com/reference/kotlin/java/util/Iterator.html#hasNext())method is guaranteed to read-ahead by at least one element. If`hasNext`method returns`true`, and is followed by a call to the`next`method, it is guaranteed that the`next`method will not throw an exception due to an I/O error, or because the stream has been [closed](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close()). The`Iterator`does not support the [remove](https://developer.android.com/reference/kotlin/java/util/Iterator.html#remove())operation.

A`DirectoryStream`is opened upon creation and is closed by invoking the`close`method. Closing a directory stream releases any resources associated with the stream. Failure to close the stream may result in a resource leak. The try-with-resources statement provides a useful construct to ensure that the stream is closed: 

```kotlin
Path dir = ...
    try (DirectoryStream<Path> stream = Files.newDirectoryStream(dir)) {
        for (Path entry: stream) {
            ...
        }
    }
  
```

Once a directory stream is closed, then further access to the directory, using the`Iterator`, behaves as if the end of stream has been reached. Due to read-ahead, the`Iterator`may return one or more elements after the directory stream has been closed. Once these buffered elements have been read, then subsequent calls to the`hasNext`method returns`false`, and subsequent calls to the`next`method will throw`NoSuchElementException`.

A directory stream is not required to be*asynchronously closeable* . If a thread is blocked on the directory stream's iterator reading from the directory, and another thread invokes the`close`method, then the second thread may block until the read operation is complete.

If an I/O error is encountered when accessing the directory then it causes the`Iterator`'s`hasNext`or`next`methods to throw [DirectoryIteratorException](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryIteratorException) with the [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) as the cause. As stated above, the`hasNext`method is guaranteed to read-ahead by at least one element. This means that if`hasNext`method returns`true`, and is followed by a call to the`next`method, then it is guaranteed that the`next`method will not fail with a`DirectoryIteratorException`.

The elements returned by the iterator are in no specific order. Some file systems maintain special links to the directory itself and the directory's parent directory. Entries representing these links are not returned by the iterator.

The iterator is*weakly consistent* . It is thread safe but does not freeze the directory while iterating, so it may (or may not) reflect updates to the directory that occur after the`DirectoryStream`is created.

**Usage Examples:**Suppose we want a list of the source files in a directory. This example uses both the for-each and try-with-resources constructs. 

```kotlin
List<Path> listSourceFiles(Path dir) throws IOException {
        List<Path> result = new ArrayList<>();
        try (DirectoryStream<Path> stream = Files.newDirectoryStream(dir, "*.{c,h,cpp,hpp,java}")) {
            for (Path entry: stream) {
                result.add(entry);
            }
        } catch (DirectoryIteratorException ex) {
            // I/O error encounted during the iteration, the cause is an IOException
            throw ex.getCause();
        }
        return result;
    }
  
```

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Filter](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream.Filter) An interface that is implemented by objects that decide if a directory entry should be accepted or filtered. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<T\> | [iterator](https://developer.android.com/reference/kotlin/java/nio/file/DirectoryStream#iterator())`()` Returns the iterator associated with this`DirectoryStream`. |

| Inherited functions ||
|---|---|
| From class [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable.html#) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close())`()` <br /> Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect. As noted in [AutoCloseable.close()](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close()), cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally*mark* the`Closeable`as closed, prior to throwing the`IOException`. <br /> | ||

## Public methods

### iterator

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<T>
```

Returns the iterator associated with this`DirectoryStream`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<T> | the iterator associated with this`DirectoryStream` |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if this directory stream is closed or the iterator has already been returned |
