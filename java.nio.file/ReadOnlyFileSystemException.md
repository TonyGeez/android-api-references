# ReadOnlyFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadOnlyFileSystemException

```
open class ReadOnlyFileSystemException : UnsupportedOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java/lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) ||
| | | | | ↳ | [java.nio.file.ReadOnlyFileSystemException](../java/nio/file/ReadOnlyFileSystemException.md) |

Unchecked exception thrown when an attempt is made to update an object associated with a [read-only](../java/nio/file/FileSystem.md))`FileSystem`.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReadOnlyFileSystemException](../java/nio/file/ReadOnlyFileSystemException.md))`()` Constructs an instance of this class. |

## Public constructors

### ReadOnlyFileSystemException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReadOnlyFileSystemException()
```

Constructs an instance of this class.
