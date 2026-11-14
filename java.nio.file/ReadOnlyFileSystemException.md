# ReadOnlyFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadOnlyFileSystemException

```
open class ReadOnlyFileSystemException : UnsupportedOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) ||
| | | | | ↳ | [java.nio.file.ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException#) |

Unchecked exception thrown when an attempt is made to update an object associated with a [read-only](https://developer.android.com/reference/kotlin/java/nio/file/FileSystem#isReadOnly())`FileSystem`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException#ReadOnlyFileSystemException())`()` Constructs an instance of this class. |

## Public constructors

### ReadOnlyFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadOnlyFileSystemException()
```

Constructs an instance of this class.
